---
date: 2021-02-02T11:08:01+08:00
title: "【单词卡】设计规划"
tags: ["设计规划", "个人项目"]
draft: false
keywords:
- flashcard
- 单词卡
description : "单词卡（flashcard）设计规划"
---


## 前言
这就是个单词卡（flashcard），写来记单词的。本篇博文用来记录一些大纲。  
[灵感来自](https://www.youtube.com/watch?v=V-N5x5PI4hs&list=PLknTIh1tGz_7sLcoL2tXLojR5ZA9SKC72&index=1)

<!--more-->

## 复习算法

{{< mermaid loadMermaidJS="true" >}}
graph LR
    START((开始)) --> A
    A{记忆成功} -->|Y| B
    A{记忆成功} -->|N| C
    B[熟练度增加] --> D
    C[熟练度减少] --> D
    D[调整冷却时间] --> END((结束))
{{< /mermaid >}}


## 关于冷却
每当你进行一个复习后，该单词都会进入冷却；冷却期的单词，即便连续地完成复习也不会增加熟练度。这是为了让你长期反复去记忆它，达到长期记忆的目的。冷却时间根据单词熟练度及复习结果而异，具体如下：
- 记忆失败（熟练度`下降`一级）
  1. 冷却时间增加1小时
- 记忆成功（熟练度`上升`一级）
  1. 一级熟练度：冷却时间增加1小时
  2. 二级熟练度：冷却时间增加1天
  3. 三级熟练度：冷却时间增加1周
  4. 四级熟练度：冷却时间增加1月

连续成功四次，一般来说就是记住了。