---
layout:     post                    # 使用的布局（不需要改）
title:      Pyorch Geometric安装报错              # 标题 
subtitle:   PyG安装报错的解决策略 #副标题
date:       2019-04-28              # 时间
author:     Tianbiao Yang                      # 作者
header-img: img/post-bg-2015.jpg    #这篇文章标题背景图片
catalog: true                       # 是否归档
tags:                               #标签
    - DL
---

# Pyorch Geometric安装报错

### 问题
```
$ RuntimeError: Detected that PyTorch and torch_spline_conv were compiled with different CUDA versions. PyTorch has CUDA version 10.0 and torch_spline_conv has CUDA version 0.0. Please reinstall the torch_spline_conv that matches your PyTorch install.
```
### 解决策略
```python
# Add this in a Google Colab cell to install the correct version of Pytorch Geometric.
import torch

def format_pytorch_version(version):
    return version.split('+')[0]

TORCH_version = torch.__version__
TORCH = format_pytorch_version(TORCH_version)

def format_cuda_version(version):
    return 'cu' + version.replace('.', '')

CUDA_version = torch.version.cuda
CUDA = format_cuda_version(CUDA_version)

!pip install torch-scatter==latest+{CUDA}     -f https://pytorch-geometric.com/whl/torch-{TORCH}.html
!pip install torch-sparse==latest+{CUDA}      -f https://pytorch-geometric.com/whl/torch-{TORCH}.html
!pip install torch-cluster==latest+{CUDA}     -f https://pytorch-geometric.com/whl/torch-{TORCH}.html
!pip install torch-spline-conv==latest+{CUDA} -f https://pytorch-geometric.com/whl/torch-{TORCH}.html
!pip install torch-geometric 

```