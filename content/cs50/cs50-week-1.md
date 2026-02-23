---
title: "CS50 学习日志：Week 1 - C 语言与计算机基础"
date: 2026-02-18T16:00:00+08:00  # 自动生成的，如果没有请保留格式
draft: false                     # 必须改成 false 才能发布
author: "Sanjin"

# 这是一个很棒的功能，会显示在首页预览卡片上
summary: "告别 Scratch，进入 C 语言的世界。探索编译器、命令行、内存溢出以及计算机的底层思考逻辑。"

tags: ["CS50", "C", "计算机基础", "ZJU"]
categories: ["Study Logs"]

# (可选) 如果你想让文章顶部显示一张图，可以以后再配置 cover
# cover:
#     image: "" 
#     alt: "CS50 Header"
---
# CS50 学习日志：Week 1 - C 语言与计算机基础

> 学习进度：已完成
> 关键主题：编译器、命令行、基础语法、内存溢出

---

## 💻 核心概览：Hello, C World
*状态：已掌握*

告别了 Week 0 的 Scratch 积木块，Week 1 带我进入了真正的代码世界。虽然 **C 语言** 看起来古老且严苛，但它是理解计算机如何“思考”的基石。

正如课程所强调的，这一周不仅是学习语法，更是关于 **正确性 (Correctness)**、**设计 (Design)** 和 **代码风格 (Style)** 的一种修行 [1]。

### 🔑 关键概念 (Key Concepts)

在这一章中，我深入接触了计算机科学最底层的逻辑：

1.  **从源代码到机器码 (Source Code to Machine Code)**
    *   理解了 **编译器 (Compiler)** 的作用：将人类可读的代码转换为计算机可执行的二进制指令 (0和1) [1]。
2.  **开发环境与工具**
    *   开始使用 **Visual Studio Code** 和 **Linux** 命令行。
    *   学习了 **CLI (命令行界面)** 的基础操作，不再依赖鼠标，而是通过命令与系统对话 [1]。
3.  **C 语言基础语法**
    *   **变量与类型 (Variables & Types)**: 必须明确告诉计算机每个数据是什么类型（如 `int`, `float`, `char` 等）[1]。
    *   **头文件与库 (Header Files & Libraries)**: 学会了如何引入标准库（如 `<stdio.h>`）来使用现成的功能 [1]。
    *   **循环与条件 (Loops & Conditionals)**: 控制程序的逻辑流。
4.  **计算机的局限性**
    *   **整数溢出 (Integer Overflow)**: 当数字超过计算机存储上限时会发生什么？
    *   **浮点数精度问题 (Floating-Point Imprecision)**: 计算机在处理小数时并不总是完美的 [1]。

---

## 📺 补充学习资源 (Shorts)
*来源：Week 1 课程资料*

讲座搭建了骨架，而 Shorts 视频填充了具体的血肉。特别是以下几个短视频对我理解 C 语言的细节非常有帮助 [2]：

*   **Data Types (数据类型)**: 深入理解不同类型占用的内存大小。
*   **Operators (运算符)**: 处理算术和逻辑运算。
*   **Conditional Statements (条件语句)**: `if`, `else`, `switch` 的用法。
*   **Loops (循环)**: `for`, `while`, `do-while` 的区别。
*   **Command Line (命令行)**: 如何在终端中高效操作。
*   **Magic Numbers (魔术数字)**: 为什么我们要避免在代码中直接使用不明意义的数字。
---
[[cnote]]