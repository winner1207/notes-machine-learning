# 一、监督学习 vs 无监督学习
![](https://github.com/winner1207/notes-machine-learning/raw/master/resource/lecture01/info.png)
- ## 监督学习(Supervised Learning)
　　在监督学习中，给定一组数据，我们知道正确的输出结果应该是什么样子，并且知道在输入和输出之间有着一个特定的关系。这么说可能理解起来不是很清晰，没关系，后面有具体的例子。

- ### 监督学习的分类
　　监督学习可分为“回归”和“分类”问题。
![](https://github.com/winner1207/notes-machine-learning/raw/master/resource/lecture01/1.png)
　　在回归问题中，我们会预测一个连续值。也就是说我们试图将输入变量和输出用一个连续函数对应起来；而在分类问题中，我们会预测一个离散值，我们试图将输入变量与离散的类别对应起来。
　　下面举两个例子，就会非常清楚这几个概念了。

- ### 监督学习举例
- #### 回归
　　通过房地产市场的数据，预测一个给定面积的房屋的价格就是一个回归问题。这里我们可以把价格看成是面积的函数，它是一个连续的输出值。 但是，当把上面的问题改为“预测一个给定面积的房屋的价格是否比一个特定的价格高或者低”的时候，这就变成了一个分类问题, 因为此时的输出是‘高’或者‘低’两个离散的值。
![](https://github.com/winner1207/notes-machine-learning/raw/master/resource/lecture01/2.png)

- #### 分类
　　给定医学数据，通过肿瘤的大小来预测该肿瘤是恶性瘤还是良性瘤(课程中给的是乳腺癌的例子)，这就是一个分类问题，它的输出是0或者1两个离散的值。(0代表良性，1代表恶性)。
　　分类问题的输出可以多于两个，比如在该例子中可以有{0,1,2,3}四种输出，分别对应{良性, 第一类肿瘤, 第二类肿瘤, 第三类肿瘤}。
　　下图中上下两个图只是两种画法。第一个是有两个轴，Y轴表示是否是恶性瘤，X轴表示瘤的大小; 第二个是只用一个轴，但是用了不同的标记，用O表示良性瘤，X表示恶性瘤。
![](https://github.com/winner1207/notes-machine-learning/raw/master/resource/lecture01/3.png)
　　在这个例子中特征只有一个，那就是瘤的大小。 有时候也有两个或者多个特征, 例如下图， 有“年龄”和“肿瘤大小”两个特征。(还可以有其他许多特征，如下图右侧所示)
![](https://github.com/winner1207/notes-machine-learning/raw/master/resource/lecture01/4.png)

- ## 无监督学习
　　在无监督学习中，我们基本上不知道结果会是什么样子，但我们可以通过聚类的方式从数据中提取一个特殊的结构。在无监督学习中给定的数据是和监督学习中给定的数据是不一样的。在无监督学习中给定的数据没有任何标签或者说只有同一种标签。如下图所示：
![](https://github.com/winner1207/notes-machine-learning/raw/master/resource/lecture01/5.png)
　　如下图所示，在无监督学习中，我们只是给定了一组数据，我们的目标是发现这组数据中的特殊结构。例如我们使用无监督学习算法会将这组数据分成两个不同的簇,，这样的算法就叫聚类算法。
![](https://github.com/winner1207/notes-machine-learning/raw/master/resource/lecture01/6.png)

- ### 无监督学习举例
- #### 新闻分类
　　第一个例子举的是Google News的例子。Google News搜集网上的新闻，并且根据新闻的主题将新闻分成许多簇, 然后将在同一个簇的新闻放在一起。如图中红圈部分都是关于BP Oil Well各种新闻的链接，当打开各个新闻链接的时候，展现的都是关于BP Oil Well的新闻。
![](https://github.com/winner1207/notes-machine-learning/raw/master/resource/lecture01/7.png)

- #### 根据给定基因将人群分类
　　如图是DNA数据，对于一组不同的人我们测量他们DNA中对于一个特定基因的表达程度。然后根据测量结果可以用聚类算法将他们分成不同的类型。这就是一种无监督学习, 因为我们只是给定了一些数据，而并不知道哪些是第一种类型的人，哪些是第二种类型的人等等。
![](https://github.com/winner1207/notes-machine-learning/raw/master/resource/lecture01/8.png)


