## 51. 选择管道组件：任务简单性

除了数据可用性之外，在选择管道组件时还应考虑第二个因素：单个组件需要解决的任务有多简单？ 您应该尽可能尝试选择那些易于构建或学习的管道组件。那么，对于一个管道组件来说，何谓之「易于」学习呢？

![26](https://raw.githubusercontent.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/master/md_images/26.png)

思考下列的机器学习任务，并按照从难到易的顺序依次列出：

1. 分类图像是否曝光过度（如上例所示）;
2. 分类图像是室内还是室外拍摄；
3. 分类图像是否包含猫；
4. 分类图像是否包含黑色和白色毛皮的猫；
5. 分类图像是否包含暹罗猫（特定品种的猫）。

上述任务每一个都是属于图像的二分类任务：输入图片，输出 0 或者 1。但是列表前面的知识似乎更容易让神经网络学习到。也即是说，用更少的样本训练更简单的任务。

到目前，机器学习还没有一个好的正式定义来定义是什么导致了一项任务变得容易或困难 [2]。但随着深度学习和多层神经网络的兴起，我们有时候会将那些只需要较少的计算步骤就能完成的任务定义为「容易」（对应于浅层神经网络）。而将那些需要更多的计算步骤才能完成的任务定义为「困难」（对应于深层神经网络）。但这都是非正式定义。

[2]： 信息论中有一个概念叫做：「柯尔莫哥洛夫复杂性（Kolmogorov Complexity）」——学习函数的复杂性等价于可以产生该函数的最短计算机程序的长度。然而，这一理论概念在人工智能中几乎没有实际应用。详见：[https：//en.wikipedia.org/wiki/Kolmogorov_complexity](https：//en.wikipedia.org/wiki/Kolmogorov_complexity)

如果您能够将一个复杂的任务，将其分解为更简单的子任务，那么通过显式地对子任务的步骤进行编码，你就给了算法先验知识，这可以帮助它更有效地学习一项任务。

![](https://raw.githubusercontent.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/master/md_images/27.png)

假设您正在构建一个暹罗猫检测器。 下列是一个纯粹的端到端学习架构：

![](https://raw.githubusercontent.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/master/md_images/28.png)

相比之下，您可以选择使用管道，步骤有两个:

![](https://raw.githubusercontent.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/master/md_images/29.png)

第一步（猫检测器）检测图像中的所有猫：

![](https://raw.githubusercontent.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/master/md_images/30.png)

然后，第二步将每个检测到的猫（一次一个）的裁剪图像传递给猫品种分类器，如果检测到的猫分类为是暹罗猫，则输出 1。

![](https://raw.githubusercontent.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/master/md_images/31.png)

与使用标签 0/1 训练纯粹的端到端分类器相比，管道中的两个组件中的每一个——猫探测器和猫品种分类器——似乎都更容易学习，并且只需要更少的数据[^3]。

[^3]:如果你熟悉对象物体检测算法，那么你应该知道它们不仅仅只学习 0/1 图像标签，而是使用作为训练数据的一部分提供的边界框进行训练。对他们的讨论超出了本书的范围，详见 Coursera （[http://deeplearning.ai​](http://deeplearning.ai​)），有相关课程专门讨论对象物体检测。

作为最后一个例子，让我们重新回顾之前的自动驾驶算法管道：

![](https://raw.githubusercontent.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/master/md_images/24.png)

通过使用这条管道，你可以告诉算法有 3 个关键步骤：（1）检测其他车辆；（2）检测行人；（3）为你的汽车规划道路。此外，与纯粹的端到端学习方法相比，这些方法都是一个相对简单的函数，因此可以用更少的数据来学习。

总之，在决定管道组件应该是什么时，尝试去构建一个管道，让其中每个组件都是一个相对「简单」的功能，从而让组件能够使用较少的数据进行学习。