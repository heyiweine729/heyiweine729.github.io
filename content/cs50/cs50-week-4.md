---
title: "CS50 学习日志：Week 4 - 内存与指针 (Memory)"
date: 2026-02-18T21:25:00+08:00
draft: false
author: "Sanjin"
summary: "深入 C 语言最危险的领域：内存与指针。掌握十六进制、栈与堆的区别，以及手动管理内存的艺术。"
tags: ["CS50", "C", "Pointers", "Memory Management"]
categories: ["Study Logs"]
---

# CS50 学习日志：Week 4 - 内存与指针 (Memory)

> 学习进度：已完成
> 关键主题：指针、十六进制、内存管理、文件 I/O

---

## 🧠 核心概览：揭开内存的盖子
*状态：已掌握（虽然掉了很多头发）*

这一周，我们深入到了 C 语言最强大但也最危险的领域：**内存 (Memory)**。

我们不再通过变量名来间接访问数据，而是通过**指针 (Pointers)** 直接访问数据所在的物理地址。这一章让我明白了为什么有些程序会崩溃（Segmentation Fault），以及为什么计算机会有安全漏洞（Buffer Overflow）。

### 🔑 关键概念 (Key Concepts)

1.  **Hexadecimal (十六进制)**
    * 学习了用 `0x` 开头的 16 进制数来表示内存地址。相比于二进制，它是更紧凑的表达方式。

2.  **Pointers (指针)**
    * `int *p`: 一个存储了另一个变量**地址**的变量。
    * `&` (取地址) 和 `*` (解引用) 是这一周最常用的两个运算符。

3.  **Memory Management (内存管理)**
    * **Stack (栈)**: 用于存储函数内的局部变量，自动分配和释放。
    * **Heap (堆)**: 用于**动态内存分配 (Dynamic Memory Allocation)**。
    * **malloc & free**: 我必须手动申请内存 (`malloc`)，并且一定要记得手动释放 (`free`)，否则就会导致**内存泄漏 (Memory Leak)**。

4.  **File I/O & Images (文件与图像)**
    * 数据在磁盘上只是一堆字节。通过操作这些字节，我们可以实现图像滤镜（如模糊、灰度化）甚至恢复被删除的照片。

---

## 📺 补充学习资源 (Shorts)
*来源：Week 4 课程资料*

由于指针的概念非常抽象，Shorts 视频通过可视化的方式帮助我建立了心理模型：

* **Hexadecimal (十六进制)**: 理解内存地址的计数系统。
* **Pointers (指针)**: 核心概念的动画演示。
* **Defining Custom Types (自定义类型)**: 使用 `typedef` 简化代码。
* **Dynamic Memory Allocation (动态内存分配)**: 详解 `malloc` 的使用场景。
* **Call Stacks (调用栈)**: 理解函数调用时内存是如何层叠的。
* **File Pointers (文件指针)**: 如何读取和写入文件 (`fopen`, `fclose`)。