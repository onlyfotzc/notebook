---
layout: post
title: a post with images
date: 2024-08-28 21:01:00 +0800
description: this is what included images could look like
tags: formatting images
categories: sample-posts
thumbnail: assets/img/mdj.jpg
---

时隔一年，再一次被诊断为尿道感染，开了两种药，一种是利尿的，一种是止疼的.
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
