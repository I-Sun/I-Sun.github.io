# ImageNet Classification with Deep Convolutional Neural Networks

---

## 摘要 Abstract

作者训练（设计）一个卷积神经网络在大规模图像识别中取得了当前最好得结果。并参加了ImageNet2012图像识别比赛获得冠军，其成绩远远领先于第二名。

```
AlexNet特点简述：
	6000万个参数，650万个神经元
	五个卷积层，三个全连接层，中间包含池化层（max pooling）,采用softmax对1000类物品进行分类
	为了训练更快：采用不饱和神经元（分布式训练，局部连接），GPU加速训练
	提出了dropout的正则化技术放置网络过拟合
```

---

## 1 介绍 Introduction



---

## 2 数据集 The Dataset

---

## 3 网络结构 The Architecture

### 3.1 非线性激活函数Relu

### 3.2 多GPU训练

### 3.3 局部响应归一化  Local Response Normalization

### 3.4 重叠的池化层 Overlapping Pooling

### 3.5 网络总体架构 Overall Architecture



---

## 4 减少过拟合 Reducing Overfitting

### 4.1 数据增广

### 4.2 Dropout

---

## 5 训练细节 Details of learning

---

## 6 结论 Results

### 6.1 定性评估 Qualitative Evaluations

---

## 7 讨论 Discussion

