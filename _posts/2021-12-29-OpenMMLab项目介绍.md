---
title：OpenMMLab开源项目介绍
tags：MMLab MMCV MMDetection ...
---

#	OpenMMLab是什么？

OpenMMLab项目是香港中文大学-商汤科技联合实验室 MMLab 开源的一个算法代码库平台，包含了众多计算机视觉方向的SOTA网络的实现。OpenMMLab项目的目的是：为计算机视觉的一些重要方向建立统一而开放的代码库，并不断把新的算法沉淀其中。避免研究者在为了复现他人的论文代码中遇到的各种各样问题的情况，极大的方便了研究者进行课堂研究。  

[官网链接]( https://mmcv.readthedocs.io/en/latest/ )

[git项目链接]( https://github.com/open-mmlab )

#	 OpenMMLab包含哪些方向？

**MMCV**：用于计算机视觉研究的基础Python库，支持OpenMMLab旗下其他开源库。 

**MMDetection**：基于PyTorch的开源目标检测工具箱。是OpenMMLab最知名的开源库，几乎是研究目标检测必备！ 

**MMDetection3D**：基于PyTorch的开源的3D目标检测的开源库。 

**MMSegmentation**：基于PyTorch的开源的语义分割工具箱. 

**MMClassification**：基于PyTorch的开源的图像分类工具箱。 

**MMPose**：基于PyTorch的开源姿势估计工具箱。 

**MMAction/MMAction2**：基于PyTorch开放源代码的工具箱，用于动作理解。 

**MMSkeleton**：用于人体姿势估计，基于骨架的动作识别和动作合成。

**MMFashion**：基于PyTorch的开源视觉时尚分析工具箱。 

**MMEditing**：基于PyTorch的开源图像和视频编辑工具箱主要特点： 

**OpenPCDet**：清晰，简单，自成体系的开源项目，用于基于LiDAR的3D目标检测。 

**OpenUnReID**：研究用于目标重识别的无监督学习和无监督域适应的开源库，基于PyTorch实现。 

**OpenSelfSup**：基于PyTorch的无监督表示学习工具箱。

**MMRazor**：用于模型压缩的工具箱。

...  

#	OpenMMLab在windows上的安装(Linux可参考官网)

在windows上安装MMCV会比在Linux上复杂点，需要预先安装以下的环境：

git/VScode/conda：安装方式参考[windows10+pytorch+conda深度学习环境安装教程](https://panie-0924.github.io/2021/12/29/windows10+pytorch+conda%E6%B7%B1%E5%BA%A6%E5%AD%A6%E4%B9%A0%E7%8E%AF%E5%A2%83%E5%AE%89%E8%A3%85%E6%95%99%E7%A8%8B.html)

##	安装MMCV

1、clone源码

`git clone https://github.com/open-mmlab/mmcv.git`

`cd mmcv`

2、安装python包

`pip3 install -r requirements/runtime.txt`

3、建议安装ninja加速编译

`pip install -r requirements/optional.txt`

4、编译MMCV

MMCV有2种编译方式：CPU、GPU。可以根据个人需要按需编译

CPU版本安装

```
##	简单安装
# activate environment
conda activate mmlab
# change directory
cd mmcv
# install
python setup.py develop
# check
pip list

##	CPU编译环境设置
$env:MMCV_WITH_OPS = 1
$env:MAX_JOBS = 8  # based on your available number of CPU cores and amount of memory

##	安装CPU版本
# activate environment
conda activate mmlab
# change directory
cd mmcv
# build
python setup.py build_ext # if success, cl will be launched to compile ops
# install
python setup.py develop
# check
pip list
```



<!--more-->