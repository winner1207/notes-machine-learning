# 二、单变量线性回归(Linear Regression with One Variable) 
![](https://github.com/winner1207/notes-machine-learning/raw/master/resource/chapter02/info.png)

## 2.1 模型表示
我们的第一个学习算法是线性回归算法。在这段视频中，你会看到这个算法的概况，更重要的是你将会了解监督学习过程完整的流程。

让我们通过一个例子来开始：这个例子是预测住房价格的，我们要使用一个数据集，数据集包含俄勒冈州波特兰市的住房价格。在这里，我要根据不同房屋尺寸所售出的价格，画出我的数据集。比方说，如果你朋友的房子是 1250 平方尺大小，你要告诉他们这房子能卖多少钱。那么，你可以做的一件事就是构建一个模型，也许是条直线，从这个数据模型上来看，也许你可以告诉你的朋友，他能以大约 220000(美元)左右的价格卖掉这个房子。这就是监督学习算法的一个例子。

![](https://github.com/winner1207/notes-machine-learning/raw/master/resource/chapter02/1.png)
它被称作监督学习是因为对于每个数据来说，我们给出了“正确的答案”，即告诉我们：根据我们的数据来说，房子实际的价格是多少，而且，更具体来说，这是一个回归问题。回归一词指的是，我们根据之前的数据预测出一个准确的输出值，对于这个例子就是价格，同时，还有另一种最常见的监督学习方式，叫做分类问题，当我们想要预测离散的输出值，例如，我们正在寻找癌症肿瘤，并想要确定肿瘤是良性的还是恶性的，这就是 0/1 离散输出的问题。更进一步来说，在监督学习中我们有一个数据集，这个数据集被称训练集。

以之前的房屋交易问题为例，假使我们回归问题的训练集（Training Set）如下表所示：
![](https://github.com/winner1207/notes-machine-learning/raw/master/resource/chapter02/2.png)
我们将要用来描述这个回归问题的标记如下:
- m 代表训练集中实例的数量
- x 代表特征/输入变量
- y 代表目标变量/输出变量
- (x,y) 代表训练集中的实例
- (x(i),y(i) ) 代表第 i 个观察实例
- h 代表学习算法的解决方案或函数也称为假设（hypothesis）
![](https://github.com/winner1207/notes-machine-learning/raw/master/resource/chapter02/3.png)

这就是一个监督学习算法的工作方式，我们可以看到这里有我们的训练集里房屋价格我们把它喂给我们的学习算法，学习算法的工作了，然后输出一个函数，通常表示为小写 h表示。h 代表 hypothesis(假设) ，h 表示一个函数，输入是房屋尺寸大小，就像你朋友想出售的房屋，因此 h 根据输入的 x 值来得出 y 值，y 值对应房子的价格 因此，h 是一个从x 到 y 的函数映射。

我将选择最初的使用规则 h 代表 hypothesis，因而，要解决房价预测问题，我们实际上是要将训练集“喂”给我们的学习算法，进而学习得到一个假设 h，然后将我们要预测的房屋的尺寸作为输入变量输入给 h，预测出该房屋的交易价格作为输出变量输出为结果。那么，对于我们的房价预测问题，我们该如何表达 h？

一种可能的表达方式为：![](https://github.com/winner1207/notes-machine-learning/raw/master/resource/chapter02/4.png)， 因为只含有一个特征/输入变量，因此这样的问题叫作单变量线性回归问题。

## 2.2 代价函数
在这段视频中我们将定义代价函数的概念，这有助于我们弄清楚如何把最有可能的直线与我们的数据相拟合。如图：
![](https://github.com/winner1207/notes-machine-learning/raw/master/resource/chapter02/5.png)

在线性回归中我们有一个像这样的训练集，m 代表了训练样本的数量，比如 m = 47。而我们的假设函数，也就是用来进行预测的函数，是这样的线性函数形式：![](https://github.com/winner1207/notes-machine-learning/raw/master/resource/chapter02/4.png)

接下来我们会引入一些术语我们现在要做的便是为我们的模型选择合适的参数（parameters）θ0 和 θ1，在房价问题这个例子中便是直线的斜率和在 y 轴上的截距。

我们选择的参数决定了我们得到的直线相对于我们的训练集的准确程度，模型所预测的值与训练集中实际值之间的差距（下图中蓝线所指）就是建模误差（modeling error）。
![](https://github.com/winner1207/notes-machine-learning/raw/master/resource/chapter02/6.png)

我们的目标便是选择出可以使得建模误差的平方和能够最小的模型参数。 即使得代价函数![](https://github.com/winner1207/notes-machine-learning/raw/master/resource/chapter02/7.png)最小





