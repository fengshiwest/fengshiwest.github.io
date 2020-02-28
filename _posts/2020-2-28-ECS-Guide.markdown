---
layout: post
title: ECS Guide
date: 2020-02-26 15:32:24.000000000 +09:00
---

### ECS Guide & First Experience

#### 1. How to login it?

https://ecs.console.aliyun.com/

Login myself console website, then go to my bought list, where I can get the essential for my ECS. 

#### 2. How to connect it?

There are two ways for connect remotely, Workbench and VNC. 

For Workbench, the login window like this:

<img src="img\workbench window.png" alt="workbench window" style="zoom: 50%;" />



For VNC, the login window like this:

<img src="img\vnc window.png" alt="1582900023962" style="zoom: 33%;" />

Specially, these two password is different, the workbench password is the Operate System login password(contain capital letter, lowercase and digital), the vnc connect password is for just connecting(six digitals), after connecting, it is also necessary to login in for Operate System.

After inputting the correct username(if not change, root) and password, we just connect it.

#### 3. How can I get a graphic interface?

for a graphic interface, I use VNC Server and VNC Viewer, the main steps in following blogs:

https://blog.csdn.net/qq_35809147/article/details/93631634

https://www.jianshu.com/p/6bb261704952

generally, too long time leaving will result in the shut down for VNC Viewer, the way to restart it is kill the process of VNC Server then restart it. Use these two command:

kill: `vncserver -kill :1`

start: `vncserver`

#### 4. How can I startup PyCharm?

For more convenient to use python, I install Pycharm for help. But Unlike general Ubuntu System, I can't find a desktop icon for it. The step to open it is:

1. go to the folder where pycharm locates

   <img src="img\pycharm location" alt="1582901252447" style="zoom:50%;" />

2. use the command `bin/pycharm.sh` to start