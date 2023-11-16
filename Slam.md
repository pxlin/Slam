# Slam

## 第一章ROS必备入门

### 1.1简介

#### 1.ROS是什么

机器人开发平台

①ROS是一个分布式通信框架

进程通信（程序）

+

网络通信（不同计算机）

②ROS是一个开发工具

③开源软件包

![ROS1](C:\Users\ASUS\Desktop\ROS1.png)

PS:没必要逐行看代码死记命令

### 1.2ROS开发环境搭建

Ubuntu ，ROS

### 1.3ROS系统架构

程序=进程=节点

话题通信，服务通信，动作通信

![8OOGJXM8ATO8B_5R@38X55E](C:\Users\ASUS\Desktop\8OOGJXM8ATO8B_5R@38X55E.png)

### 1..4ROS调试工具

![ROS3](C:\Users\ASUS\Desktop\ROS3.png)

第二行查看状态

第一行启动

多采用可视化工具

### <u>1.5ROS节点通信</u>

1.话题通信

节点①一>话题一>节点②

标准消息类型：https://wiki.ros.org/std_msgs

https://wiki.ros.org/sensor_msgs

https://wiki.ros.org/geometry_msgs

https://wiki.ros.org/nav_msgs

https://wiki.ros.org/actionlib_msgs

2.服务通信

服务消息类型自定义

3.动作通信

通信接口和通信协议（eg.HTTP)

### 1.6ROS其他重要概念

parameter

tf（坐标转换工具）

urdf（机器模型）

launch

plugin（插件）

nodelet（提高效率）

## 第二章C++编程范式

