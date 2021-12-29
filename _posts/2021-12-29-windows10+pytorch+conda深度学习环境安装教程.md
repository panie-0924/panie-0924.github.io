---
title: windows10+pytorch+conda深度学习环境安装教程
tags: win10 pytorch conda git 深度学习
---

#	环境介绍

​	**win10**：Windows操作系统。

​	**VSCode**：一款最常用的代码编辑器。[下载地址](https://code.visualstudio.com/download ) 

​	**pytorch**：PyTorch是facebook推出的一个Python的开源机器学习库，前身是由Lua语言开发的torch这个机器学习框架。近几年广受学术界和工业界的热捧。

​	**cnoda**：conda是一个环境包，方便用于环境的管理，适用于多种语言，如：python、R、Java、Javascript、C/C++等等。[下载地址](https://www.anaconda.com/products/individual )

​	**git**：用于分布式版本系统的控制管理。[下载地址](https://git-scm.com/downloads )

#	安装步骤

## 第一步：安装conda

​	双击上面提供的安装包，无脑安装；

##	第二步：在conda下安装pytorch

​	**1、打开anaconda prompt**

​		![1640746150554](https://github.com/panie-0924/panie-0924.github.io/blob/4b0fb729346b9192b45810bc2ad481fb388dbaf9/typora-user-images/1640746150554.png)

​	**2、创建并切换到工作目录**

​		`mkdir mmlab` ##mmlab是项目名称，可以任意取，以下出现mmlab的都适用，保持一致

​		`cd mmlab`

​		![1640746150554](https://github.com/panie-0924/panie-0924.github.io/blob/4b0fb729346b9192b45810bc2ad481fb388dbaf9/typora-user-images/1640746302743.png)

​	**3、创建pytorch的conda虚拟环境**

​		`conda create --mmlabpytorch python=3.6`

​		![1640747018723](https://github.com/panie-0924/panie-0924.github.io/blob/4b0fb729346b9192b45810bc2ad481fb388dbaf9/typora-user-images/1640746584343.png)

​		后续，输入Y确认安装

​		创建好之后可以用一下命令查看目前conda有的虚拟环境

​		`conda info -e`

​		![1640747018723](https://github.com/panie-0924/panie-0924.github.io/blob/4b0fb729346b9192b45810bc2ad481fb388dbaf9/typora-user-images/1640746996801.png)

​	**4、启动Pytorch Anaconda虚拟环境**

​		`activate mmlab`

​		![1640747177011](https://github.com/panie-0924/panie-0924.github.io/blob/4b0fb729346b9192b45810bc2ad481fb388dbaf9/typora-user-images/1640747177011.png)

​	**5、安装pytorch**

​		pytorch官网： https://pytorch.org/ 

​		详细版本可以自己选择：

​		![1640747363531](https://github.com/panie-0924/panie-0924.github.io/blob/4b0fb729346b9192b45810bc2ad481fb388dbaf9/typora-user-images/1640747363531.png)

​		 `conda install pytorch torchvision torchaudio cudatoolkit=10.2 -c pytorch `



<!--more-->

---

