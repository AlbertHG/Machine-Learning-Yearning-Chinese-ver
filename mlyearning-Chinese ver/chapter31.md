## 31. 解读学习曲线：其他情况

来看下面这个学习曲线图：

![](https://raw.githubusercontent.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/master/md_images/17.png)

这张趋势图体现出了高方差、高偏差还是两者都有？

这条蓝色的训练误差曲线相对较低，然后红色的这条开发误差曲线则远高于蓝色的训练误差曲线。因此，该情况属于偏差很小方差很大情况。则，增加更多的训练数据可能有助于减小开发误差和训练误差之间的差距。

现在，曲线图变成这样：

![](https://raw.githubusercontent.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/master/md_images/18.png)

这一次，训练误差（蓝线）变得很大，因为它远高于期望的性能水平（绿线）。而开发误差（红线）也比训练误差大得多。因此，这种情况同时存在这高方差和高偏差问题。你必须找到一种方法来减少算法中的高偏差和高方差。