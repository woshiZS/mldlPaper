## 翻译与提炼（会附带一些相关背景知识的介绍）

### Abstract

现有的声音增强技术都在spectral domain或者更高层次上的feature上操作，并且抗干扰能力很小，因此引入segan这个泛化用于语音增强的框架

### Introduction

语音增强主要为了增强语音信号和可辨识度，经典的enhancement methods:

* spectral subtraction
* Wiener filtering
* Statistical model-based methods
* Subspace algorithm

目前主流的增强多采用LSTM网络进行学习训练（在RNN基础上多了输入控制，输出控制以及忘记控制）用于降去除噪声。

傅里叶变换和短时傅里叶变换