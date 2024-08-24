---
layout: post
title: 内网文件同步方案
date: 2024-08-24 21:02:13
description: 实现一种基于ubuntu系统的内网文件同步系统方案思路
tags: ubuntu,tech
categories: inspiration,project
tabs: true

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
实验室电脑多，但每台执行器角色的服务器目前都是由个人自行管理，导致每台电脑的测试工具存储目录各有不同，新手或是其他人无法知道别人的测试工具存储目录，另外，测试工具也是个人手动从服务器下载，

## 思路
## 实现
## 验证

## First tabs

To add tabs, use the following syntax:

{% raw %}

```liquid
{% tabs group-name %}

{% tab group-name tab-name-1 %}

Content 1

{% endtab %}

{% tab group-name tab-name-2 %}

Content 2

{% endtab %}

{% endtabs %}
```

{% endraw %}

With this you can generate visualizations like:

{% tabs log %}

{% tab log php %}

```php
var_dump('hello');
```

{% endtab %}

{% tab log js %}

```javascript
console.log("hello");
```

{% endtab %}

{% tab log ruby %}

```javascript
pputs 'hello'
```

{% endtab %}

{% endtabs %}

## Another example

{% tabs data-struct %}

{% tab data-struct yaml %}

```yaml
hello:
  - "whatsup"
  - "hi"
```

{% endtab %}

{% tab data-struct json %}

```json
{
  "hello": ["whatsup", "hi"]
}
```

{% endtab %}

{% endtabs %}

## Tabs for something else

{% tabs something-else %}

{% tab something-else text %}

Regular text

{% endtab %}

{% tab something-else quote %}

> A quote

{% endtab %}

{% tab something-else list %}

Hipster list

- brunch
- fixie
- raybans
- messenger bag

{% endtab %}

{% endtabs %}
