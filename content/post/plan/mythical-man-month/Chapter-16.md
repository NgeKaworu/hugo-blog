---
date: 2020-10-30T05:01:14+08:00
title: "【人月神话】章节16 阅读笔记"
draft: false
tags: ["设计规划"]
keywords:
- "人月神话"
- "项目管理"
- "没有银弹"
description : "本章从软件工程的根本和次要问题出发，论述了为什么软件工程没有银弹。"
---

没有任何技术或管理上的进展，能够独立地许诺十年内使生产率、可靠性或简洁性获得数量级上的进步。   

> There is no single development, in either technology or management technique, which by itselfpromises even one order-of-magnitude improvement within a decade in productivity, in eliability,in simplicity. 

硬件提高的性能，很快被软件消耗掉了  
-- 安迪比尔定理

> Andy gives, Bill takes away.  
> -- Andy and Bill’s Law  


集成电路上可容纳的晶体管数目，约每隔两年便会增加一倍  
-- 摩尔定律  

> number of transistors on a given chip can be doubled every two years  
> -- Moore's Law  


<!--more-->

本章从软件工程的根本和次要问题出发，论述了为什么软件工程天生没有银弹。

## 根本问题
### 复杂度
规模上，软件实体可能比任何由人类创造的其他实体要复杂，因为没有任何两个软件部分是相同的（至少是在语句的级别）。如果有相同的情况，我们会把它们合并成供调用的子函数。  
复杂度带来的问题
1. 团队成员之间的沟通非常困难，导致了产品瑕疵、成本超支和进度延迟；
2. 列举和理解所有可能的状态十分困难，影响了产品的可靠性；
3. 由于 **函数的** 复杂度，函数调用变得困难，导致程序难以使用；由于结构性复杂度，程序难以在不产生副作用的情况下用新函数扩充；
4. 由于 **结构性** 复杂度，造成很多安全机制状态上的不可见性。
5. 复杂度不仅仅导致技术上的困难，还引发了很多管理上的问题。
6. 它使全面理解问题变得困难，从而妨碍了概念上的完整性；
7. 它使所有离散出口难以寻找和控制；它引起了大量学习和理解上的负担，使开发慢慢演变成了一场灾难。


### 一致性
必须控制很多来自 **必须遵循的** 、 **人为惯例的** 、 **系统的** 、 **随心所欲的** 、 **毫无规则可言的**且 **无法简化的** 复杂度。它们随接口的不同而改变，随时间的推移而变化，而且，这些变化不是必需的。

### 可变性
简言之，软件产品扎根于文化的母体中，如各种应用、用户、自然及社会规律、计算机硬件等等。后者持续不断地变化着，这些变化无情地强迫着软件随之变化。

### 不可见性
软件的客观存在不具有空间的形体特征。

## 次要问题上的突破
次要问题是指出现在目前生产上的，但并非那些与生俱来的困难。主要是 **业务**。

### 高级语言
勿庸置疑，软件生产率、可靠性和简洁性上最有力的突破是使用高级语言编程。大多数观察者相信开发生产率至少提高了五倍，同时可靠性、简洁性和理解程度也大为提高。
> 然而，对于较少使用那些复杂深奥语言要素的用户，高级语言在某种程度上增加而不是减少了脑力劳动上的负担。

### 分时
分时解决了完全不同的困难。分时保证了及时性，从而使我们能维持对复杂程度的一个总体把握。
> 批处理编程的较长周转时间意味着 **不可避免会遗忘一些细枝末节** ，如果我们停下编程，调用编译程序或者执行程序，思维上的中断使我们不得不重新进行思考， **它在时间上的代价非常高昂。最严重的结果可能是失去对复杂系统的掌握** 。  

> 分时所起作用也非常有限。主要效果是缩短了系统的响应时间。随着它接近于零，到达人类可以辨识的基本能力——大概 100 毫秒时，所获得的好处就接近于无了。

### 统一编程环境
第一个集成开发环境——Unix 和 Interlisp 现在已经得到了广泛应用，并且使生产率提高了 5 倍。为什么？  


下面讲了一些概念性的东西
## “希望”

### 高级编程语言
这类语言出现最大的回报来自出现时的冲击，它通过使用更加抽象的语句来开发，降低了机器的次要复杂度

### 面向对象编程
仅仅能消除所有设计表达上的次要困难。软件的内在问题是设计的复杂度，上述方法并没有对它有任何的促进。

### 人工智能
这里的人工智能分两种：
1. 真正意义上的（目前还处于人工智障阶段的）
2. 辅助编程的，IDE已经实现了

### 专家系统
专家系统是包含归纳推论引擎和规则基础的程序，它接收输入数据和假设条件，通过从基础规则推导逻辑结果，提出结论和建议，向用户展示前因后果，并解释最终的结果。推论引擎除了处理推理逻辑以外，通常还包括复杂逻辑或者概率数据和规则。
> IDE已经实现了初级范畴功能

### “自动”编程
> IDE实现了代码补全

### 图形化编程
> 这几乎不可能

### 程序验证
编译器，静态语言，编译时验证，诸如此类。

### 环境和工具
docker、统一IDE、基础库、通用库等等...

### 工作站
软件不足，硬件来凑
> 我们当然欢迎更加强大的工作站，但是不能期望有魔术般的提高。


## 针对概念上根本问题的颇具前途的方法
虽然现在软件上没有技术上的突破能够预示我们可以取得像在硬件领域上一样的进展，但在现实的软件领域中，既有大量优秀的工作，也有不引人注意的平稳进步。  

所有针对软件开发过程中次要困难的技术工作基本上能表达成以下的生产率公式：  

{{< math >}}
\begin{matrix}
任务时间 = \sum{（频率）}_i × {（时间）}_i 
\end{matrix}
{{< /math >}}

下面是提出的一些方法  
1. 购买和自行开发。
> 构建软件最可能的彻底解决方案是不开发任何软件。  
> 其实就是不重复造轮子，用开源的或者商业解决方案。
2. 需求精炼和快速原型
> 事实上，客户不知道他们自己需要什么。他们通常不知道哪些问题是必须回答的。并且，连必须确定的问题细节常常根本不予考虑，甚至只是简单地回答——“开发一个类似于我们已有的手工处理过程的新软件系统”
原型能帮助用户精炼需求
3. 增量开发——增长，而非搭建系统。
> 微服、模块化就是这类的实践
4. 卓越的设计人员。  
关键的问题是如何提高软件行业的核心，一如既往的是——人员。

培养人才显而易见的步骤
- 尽可能早地、有系统地识别顶级的设计人员。最好的通常不是那些最有经验的人员。
- 为设计人员指派一位职业导师，负责他们技术方面的成长，仔细地为他们规划职业生涯。
- 为每个方面制订和维护一份职业计划，包括与设计大师的、经过仔细挑选的学习过程、正式的高级教育和以及短期的课程——所有这些都穿插在设计和技术领导能力的培养安排中。
- 为成长中的设计人员提供相互交流和学习的机会。

## 17章
17章其实是本章的补充，距上一章发布就是过去了9年，而至今也差不多40年了。  

而上章论述的问题依旧存在。

放在这里是因为17章没有什么新的东西，只是用资料总结和强调了本章的观点