---
title: Python使用技巧
tags: Python
key: key_11
pageview: true
---

## Conda 创建Liunx虚拟环境

1、查看当前存在的虚拟环境

`conda env list`

2、创建虚拟环境

`conda create -n env_name python=x.x`

3、激活虚拟环境

`conda activate env_name`

4、关闭虚拟环境

`conda deactivate`

5、删除虚拟环境

`conda remove -n env_name --all`

## 包含venv目录时激活与推出环境


1、激活虚拟环境

Linux:

`cd venv`

`source ./bin/activate`

Windows:

`cd venv`

`.\Scripts\activate.bat`

2、退出环境

Linux:

`deactive`

Windows:

`.\Scripts\deactivate.bat`

## 超算长时间占用计算节点

1、设置账户、计算资源类型、时间

`salloc -A account -p gpu --gres=gpu:1 -t 1-00:00:00`

2、新建会话

`tmux new -t session`

3、分离会话

`tmux detach`

## 参考文献

[阮一峰：Tmux使用教程](http://www.ruanyifeng.com/blog/2019/10/tmux.html)