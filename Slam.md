# Slam

## 第一章ROS必备入门

### 1.1简介

#### 1.ROS是什么

机器人开发平台

①ROS是一个分布式通信框架

进程通信（程序）+网络通信（不同计算机）

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

+ parameter

+ tf（坐标转换工具）

+ urdf（机器模型）

+ launch

+ plugin（插件）

+ nodelet（提高效率）

## 第二章C++编程范式

Python即写即执行，解释器->虚拟机->硬件

实时性（slam数据处理运行耗时影响信息传递的及时性）

### 2.1C++工程的组织结构

![image-20231116144356276](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20231116144356276.png)

初始数据，ROS（功能包）转换成数字传递给核心算法，得出结果后经ROS输出

![6B7BQV80Z~0EWDSIJ0Y6X34](C:\Users\ASUS\Documents\Tencent Files\2242688787\FileRecv\MobileFile\Image\6B7BQV80Z~0EWDSIJ0Y6X34.png)

### 2.2C++代码的编译方法

#### g++编译代码

![image-20231116145733143](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20231116145733143.png)

连接：引用第三方文件（包括动态libxx.so和静态libxx.o）

GCC(工具集)分为gcc（纯C或者混合C和C++项目）和g++（纯C++项目）

#### make编译代码

##### makefile文件：

1 start:

2     g++ -o foo.o -c foo.cpp

3     g++ -o main.o -c main.cpp

4     g++ -o demo foo.o main.o

5 clean:

6     rm -rf foo.o main.o

#### CMake编译代码

##### CMakeList.txt文件

1 cmake_minimum_required (VERSION 2.8)

2 project(demo)

3 

4 include_directories("${PROJECT_BINARY_DIR}")

5

 6 add_library(foo foo.cpp)

7 add_executable (demo main.cpp)

8 target_link_libraries (demo foo)

(Cmake->makefile->make)

### 2.3C++编程风格指南

![image-20231116152947846](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20231116152947846.png)

C++链接知识------Cnotebook