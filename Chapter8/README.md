概率在现代模式识别中起着重要的作用。我们已经在第1章中看到了概率论可以使用两个简单的方程（加和规则和乘积规则）表示。本书中所有的概率推断以及学习操作，无论多么复杂，都是在重复使用这两个方程。因此，我们接下来将完全通过代数计算来对更加复杂的模型进行建模和求解。然而，我们会发现，使用概率分布的图形表示进行分析很有好处。这种概率分布的图形表示被称为概率图模型（probabilistic graphical models）。这些模型提供了几个有用的性质：    

* 它们提供了一种简单的方式将概率模型的结构可视化，可以用于设计新的模型。    
* 通过观察图形，我们可以更深刻地认识模型的性质，包括条件独立性质。    
* 高级模型的推断和学习过程中的复杂计算可以根据图计算表达，图隐式地承载了背后的数学表达式。     


一个图由结点（nodes）（也被称为端点（vertices））和它们之间的链接（links）（也被称为边（edges）或弧（arcs））组成。在概率图模型中，每个结点表示一个随机变量（或一组随机变量），链接表示这些变量之间的概率关系。这样，图描述了联合概率分布在所有随机变量上能够分解为一组因子的乘积的方式，每个因子只依赖于随机变量的一个子集。我们首先讨论贝叶斯网络（Bayesian network），也被称为有向图模型（directed graphicalmodel）。这个模型中，图之间的链接有一个特定的方向，使用箭头表示。另一大类图模型是马尔科夫随机场 （Markov random fields），也被称为无向图模型（undirected graphical models）。这个模型中，链接没有箭头，没有方向性质。有向图对于表达随机变量之间的因果关系很有用，而无向图对于表示随机变量之间的软限制比较有用。为了求解推断问题，通常比较方便的做法是把有向图 和无向图都转化为一个不同的表示形式，被称为因子图（factor graph）。    

本章中，我们会将注意力集中在那些能够用于模式识别和机器学习应用中的图模型的关键概念。关于图模型的更一般的讨论，可以参考Whittaker(1990)、Lauritzen( 1996)、Jensen(1996)、Castillo et al.(1997)、Jordan(1999)、Cowell et al.(1999)及Jordan(2007)。    


