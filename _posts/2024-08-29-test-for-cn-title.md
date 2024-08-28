---
layout: post
title: 测试中文Title
date: 2024-08-28 23:50:00 +0800
description: this is what included images could look like
tags: formatting images
categories: sample-posts
thumbnail: assets/img/mdj.jpg
---

1. 如遇到title为中文->取文件名
2. 路径取date的时间，与文件名无关
<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/mdj.jpg" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/mdj-cat.jpg" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    止疼：美达佳 120元；利尿：沙斯多芬利尿通胶囊8*14 112元
</div>
