---
layout: post
title: 内网文件同步方案
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
## 验证