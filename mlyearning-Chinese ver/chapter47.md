## 47. 端到端学习技术的兴起

假设您希望构建一个系统来检索关于在线购物网站上的产品评论，并自动通知你，用户是否喜欢或不喜欢该产品。例如，您希望识别出以下评论是属于积极评论：

- This is a great mop!

识别出以下评论是属于消极评论：

- This mop is low quality--I regret buying it.

识别正面和负面意见的机器学习问题被称为“情感分类”问题。为了建立这个系统，你可以构建一个由两部分组成的“管道(Pipeline)”：

1. 解析器(Parser)：一种用来标注文本内容中最重要的单词信息 [1] 的系统，例如，你可以使用解析器来标记文本中所有的形容词和名词，因此例子变成了下列所示的那样：
    - This is a $great_{Adjectve}$  $mop_{Noun}$!
2. 情感分类器( Sentiment classifier)：一种将带注释的文本作为输入，并预测整体情绪的学习算法。解析器的注释可以极大地帮助这个学习算法：通过给予形容词一个更高的权重，你的算法将能够快速地识别出那些重要的单词(如“great”)，同时忽略不那么重要的单词，例如“this”。

[1]: 解析器给出的文本注释要比这个丰富得多，但是这个简化的描述足以解释端到端的深度学习

我们将两个组件组成的“管道”可视化如下：

![20](https://raw.githubusercontent.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/master/md_images/20.png)

近期出现了用单一学习算法替代管道系统的趋势。这项任务的端到端学习算法尝试在仅输入原始文本“This is a great mop!”的情况下直接识别情绪的可能性：

![21](https://raw.githubusercontent.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/master/md_images/21.png)

神经网络通常用于端到端学习系统。术语“端到端(End-to-end)”指的是我们要求学习算法直接从输入到所需的输出。即，学习算法直接将系统的“输入端”连接到“输出端”。

在处理一些数据丰富的应用中，端到端学习算法非常成功。但这并不意味着它们总是一个好的选择。接下来的几章将给出更多的端到端系统的例子，并给出关于何时应该使用它们和不应该使用它们的建议。