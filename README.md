# Machine Learning Yearning

本项目是 Andrew NG 的关于机器学习策略的工具书的中文翻译稿源文件！（非商用翻译）

*欢迎Star*

更好的阅读体验，请移步本人博客：[博客传送门](https://alberthg.github.io/tags/#maching%20learning%20yearning)

本书的英文原稿全文已于2018年9月29日全部推送完毕，感谢 Andrew NG。

官网传送门：[https://www.deeplearning.ai/](https://www.deeplearning.ai/)  -OR-  [http://www.mlyearning.org/](http://www.mlyearning.org/)

目的
-------

根据NG的介绍，本书重点不是 ML 的算法，而是如何使 ML 算法发挥作用。琳琅满目的 ML 算法就像是工具箱里边的各种工具一样，这本书则是教会人们如何使用这些工具。

对于书名《Machine Learning Yearning》，我将其翻译为《机器学习要领》，希望能表达出 Andrew NG 编写这本书的目的:

> focused not on teaching you ML algorithms, but on how to make ML algorithms work.

经验即要领，同时单词「yearning」读音和「要领」相似，故以此名之。

在原稿中，Andrew NG 把每一个主题都浓缩到 1-2 页的阅读量，是非常精炼的：

- 1-4：绪论 「Introduction」；
- 5-12：配置开发集和训练集 「Setting up development and test sets」；
- 13-19：基本误差分析 「Basic Error Analysis」；
- 20-27：偏差和方差 「Bias and Variance」；
- 28-32：学习曲线 「Learning curves」；
- 33-35：比较人类水平表现 「Comparing to human-level performance」；
- 36-43：不同分布下的训练和测试 「Training and testing on different distributions」；
- 44-46：调试推理算法 「Debugging inference algorithms」；
- 47-52：端到端的深度学习 「End-to-end deep learning」；
- 53-57：根据组件执行误差分析 「Error analysis by parts」；
- 58：全书结语「Conclusion」。

翻译的水平有限（如有错误，请指出），而且有些地方是在经过自己的理解之后并尽量遵照原文进行翻译，只是希望尽可能的读起来通顺。

翻译稿
-------

在本书中，你将学习多达 50 多个 Andrew NG 多年总结的工程要领：

### 绪论 「Introduction」

[1、为什么需要机器学习策略](https://github.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/blob/master/mlyearning-Chinese%20ver/chapter1.md)

[2、如何利用本书帮助你的团队](https://github.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/blob/master/mlyearning-Chinese%20ver/chapter2.md)

[3、预备知识和符号约定](https://github.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/blob/master/mlyearning-Chinese%20ver/chapter3.md)

[4、规模化驱动下的机器学习发展](https://github.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/blob/master/mlyearning-Chinese%20ver/chapter4.md)

### 配置开发集和训练集 「Setting up development and test sets」

随着机器学习正朝着更大的数据集方向发展，关于配置开发/测试集的准则也在发生变化，本章内容将指导你如何在团队中调整机器学习策略，以及如何设置开发集和测试集，以适应现代化的机器学习项目。

[5、你的开发集和测试集](https://github.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/blob/master/mlyearning-Chinese%20ver/chapter5.md)

[6、发集和测试集应当服从同一分布](https://github.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/blob/master/mlyearning-Chinese%20ver/chapter6.md)

[7、开发集/测试集多大合适](https://github.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/blob/master/mlyearning-Chinese%20ver/chapter7.md)

[8、为团队进行算法优化建立单一数字评估指标](https://github.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/blob/master/mlyearning-Chinese%20ver/chapter8.md)

[9、优化和满足指标](https://github.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/blob/master/mlyearning-Chinese%20ver/chapter9.md)

[10、使用开发集和评估指标加速迭代](https://github.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/blob/master/mlyearning-Chinese%20ver/chapter10.md)

[11、何时更改开发/训练集和评估指标](https://github.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/blob/master/mlyearning-Chinese%20ver/chapter11.md)

[12、小结：设置开发和测试集](https://github.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/blob/master/mlyearning-Chinese%20ver/chapter12.md)

### 基本误差分析 「Basic Error Analysis」

本章内容将通过描述手动分析误差的流程，来为项目优化选择合适的方向。

[13、快速搭建第一个系统并开始迭代](https://github.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/blob/master/mlyearning-Chinese%20ver/chapter13.md)

[14、误差分析：查看开发集样本来评估想法](https://github.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/blob/master/mlyearning-Chinese%20ver/chapter14.md)

[15、在误差分析中并行评估多个想法](https://github.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/blob/master/mlyearning-Chinese%20ver/chapter15.md)

[16、清除标注错误的开发/测试集数据](https://github.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/blob/master/mlyearning-Chinese%20ver/chapter16.md)

[17、 如果你有一个很大的开发集，拆分为两半，并只关注其中一个](https://github.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/blob/master/mlyearning-Chinese%20ver/chapter17.md)

[18、眼球开发集和黑盒开发集应该多大](https://github.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/blob/master/mlyearning-Chinese%20ver/chapter18.md)

[19、小结：基本误差分析](https://github.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/blob/master/mlyearning-Chinese%20ver/chapter19.md)

### 偏差和方差 「Bias and Variance」

传统的关于偏差和方差的观点在现代机器学习项目中变得越来越不适用，是时候更新这些传统的指导方针了，本章将教你如何利用偏差和方差来优化现代机器学习项目。 

[20、偏差和方差：两大误差来源](https://github.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/blob/master/mlyearning-Chinese%20ver/chapter20.md)

[21、举例说明偏差和方差](https://github.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/blob/master/mlyearning-Chinese%20ver/chapter21.md)

[22、比较最优误差](https://github.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/blob/master/mlyearning-Chinese%20ver/chapter22.md)

[23、解决方差和偏差](https://github.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/blob/master/mlyearning-Chinese%20ver/chapter23.md)

[24、权衡偏差和方差](https://github.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/blob/master/mlyearning-Chinese%20ver/chapter24.md)

[25、减少可避免偏差的技巧](https://github.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/blob/master/mlyearning-Chinese%20ver/chapter25.md)

[26、在训练集上的误差分析](https://github.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/blob/master/mlyearning-Chinese%20ver/chapter26.md)

[27、减少方差的技巧](https://github.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/blob/master/mlyearning-Chinese%20ver/chapter27.md)

### 学习曲线 「Learning curves」

本章内容将提供一个更加丰富和直观的方式，来帮助你更好地将偏差归因到可避免偏差或者是方差上。

[28、诊断偏差和方差：学习曲线](https://github.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/blob/master/mlyearning-Chinese%20ver/chapter28.md)

[29、绘制训练误差曲线](https://github.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/blob/master/mlyearning-Chinese%20ver/chapter29.md)

[30、解读学习曲线：高偏差](https://github.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/blob/master/mlyearning-Chinese%20ver/chapter30.md)

[31、解读学习曲线：其他情况](https://github.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/blob/master/mlyearning-Chinese%20ver/chapter31.md)

[32、绘制学习曲线](https://github.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/blob/master/mlyearning-Chinese%20ver/chapter32.md)

### 比较人类水平表现 「Comparing to human-level performance」

本章内容将提出通过和人类表现水平的比较来加快机器学习发展的策略。学习算法的性能表现在越来越多的领域超越了人类水平表现，从语音识别到图像识别（狭义领域）。在深度学习领域，与人类水平表现竞争已然成为一项新兴的运动，当你的算法表现超越人类的时候会发生什么呢？

[33、为什么我们要比较人类表现水平](https://github.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/blob/master/mlyearning-Chinese%20ver/chapter33.md)

[34、如何定义人类水平表现](https://github.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/blob/master/mlyearning-Chinese%20ver/chapter34.md)

[35、超越人类表现水平](https://github.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/blob/master/mlyearning-Chinese%20ver/chapter35.md)

### 不同分布下的训练和测试 「Training and testing on different distributions」

本章内容将探讨当训练集的数据分布和开发/测试集的分布不一致的时候可能出现的情况。有时候不得不将与测试集不同分布的训练集用在构建模型上，那什么时候这种做法合适呢？如何确保你的算法表现总能在目标分布中表现良好呢？此外，本章同时将教会你如何诊断出数据不匹配，你也将学习如何解决数据不匹配的技术。

[36、当你不得不在不同分布中进行训练和测试](https://github.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/blob/master/mlyearning-Chinese%20ver/chapter36.md)

[37、如何决定是否使用所有数据](https://github.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/blob/master/mlyearning-Chinese%20ver/chapter37.md)

[38、如何决定是否包含不一致的数据](https://github.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/blob/master/mlyearning-Chinese%20ver/chapter38.md)

[39、数据加权](https://github.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/blob/master/mlyearning-Chinese%20ver/chapter39.md)

[40、从训练集到开发集的泛化](https://github.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/blob/master/mlyearning-Chinese%20ver/chapter40.md)

[41、辨别偏差、方差和数据不匹配导致的误差](https://github.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/blob/master/mlyearning-Chinese%20ver/chapter41.md)

[42、解决数据不匹配的问题](https://github.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/blob/master/mlyearning-Chinese%20ver/chapter42.md)

[43、人工合成数据](https://github.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/blob/master/mlyearning-Chinese%20ver/chapter43.md)

### 调试推理算法 「Debugging inference algorithms」

本章内容将探讨用于调试语音识别系统、机器翻译系统和增强学习系统的共享 AI 设计模式是什么?

[44、优化验证测试](https://github.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/blob/master/mlyearning-Chinese%20ver/chapter44.md)

[45、优化验证测试的一般形式](https://github.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/blob/master/mlyearning-Chinese%20ver/chapter45.md)

[46、强化学习的例子](https://github.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/blob/master/mlyearning-Chinese%20ver/chapter46.md)

### 端到端的深度学习 「End-to-end deep learning」

Andrew NG 提到他曾经负责开发过一个大型端到端语音识别系统，并取得的很好的效果，但是他同时表示盲目使用该技术并不是好事。本章内容将探讨什么是端到端的深度学习？ 什么时候应该使用它，什么时候应该避免它？同时给出了当不适合使用端到端学习技术之时，如何将机器学习任务分解成多个子任务的建议

[47、端到端学习技术的兴起](https://github.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/blob/master/mlyearning-Chinese%20ver/chapter47.md)

[48、更多的端到端学习的例子](https://github.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/blob/master/mlyearning-Chinese%20ver/chapter48.md)

[49、端到端学习的优点和缺点](https://github.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/blob/master/mlyearning-Chinese%20ver/chapter49.md)

[50、选择管道组件：数据可用性](https://github.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/blob/master/mlyearning-Chinese%20ver/chapter50.md)

[51、选择管道组件：任务简单性](https://github.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/blob/master/mlyearning-Chinese%20ver/chapter51.md)

[52、直接学习复杂的输出](https://github.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/blob/master/mlyearning-Chinese%20ver/chapter52.md)

### 根据组件执行误差分析 「Error analysis by parts」

本章学习到如何进行机器学习管道的误差分析，如何利用复杂系统的组件来为误差分析提供帮助。

[53、根据组件执行误差分析](https://github.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/blob/master/mlyearning-Chinese%20ver/chapter53.md)

[54、将误差归因到某个组件](https://github.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/blob/master/mlyearning-Chinese%20ver/chapter54.md)

[55、误差归因的一般情况](https://github.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/blob/master/mlyearning-Chinese%20ver/chapter55.md)

[56、组件误差分析与人类效率的比较](https://github.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/blob/master/mlyearning-Chinese%20ver/chapter56.md)

[57、发现有缺陷的机器学习管道](https://github.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/blob/master/mlyearning-Chinese%20ver/chapter57.md)

### 全书结语「Conclusion」

结语部分我把它和第57节合并了，没什么内容的！

[58、全书结语](https://github.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/blob/master/mlyearning-Chinese%20ver/chapter57.md)

🎉🎉🎉🎉 完结撒花 🎉🎉🎉🎉🎉

英文原稿
-------

详见文件夹：[「mlyearning-Draft」](https://github.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/tree/master/mlyearning-Draft)

- 「Ng_MLY01.pdf」：1-14 节
- 「Ng_MLY02.pdf」：15-19 节
- 「Ng_MLY03.pdf」：20-22 节
- 「Ng_MLY04.pdf」：23-27 节
- 「Ng_MLY05.pdf」：28-30 节
- 「Ng_MLY06.pdf」：31-32 节
- 「Ng_MLY07.pdf」：33-35 节
- 「Ng_MLY08.pdf」：36-39 节
- 「Ng_MLY09.pdf」：40-43 节
- 「Ng_MLY10.pdf」：44-46 节
- 「Ng_MLY11.pdf」：47-49 节
- 「Ng_MLY12.pdf」：50-52 节
- 「Ng_MLY13.pdf」：53-58 节

致谢
---------

感谢蒋兆函同学为翻译提供的建议！

License
-------

[知识共享署名-相同方式共享 4.0 国际许可协议（CC BY-SA 4.0）](https://creativecommons.org/licenses/by-sa/4.0/)

备注
-------

GitHub 的 README.md 文件不提供 LaTeX 公式解析，可使用 Chrome 浏览器插件 [GitHub with MathJax](https://chrome.google.com/webstore/detail/github-with-mathjax/ioemnmodlmafdkllaclgeombjnmnbima)
