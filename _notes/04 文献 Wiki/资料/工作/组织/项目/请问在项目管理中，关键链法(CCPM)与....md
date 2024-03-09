---
title: 请问在项目管理中，关键链法(CCPM)与...
date created: 2024-03-09
date modified: 2024-03-09
tags:
---


[www.zhihu.com](https://www.zhihu.com/question/27587884)安安莉波波 关注

回答这三个问题之前，想提出一个问题：你有没有读过《[关键链](https://www.zhihu.com/search?q=%E5%85%B3%E9%94%AE%E9%93%BE&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A70818049%7D)》这本书？读了几遍？你的问题的答案在《关键链》这本书里都可以找到。

以下是我对你的问题的“简要”回答，要深刻理解，最好还是研读《关键链》。

1，请简要介绍二者的定义；

CCPM: Critical Chain Project Management，[关键链项目管理](https://www.zhihu.com/search?q=%E5%85%B3%E9%94%AE%E9%93%BE%E9%A1%B9%E7%9B%AE%E7%AE%A1%E7%90%86&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A70818049%7D)，CCPM不是方法，那个“M”不是Method，它是一种项目管理思维方式，是TOC(Theory of Constraint)思想在项目管理领域的一种在思想层面上的实现，开辟了项目管理思维的另一个领域，不同的项目管理领域还有[敏捷项目管理](https://www.zhihu.com/search?q=%E6%95%8F%E6%8D%B7%E9%A1%B9%E7%9B%AE%E7%AE%A1%E7%90%86&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A70818049%7D)，其“实施方法”如Scrum，但Scrum我认为不是[项目管理思维](https://www.zhihu.com/search?q=%E9%A1%B9%E7%9B%AE%E7%AE%A1%E7%90%86%E6%80%9D%E7%BB%B4&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A70818049%7D)，只是定义了一种敏捷项目管理的一个框架（Framework），若非要问CCPM使用什么方法管理项目，可以说它坚持了TOC的“五步骤”思想的方式，一切以寻找“约束”为出发点，聚焦在“约束”所在的那条最长的任务序列即是“关键链”；

CPM：Critical Path Method，[关键路径](https://www.zhihu.com/search?q=%E5%85%B3%E9%94%AE%E8%B7%AF%E5%BE%84&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A70818049%7D)（线）方法，注意这里的“M”才是Method，是在CCPM和敏捷项目管理未出现之前的一种项目管理的方法（或工具）。一般（传统）来讲，凡采用CPM管理项目的方法被称为传统[项目管理方法](https://www.zhihu.com/search?q=%E9%A1%B9%E7%9B%AE%E7%AE%A1%E7%90%86%E6%96%B9%E6%B3%95&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A70818049%7D)。CCPM的出现就是专门解决传统项目管理中问题的。Critical Path即是那条用时间计算的最长的一串任务序列，其定义就与CCPM不同，CCPM考虑的是“资源”依赖或冲突，而Critical Path只说时间。

2，请问导致关键链与关键路径在排程中不统一的根本原因是什么？为何会产生这样的现象？

第一问你问的应该是：相同的项目，两者的排程（“[项目计划](https://www.zhihu.com/search?q=%E9%A1%B9%E7%9B%AE%E8%AE%A1%E5%88%92&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A70818049%7D)”）为什么会不一样？

首先你应该了解为什么CCPM会出现？CCPM的出现就是为了解决采用CPM的传统项目管理中出现的问题，而采用CPM的传统项目管理有哪些问题呢？我简单罗列一下，你最好还是温习一下《关键链》这本书，然后自己再结合实际总结：

a. CPM把安全时间放在每个任务的末尾，仅保护单一任务的按时完成；

b. 任何单一任务的提前完成对项目（具体说是对后一个任务的启动）没有帮助，因为后一个任务的资源可能没有到位，因为下面h点；

c. CPM提倡任务早开始，容易出现“学生拖延症”和“[帕金森定律](https://www.zhihu.com/search?q=%E5%B8%95%E9%87%91%E6%A3%AE%E5%AE%9A%E5%BE%8B&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A70818049%7D)”，容易把安全时间浪费掉和间隙吃掉；

d. CPM没有考虑资源（人）的依赖关系，容易出现资源（人）冲突或造成多任务并行；

e. CPM有对单一任务的风险意识，但对整个项目的风险意识薄弱，往往整个项目的完成概率受最后一个任务的完成概率影响；

f. CPM只监控和衡量关键路径的任务进度，对[非关键路径](https://www.zhihu.com/search?q=%E9%9D%9E%E5%85%B3%E9%94%AE%E8%B7%AF%E5%BE%84&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A70818049%7D)的任务关注度不够，造成项目经理的关注点在项目层面上出现分散；

g. CPM的项目进度衡量方法不够准确，导致对项目进度状态的把控不对；

h. 因为里程碑的存在，CPM关注每个任务的按时完成，而弱化了对整个项目的关注，如同[e点](https://www.zhihu.com/search?q=e%E7%82%B9&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A70818049%7D)；

i. CPM没有考虑人性（懒惰的一面），认为时间的充裕对任务的按时完成是正影响；

j. 未做资源（人）的计划，假设资源（人）是无限提供的，随叫随到；

k. CPM的项目只在项目开始或发生变化时做估算。

CPM中其实可以说是没有Buffer（缓冲）概念，确切地应该称之为安全时间，仅仅是时间维度，你可能会说，CPM的项目也听人说“Buffer”呀，是的，那我再严谨一些，CPM中所说的的Buffer和CCPM中的Buffer不一样，想想CPM中就没有Project Buffer和Resource Buffer。

因为关键链解决了以上问题，所以排程自然就会不一样。

第二问的答案应该说已经很明显了。为什么会产生这个现象，用TOC的语言说，就是CCPM让项目经理更加聚焦到整个项目的进度，而非单一任务，更符合对项目经理对整个项目把控的[全局观](https://www.zhihu.com/search?q=%E5%85%A8%E5%B1%80%E8%A7%82&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A70818049%7D)的要求。

3，请问CCPM实践中收集、分配Project Buffer和Feeding Buffer的[具体原则](https://www.zhihu.com/search?q=%E5%85%B7%E4%BD%93%E5%8E%9F%E5%88%99&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A70818049%7D)有哪些？

你的问题好像在问PB和FB的[时间长度](https://www.zhihu.com/search?q=%E6%97%B6%E9%97%B4%E9%95%BF%E5%BA%A6&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A70818049%7D)应该用什么方法计算是吧？

我采用过的计算方法有三种：

第一种：1/2法 （这种方法最简单）

一个项目包含两个任务的估算分别是：第一个任务6天（工作时间＋安全时间），第二个任务14天，那么，Buffer就是(6+14)/2/2=5天，(6+14)/2是按安全时间占任务总估算时间的1/2的概念算出总安全时间，再/2得到Buffer时间，这个项目的[计划工期](https://www.zhihu.com/search?q=%E8%AE%A1%E5%88%92%E5%B7%A5%E6%9C%9F&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A70818049%7D)就是3（＝6/2，第一个任务的工作时间）＋7天（＝14/2，第二个任务的工作时间）＋5天（Buffer）=15天。

第二种：[标准方差法](https://www.zhihu.com/search?q=%E6%A0%87%E5%87%86%E6%96%B9%E5%B7%AE%E6%B3%95&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A70818049%7D)（这种方法更科学）

一个项目包含两个任务的估算分别是：第一个任务6天（[工作时间](https://www.zhihu.com/search?q=%E5%B7%A5%E4%BD%9C%E6%97%B6%E9%97%B4&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A70818049%7D)＋安全时间），第二个任务14天，那么，Buffer就是SQRT{ \[ (6/2)^2 + (14/2)^2 \] /2 }~=5.4天（按6天算），^2是求平方，SQRT是求[开方](https://www.zhihu.com/search?q=%E5%BC%80%E6%96%B9&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A70818049%7D)，这个项目的计划工期就是3天（＝6/2，第一个任务的工作时间）＋7天（＝14/2，第二个任务的工作时间）＋6天（Buffer）=16天。

第三种：[概率法](https://www.zhihu.com/search?q=%E6%A6%82%E7%8E%87%E6%B3%95&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A70818049%7D)（这种方法应该更准确些，是对第一种方法的改进，对第二种方法的简化，我现在使用的就是这种）

这种方法要求视给出的估算时间完成任务的概率多少来确定Buffer和安全时间的关系，同时还要考虑你要求项目的完成概率。

根据《关键链》中任务完成概率和使用时间的关系（完成任务90%的概率用3倍的工作时间，完成80%用2倍的工作时间，完成50%用1倍的工作时间），先用估算时间和完成概率推算出工作时间，再根据你要求项目完成的[概率计算](https://www.zhihu.com/search?q=%E6%A6%82%E7%8E%87%E8%AE%A1%E7%AE%97&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A70818049%7D)出安全时间（即Buffer）。

比如说，一个项目包含一个任务，15天完成的概率是90%，那么工作时间就是15/3=5天，如果你要求这个项目完成概率控制在80%左右，那么Buffer＝5天，如果你要求的概率是90%左右，那么Buffer = 5 x 2 = 10天。

那么处理上面例子就是：

一个项目包含两个任务的估算分别是：第一个任务6天（工作时间＋安全时间，完成概率90%），第二个任务14天（完成概率80%），而你要求这个项目完成概率控制在80%左右，Buffer就是6/3+14/2=9，这个项目的计划工期就是2天（＝6/3，第一个任务的工作时间）＋7天（＝14/2，第二个任务的工作时间）＋9天（Buffer）=18天。如果你想更科学一些，就用第二种方法在这个推算出来的安全时间的基础上计算。

别忘记TOC“五步骤”的最后一步：实现持续增长的回到第一步。为什么呢？因为根据CCPM多个项目的完成，消耗Buffer的位置不同，可能会影响你对Buffer的[计算参数](https://www.zhihu.com/search?q=%E8%AE%A1%E7%AE%97%E5%8F%82%E6%95%B0&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A70818049%7D)，这有可能是由估算的不准确性造成的。

————————————————————

2017/7/27更新

以上是从两种项目管理的具体方法上进行了比较分析，以下则从思想角度的不同再做一点补充：

CCPM是TOC思想在项目管理领域中的应用，但其核心思想仍然继承了TOC思想的核心：那就是“聚焦”（Focus）。但项目要聚焦什么呢？

应该知道，项目有时间、范围、资源、成本等主要方面。可以将这些方面看作完成一个项目的不同环节，哪一个环节在某个时刻表现的弱了，那么就应该关注这个方面，然后让指导[项目经理](https://www.zhihu.com/search?q=%E9%A1%B9%E7%9B%AE%E7%BB%8F%E7%90%86&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A70818049%7D)的工作聚焦到这个方面。这个表现最弱的方面也就是TOC提出的“瓶颈”（制约）。

而“在一个系统（这里就指项目）中瓶颈是会转移的：有时瓶颈在时间方面，此时工期可能显得紧张；有时瓶颈在资源方面，此时人力可能显得紧张等等。那么这些紧张的瓶颈最终会在CCPM的[缓冲消耗](https://www.zhihu.com/search?q=%E7%BC%93%E5%86%B2%E6%B6%88%E8%80%97&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A70818049%7D)中表现出来。如此，当缓冲消耗出现快速消耗趋势的时候，就会引导项目经理去关注项目的几个方面，让这个瓶颈跳出来，然后对瓶颈进行处理，从而达到项目在全局上获得最大利益。

TOC还有一个指导原则：做应该做的事情，不做不应该做的事情。那么当瓶颈在时间方面时，项目经理应该关注项目的工期，做了应该做的事情，不应该关注项目的资源，没做不应该做的事情；当瓶颈转移到资源方面时，项目经理应该关注项目的资源，做了应该做的事情，不应该关注项目的时间，没做不应该做的事情。

而CPM让项目经理只关注了项目的时间方面——工期，即在关键路径上的进度。所以当瓶颈在时间方面时还好，但当瓶颈转移到了资源方面时，CPM的项目经理仍然关注在项目的时间方面，做了不应该做得事情，自然对项目的全局利益表现贡献不会太多。

CCPM就好像中国古代的“权变”之道，应该在变化的环境中权衡，解决方案也受权衡的结果进行调整。而CPM并没有这么做。

这也就是CCPM比CPM优势明显的地方之一。

[跳转到 Cubox 查看](https://cubox.pro/my/card?id=7098275290157155543)