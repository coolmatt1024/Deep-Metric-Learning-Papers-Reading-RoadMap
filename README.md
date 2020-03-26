# Deep-Metric-Learning-Papers-Reading-RoadMap
a roadmap for deep metric learning(DML)

ER: extensive reading
IR: intensive reading

## Intro

metric leaning has some research directions

- batch construction
- sample in batch
- weight all the samples
- ensemble

the first three directions is all about hard negative mining

## relation of some loss function

<a href="https://www.codecogs.com/eqnedit.php?latex=L=y_{ij}Dij&plus;(1-y_{ij})[m-D_{ij}]_&plus;" target="_blank"><img src="https://latex.codecogs.com/gif.latex?L=y_{ij}Dij&plus;(1-y_{ij})[m-D_{ij}]_&plus;" title="L=y_{ij}Dij+(1-y_{ij})[m-D_{ij}]_+" /></a>

name | contrastive loss | triplet loss  |   
-|-|-|-|
original| ![](https://github.com/coolmatt1024/Deep-Metric-Learning-Papers-Reading-RoadMap/blob/master/papers/pictures/CodeCogsEqn.gif) | dd


## CVPR 2019

name | describe | comments   
-|-|-
Divide and Conquer the Embedding Space for Metric Learning |  难样本挖掘+类内差异|  [DCES-ER](https://github.com/coolmatt1024/Deep-Metric-Learning-Papers-Reading-RoadMap/blob/master/papers/DCES-ER.md) |
Stochastic Class-based Hard Example Mining for Deep Metric Learning |  batch构建 |  [SCHEM-ER](https://github.com/coolmatt1024/Deep-Metric-Learning-Papers-Reading-RoadMap/blob/master/papers/SCHEM-ER.md) |
Metric LearningWith HORDE |  模型结构 |  TODO |
