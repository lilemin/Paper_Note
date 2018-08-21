# Inception v1
## Motivation
提高神经网络性能的最直接方法，就是增加网络的深度，其中包括网络的levels，以及宽度（即每一个level的单元units数量）。但这会面临着两个主要缺陷：
  1. 更大更深的网络，意味着计算更多的参数，当训练集有限时，网络将会更容易过拟合
  2. 更大更深的网络，意味着耗费更多的计算资源
### Solution

* 卷积神经网络一般的结构组成：堆叠多个卷积层（选择性地紧跟着正则化 normalization 和最大值池化 max pooling），然后是一个或多个全连接层

### Configure
### 1×1 conv.layer
1. 主要用作降维模块，以降低计算量，否则会限制我们网络的规模;
2. 用于增加网络的深度，还可以增加网络的宽度，而不会显着降低性能

### Architectural Details
Inception的主要思想是，如何通过容易获得的密集组件来近似和覆盖卷积视觉网络的最佳局部稀疏结构。假设平移不变性意味着网络由convolutional building blocks构成并且在空间上不断重复该最佳局部稀疏结构。


### Training Methodology
Item | Choice
----------- | ----------- 
optimator | asynchronous stochastic gradient descent with 0.9 momentum
learning rate | fixed learning rate schedule (decreasing the learning rate by 4% every 8 epochs)
Polyak averaging | create the final model
some tricks | image sample / photometric distortions of Andrew Howard [8]
