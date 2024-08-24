---
layout: post
title: Intranet File Synchronization Solution
date: 2024-08-24 21:02:13
description: 实现一种基于ubuntu系统的内网文件同步系统方案思路
tags: ubuntu,tech
categories: inspiration,project

toc:
  - name: 背景
    # if a section has subsections, you can add them as follows:
    # subsections:
    #   - name: Example Child Subsection 1
    #   - name: Example Child Subsection 2
  - name: 思路
  - name: 实现
  - name: 验证
---

实验室电脑全部都是Ubuntu系统，每台电脑由各自负责的同学负责，导致每台执行服务器的文件存储路径完全不一致，对于新手来说会导致文件找不到体验非常不好。



#### 目录

- 背景
- 思路
- 实现 
- 验证
## 背景
实验室电脑多，但每台执行器角色的服务器目前都是由个人自行管理，导致每台电脑的测试工具存储目录各有不同，新手或是其他人无法知道别人的测试工具存储目录，另外，测试工具也是个人手动从服务器下载。
需要有一种方案，能够让执行服务器能够自动从服务器同步最新的测试工具，并且存放到执行服务器的指定目录，实现测试工具自动同步，统一存储的场景

## 思路
1.使用Jenkins master slaver方案，搭建一台Jenkins服务器充分master角色，实验室内其他执行服务器充分slaver角色。可以通过人工或是定时的方式启动测试工具文件同步方案，实现执行服务器中的测试工具文件与中心服务器的测试工具文件保存一致，且执行服务器中的测试工具文件存储路径一致。
## 实现
#### 主服务器上安装Jenkins Master
1. 在主服务器上安装Jenkins Master
```bash
wget -q -O - https://pkg.jenkins.io/debian/jenkins.io.key | sudo apt-key add -
sudo sh -c 'echo deb http://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list'
sudo apt-get update
sudo apt-get install jenkins
```

2. 启动并且配置Jenkins Master
```bash
sudo systemctl start jenkins
```
3. 访问Jenkins Master的界面，通常是 http://your_ip_address:8080，按照引导完成初始化配置。
4. 在Jenkins Master中设置一个Slave：（待补充详细，暂不影响）
打开Jenkins Master的Web界面。
点击“Manage Jenkins” -> “Manage Nodes” -> “New Node”。
输入Slave名字，选择“Permanent Agent”或者“Durable Agent”。
配置Slave的CPU、内存等资源参数。
在“Usage”部分，选择“Utilize this node as much as possible”或者根据需求调整。
在“Launch method”部分，选择“Launch agent via SSH”，并提供Slave的SSH信息。
保存并开始Slave。

#### 从服务器上安装Jenkins Slaver
1. 在从服务器上安装Jenkins Slaver
```bash
wget -q -O - https://pkg.jenkins.io/debian/jenkins.io.key | sudo apt-key add -
sudo sh -c 'echo deb http://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list'
sudo apt-get update
sudo apt-get install jenkins-slave
```
2. 在Slave机器上启动Jenkins Slave
```bash
sudo java -jar /usr/share/jenkins/slave.jar
```

#### Jenkins上进行主从配置
1. 环境介绍
   Jenkins版本：
   Jenkins master/slaver节点均为Ubuntu
2. Jenkins主从配置
   ##### 新建节点
   ##### 配置节点
https://www.cnblogs.com/lcj0703/p/12268504.html
https://blog.csdn.net/hehedadaq/article/details/115584036
## 验证