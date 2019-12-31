## 1 概述

### 1.1 本书介绍
本书第一次明确“重构”这一概念，使之成为众多普通程序员日常开发工作中不可或缺的一部分。
本书也因此成为与《设计模式》齐名的经典著作，在世界范围内畅销不衰。

本书作者Martin Fowler 世界软件开发大师，在面向对象分析设计、UML、模式、XP和重构等领域都有卓越贡献，
现为著名软件开发咨询公司ThoughtWorks的首席科学家。

### 1.2 什么是重构
一个过程：不改变代码外在行为的前提下，对代码做出修改。
即，在代码写好之后改进它的设计。
与“设计 > 开发”相反，**在开发过程中持续不断地改进设计**

### 1.3 重构的目的
**需求的变化**使重构变得重要。如果一段代码能正常工作，并且不会再修改，也因此不需要有人理解它的工作原理，那么完全可以不去重构它。

### 1.4 本书面向的对象
专业程序员可以以一种可控、高效的方式进行重构

### 1.5 何时进行重构
* 修改已有代码，先重构使其更容易修改
* 新增代码，先可以work再不断改进

### 1.6 本书结构

* [第一章 				一个小程序进行重构的例子（重构的过程）](https://github.com/yeah31415/learning-notes/blob/master/Refactoring/Chapter1_A_Sample_of_Refactoring.md)

* [第二章 				重构的原因、重构的机遇和挑战（WHAT、WHY、WHEN）](https://github.com/yeah31415/learning-notes/blob/master/Refactoring/Chapter2_Principle_of_Refactoring.md)

* [第三章 				代码中的坏味道、如何用重构来清除（WHERE、HOW策略/解决方案)](https://github.com/yeah31415/learning-notes/blob/master/Refactoring/Chapter3_Bad_Smell_of_Code.md)

* [第四章 				重构所需的测试（单元测试）]()

* [第五章~第十二章 	**重构名录**：重构的关键手法、例子（HOW方法）](https://github.com/yeah31415/learning-notes/blob/master/Refactoring/Chapter5-12_Methods_of_Refactoring.md)

* 建议：在重构过程中时常查阅**代码中的坏味道**和**重构名录**以获得帮助。

## 2 应用与回顾

## 3 相关原则

## 4 遗留问题与参考资料
* 自动化重构工具（可靠的、不用验证的）：能够借助**语法树**来分析和重构程序代码。
  * Eclipse, IntelliJ IDEA(JAVA)
  * 语言服务器（language server)可以软件生成语法树，给单纯文本编辑器提供API

* 缺乏测试的重构手法：
  * 验证过的重构手法（Jay Bazuzi）
  * 自动化重构工具，牺牲一些重构手法

* 其他重构的学习参考资料：
  * 《重构手册》Bill Wake
  * 《数据库重构》Ambler&Sadalage《重构HTML》Harold
  * Michael Feathers《**修改代码的艺术**》如何在缺乏测试覆盖的老旧代码库上开展重构
  * 重构网站：refactoring.com
