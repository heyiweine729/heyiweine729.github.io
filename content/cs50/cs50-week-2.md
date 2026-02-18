---
title: "CS50 学习日志：Week 2 - 数组与编译背后的秘密"
date: 2026-02-18T21:17:00+08:00
draft: false
author: "Sanjin"
summary: "深入编译器的黑盒：预处理、编译、汇编、链接。探索数组、字符串与调试的艺术。"
tags: ["CS50", "C", "编译原理", "Debugging"]
categories: ["Study Logs"]
---

# CS50 学习日志：Week 2 - 数组与编译背后的秘密

> 学习进度：已完成
> 关键主题：编译管线、调试、数组、字符串、命令行参数

---

## 🛠️ 核心机制：代码是如何运行的？
*状态：已掌握*

在 Week 1，我们只是点击了“编译”按钮。在 Week 2，我深入到了这个按钮背后的黑盒，学习了源代码变成机器码的四个具体步骤。这让我对计算机的理解更加透彻。

### 🔑 关键概念 (Key Concepts)

1.  **编译的四个阶段 (The 4 Steps of Compilation)**
    * **Preprocessing (预处理)**: 处理以 `#` 开头的指令（如 `#include`），将头文件内容复制进来。
    * **Compiling (编译)**: 将 C 代码转换为汇编代码。
    * **Assembling (汇编)**: 将汇编代码转换为机器码（二进制指令）。
    * **Linking (链接)**: 将我的代码与标准库（如 `cs50.c`, `stdio.c`）的二进制文件合并，生成最终的可执行文件 [1]。

2.  **Arrays (数组)**
    * 这是我们遇到的第一个数据结构。它允许我们在内存中连续存储多个相同类型的数据。
    * **Strings (字符串)**: 在 C 语言中，字符串本质上就是字符数组 (Array of characters)。这解释了为什么处理文本比处理数字要复杂得多。

3.  **Command-Line Arguments (命令行参数)**
    * 学会了 `int main(int argc, string argv[])` 的真正含义。现在我可以写出像 Linux 命令那样接受用户输入的程序 [1]。

4.  **Debugging (调试)**
    * 不再只靠 `printf` 来找 bug，而是学会了使用调试器 (Debugger)。
    * **Step through / Step into**: 逐行执行代码，观察内存和变量的变化，这是解决逻辑错误的终极武器 [1]。

5.  **Cryptography (密码学)**
    * 课程通过加密算法的练习，展示了数组和字符操作的实际应用 [1]。

---

## 📺 补充学习资源 (Shorts)
*来源：Week 2 课程资料*

这一周的 Shorts 视频非常实用，特别是关于调试和函数作用域的部分，填补了讲座中未展开的细节：

* **Functions (函数)**: 如何模块化代码，避免重复。
* **Variables and Scope (变量与作用域)**: 局部变量 vs 全局变量，理解变量的生命周期。
* **Debugging ("Step through" & "Step into")**: 手把手教你如何使用调试工具。
* **Arrays (数组)**: 内存视角的数组存储。
* **Command Line Arguments (命令行参数)**: 处理 `argc` 和 `argv` 的实战演示 [1]。