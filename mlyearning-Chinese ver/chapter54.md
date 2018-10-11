## 54. 将误差归因到某个组件

让我们继续使用这个例子：

![](https://raw.githubusercontent.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/master/md_images/29.png)

假设猫检测器输出了这样的边界框：

![](https://raw.githubusercontent.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/master/md_images/37.png)

被裁减的图片将会作为猫品种分类器的输入，因此它给出了错误的分类结果 $y=0$, 即图片中没有猫。

![](https://raw.githubusercontent.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/master/md_images/38.png)

猫检测器的效果很糟糕。然而，一个技术娴熟的人仍然可以从这糟糕的裁剪图像中识别出暹罗猫。那么我们是否将此误差归因于猫检测器或猫品种分类器两者之一，或两者兼而有之？ 答案是模棱两可的。

如果像这样的模糊情况的数量很少，你可以做出你想要的任何决定并获得类似的结果。但是这里有一个更正式的测试方法，可以让你更明确地将错误归因于一个组件：

1. 用手动标记的边界框替换猫检测器的输出；
2. 通过猫品种分类器处理相应的裁剪图像。如果猫品种分类器仍将其错误地分类，则将误差归因于猫品种分类器。否则，将此误差归因于猫检测器；

![](https://raw.githubusercontent.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/master/md_images/39.png)

换句话说，跑一个实验，在其中为猫品种分类器提供「完美」输入，则会出现两种情况：

- 情况1：即使给出了一个「完美」的边界框，猫品种分类器仍然错误地输出 $y = 0$。 在这种情况下，很明显猫品种分类器是有问题的；
- 情况2：给定一个「完美」的边界框，品种分类器现在正确输出 $y = 1$。这表明如果只有猫探测器给出了一个更完美的边界框，那么整个系统的输出就是正确的。因此，我们将错误归因于猫探测器。

通过对开发集中误分类的图像执行此分析流程，你现在可以明确地将每个错误归因于一个组件。这允许你对整个管道的每个组件引起的错误程度进行分析，从而决定将注意力集中在哪一块。