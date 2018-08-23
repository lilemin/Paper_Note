# Inception-v4, Inception-ResNet and the Impact of Residual Connections on Learning
## Related Work
- [ResNet](https://www.cv-foundation.org/openaccess/content_cvpr_2016/papers/He_Deep_Residual_Learning_CVPR_2016_paper.pdf): 
残差连接对于训练深度聚集神经网络是非常重要的
- [Inception_v4](https://arxiv.org/abs/1602.07261): 残差连接所带来的潜在优势可能需要在更深网络结构中来展现。在实验部分，
展示了不使用残差连接时深度网络的训练并不难做到。然而，使用残差连接能够极大的提高训练速度。

## Architectural Choices
### Pure Inception blocks
Inception家族训练方式的对比
### Residual Inception Blocks
**1. 滤波器扩张层（filter-expansion layer）**
- 实现： 1 × 1 convolution layer without activation
- 用途： 为与输入的深度相匹配，增大滤波器组（filter bank）的维度

**2. inception模块**
Item | Computetional cost
-----|--------------------
Inception-ResNet-v1|大致是Inception-v3的计算成本
Inception-ResNet-v2|与Inception-v4网络的原始成本相匹配








## Comparisons
Item | AlexNet | VGGNet | GoogLeNet | ResNet 
-----|---------|--------|-----------|-------
Parameter numbers | 60 million | 180 million |5 million 

