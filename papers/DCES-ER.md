

## 出发点

Local similarity-aware deep feature embedding. 这篇文章指出了类内多样性可能造成类内距离大于类间距离，所以使用一个统一的指标可能会有问题。
> the global Euclidean distance cannot faithfully characterize the true feature similarity in a complex visual feature space


论文中的说法
>Existing approaches usually learn a single metric in the embedding space for all available data points, which may have a very complex non-uniform distribution with different notions of similarity between objects, e.g. ap- pearance, shape, color or semantic meaning.
所以，作者提出了一种分治法的思想，将样本根据嵌入特征聚成N类（减少了类内多样性），再对每一类分别学习嵌入特征

eg. 只有两类的度量学习任务：男人和女人；将这些细致地划分为中国人、美国人、俄罗斯人，分别学习，是不是任务要容易一点


## 具体实现

- 根据嵌入特征聚成K个类
- 使用每个类的样本分别学习一个嵌入特征

## 结果分析

original：72.7
加上聚类：75
聚类再加上分别学习特征：75.9

可以看出，聚类对结果提升比较明显，这实际上是一种难样本挖掘的有效方式；之前难样本挖掘往往有采样和加权两种方式，这里提供了一个新的思路。

作者还尝试了另一种聚类方式: 使用GT labels进行聚类（具体实现未知），但效果不是太好，说明特征聚类可以更有效地挖掘样本
