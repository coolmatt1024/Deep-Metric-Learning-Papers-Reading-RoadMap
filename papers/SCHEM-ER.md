
## 出发点

当前构建batch的方法比较同统一
随机采样B个类，每个类采样K个样本，总的样本数目为BK

那么怎样更好地构建batch呢？这里对采样类和在类内采样样本都做了改进
有一些类之间天然比较相近

## 实现

### 前提

为每一个类学习一个signature

训练：triplet loss + cls loss，其中cls的weight即为每一个类的signature

$S(x, y)\approxS(x, W_y)\approxS(W_x, W_y)$

## 构建batch

选择一个候选类，从该类采样k个样本
- 根据k个样本，找出最近的一些类Pc
- 根据k个样本，从Pc中找出最近的一些样本

## 其他

改进了semi-hard采样
更换了池化方式
