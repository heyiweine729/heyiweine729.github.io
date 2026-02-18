---
title: "CS50 学习日志：Week 6 - Python"
date: 2026-02-18T21:35:00+08:00
draft: false
author: "Sanjin"
summary: "从 C 语言的手动挡切换到 Python 的自动挡。体验不再需要管理内存的快乐，掌握列表、字典与模块化编程。"
tags: ["CS50", "Python", "Migration"]
categories: ["Study Logs"]
---

# CS50 学习日志：Week 6 - Python

> 学习进度：已完成
> 关键主题：函数、模块、包、高级语法

---

## 🐍 核心概览：从手动挡到自动挡
*状态：已掌握*

如果说前几周的 C 语言是在驾驶一辆手动挡的老爷车（需要关注每一个齿轮和离合器），那么 Week 6 的 Python 就像是换到了自动挡的特斯拉。

同样的逻辑，代码量却减少了一半以上。我们不再需要管理内存 (`malloc`/`free`)，也不需要声明变量类型 (`int`, `char`)，Python 处理了一切底层细节。

### 🔑 关键概念 (Key Concepts)

1.  **Python 基础语法**
    * **Variables (变量)**: 动态类型，不需要提前声明。
    * **Functions, Arguments, Return Values (函数与参数)**: 使用 `def` 关键字，代码块通过缩进来定义，而不是大括号 `{}`。
    * **Boolean Expressions & Conditionals (布尔与条件)**: `if`, `elif`, `else`，逻辑更加接近自然语言。
    * **Loops (循环)**: `for` 循环变得极其优雅，特别是在遍历列表时。

2.  **Modules & Packages (模块与包)**
    * 这是 Python 最大的威力所在。通过 `import`，我们可以使用庞大的第三方库生态系统。
    * 不再需要从零开始写链表或哈希表，Python 的 `list` 和 `dict` 内置了这些功能，且性能经过了高度优化。

---

## 📺 补充学习资源 (Shorts)
*来源：Week 6 课程资料*

这一周的 Shorts 视频相对精简，因为讲座本身已经涵盖了大量的实战演示：

* **Python**: 全面介绍 Python 语言特性的核心视频，对比 C 语言的语法差异，帮助快速迁移思维模式。