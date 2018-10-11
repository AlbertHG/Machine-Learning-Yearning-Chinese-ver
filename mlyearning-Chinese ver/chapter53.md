## 53. 根据组件执行误差分析

假设你的系统是使用复杂的机器学习管道构建的，并且希望提高系统的性能，那么你应该对整个机器学习管道的哪一个部分进行改进呢？通过将错误归因于管道的特定部分，你可以决定如何确定工作的优先级。

让我们以我们的暹罗猫分类器作为示例：

![](https://raw.githubusercontent.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/master/md_images/29.png)

第一部分是猫分类器，负责探测图片中猫咪部分并把它们抠出来；第二部分是猫的品种分类器，用来判定抠出来的猫图是否是暹罗猫品种。改进两个组件中的任何一个都可能花费你数年的时间，那么你该决定关注哪个（些）组件呢？

通过根据组件执行误差分析，你可以尝试将算法所犯的每个错误归因于管道的两个部分中的一个（或两个）。例如：某张图片样本的正确标签为含有暹罗猫（$y=1$），算法却将其标签误分类为不含有暹罗猫（$y=0$）。

![](https://raw.githubusercontent.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/master/md_images/33.png)

让我们手动检查算法两个步骤的执行过程，假设猫检测器从下图中检测出一只猫：

![](https://raw.githubusercontent.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/master/md_images/34.png)

这意味着下图将作为猫咪品种分类器的输入：

![](https://raw.githubusercontent.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/master/md_images/35.png)

接下来，猫品种分类器将该输入正确分类为不包含暹罗猫。因此，作为猫品种分类器而言，输入包含一堆岩石的图片并输入一个 $y=0$ 的标签是没问题的。实际上，作为人而言，如果给出这样的图片，也会把它标签标定为 $y=0$ 。因此，我们就可以得出，整个猫分类器管道出问题的地方在第一部分——猫探测器。

另一方面，如果猫探测器输出了以下边界框：

![](https://raw.githubusercontent.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/master/md_images/36.png)

你会得出如下结论，猫探测器是工作正常的，并且我们可以将出问题的组件定位在猫品种分类器上。

假设你遍历100个错误分类的开发集图像，并发现90个错误可归因于猫探测器，只有10个错误可归因于猫品种分类器。 那么你可以有把握地得出结论：应该更加关注如何改进猫探测器。

到目前为止，我们关于如何将误差归因于管道的某个组件的描述是非正式的：你查看每个部分的输出，看看是否可以决定哪个部分出错了。这种非正式的方法可能就是你所需要的。但在下一章中，你还将看到一种更正式的误差归因方式。