# proj - RV64N on NutShell



### 项目描述

RISC-V 指令集是一种新兴的、开放的指令集体系结构，它的一大特点是模块化与增量型。基金会定期商讨并提供一系列标准化的指令集 “扩展”（extension），如浮点扩展、向量扩展等。根据应用程序的需要，实际的硬件可以包含或不包含这些扩展，这使得开发者不必背负沉重的历史包袱。

在特权级方面，RISC-V 基金会提供了 N 扩展的技术草案，尽管其 Spec 尚未被确定并正式发布，但其中的一些设计是十分吸引人的，给 OS 开发者带来了不一样的思考。

N 扩展规定了用户态特权级的一系列实现规范，主要支持了用户态处理中断、异常的机制

我们的目标是在果壳处理器上实践用户态中断。在硬件方面，在一生一芯计划果壳处理器（NutShell）上实现 N 扩展的全部逻辑；在软件方面，修改操作系统，在硬件机制的帮助下利用用户态中断完成一系列功能。



### 所属赛道

2021全国大学生操作系统比赛的“OS功能设计”赛道



### 参赛要求

- 以小组为单位参赛，最多三人一个小组，且小组成员是来自同一所高校的本科生（2021年春季学期或之后本科毕业的大一~大四的学生）
- 如学生参加了多个项目，参赛学生选择一个自己参加的项目参与评奖
- 请遵循“2021全国大学生操作系统比赛”的章程和技术方案要求



### 项目导师

xxx



### 难度

xxx



### 特征

- 兼容 RISC-V Privileged 规范 v1.11 版本，可在此基础上进行功能扩增
- 在果壳处理器（NutShell）上进行适配
- 硬件使用Chisel语言实现，软件不限



### 文档

[RISC-V "N"扩展技术草案](http://www.five-embeddev.com/riscv-isa-manual/latest/n.html)

[一生一芯项目](https://github.com/OSCPU) 及 [果壳处理器文档](https://oscpu.github.io/NutShell-doc/)



## 预期目标



### 软硬件结合实现用户态中断

* 自主选择操作系统，可以使用已经适配果壳的操作系统（如Linux，xv6等），也鼓励将其他开源/教学操作系统移植到果壳上
* 阅读与理解果壳处理器的设计与RISC-V手册特权级部分，修改硬件代码实现对用户态中断的支持（N extension），并设计测试程序验证实现的正确性

* 使用用户态中断实现所选操作系统的部分职能，可以探索的方向包括但不限于：
  * 用户态异常处理（如整数指令溢出、浮点异常等）
  * 用户态信号（Signal）处理
  * 用户态特权级支持下的异步垃圾回收机制
  * 用户态中断在计算机安全领域的应用

* 可以结合实际需求，在 N 扩展的框架下自主设计新的 CSR 寄存器及其相应的功能
* 撰写文档分析用户态中断在所选择的 OS 上体现出的设计与性能的优势，总结其对操作系统设计的启发意义
* 鼓励同学探索用户态中断的更多使用场景

