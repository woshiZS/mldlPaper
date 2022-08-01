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



### github项目部署相关

* 首先就是wget获取对应版本的anaconda安装脚本（注意自己系统的架构，x86-64不适用与arm架构）使用```uname -a```可以查看自己的系统架构
* 另外就是conda创建虚拟环境的时候会有package not found的问题，针对我的特殊问题（需要创建python2.7的环境，但是conda创建的虚拟环境默认的Python版本就是2.7，所以直接创建无需指定python版本也是ok的
* 另外就是安装numpy的过程出现了一个问题，xlocale.h不存在，原因是在新版ubuntu中xlocale.h已经被locale.h取代。```sudo ln -s /usr/include/locale.h /usr/include/xlocale.h```创建软链接即可