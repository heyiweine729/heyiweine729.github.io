---
title: "CS50 学习日志：Week 5 - 数据结构 (Data Structures)"
date: 2026-02-18T21:30:00+08:00
draft: false
author: "Sanjin"
summary: "从队列到栈，从链表到哈希表。用指针和结构体亲手构建现代编程语言的基石。"
tags: ["CS50", "Data Structures", "Linked List", "Hash Table"]
categories: ["Study Logs"]
---

# CS50 学习日志：Week 5 - 数据结构 (Data Structures)

> 学习进度：已完成
> 关键主题：链表、树、哈希表、栈与队列

---

## 🏗️ 核心概览：自己动手构建内存结构
*状态：已掌握*

如果说 Week 2 的数组是现成的乐高底板，那么 Week 5 就是用散乱的积木块（内存节点）自己搭建结构。

我学会了利用 `struct` 和指针来创建**抽象数据类型 (Abstract Data Types)**。虽然在 C 语言中实现这些结构需要写大量的辅助代码（分配节点、连接指针），但它们是理解现代编程语言底层原理的关键。

### 🔑 关键概念 (Key Concepts)

1.  **Queues & Stacks (队列与栈)**
    * **Queues**: 先进先出 (FIFO) 的结构，像排队买票。
    * **Stacks**: 后进先出 (LIFO) 的结构，像叠盘子或浏览器的“后退”功能。

2.  **Linked Lists (链表)**
    * **Singly-Linked Lists (单向链表)**: 解决了数组大小固定的问题。每个节点包含数据和指向下一个节点的指针。虽然插入数据很快，但查找数据变成了 $O(n)$。
    * **Doubly-Linked Lists (双向链表)**: 允许向前和向后遍历，但每个节点需要更多的内存来存储额外的指针。

3.  **Trees (树)**
    * **Binary Search Trees (二叉搜索树)**: 将链表的灵活性与二分查找的高效性结合起来。通过保持“左小右大”的规则，查找速度可以达到 $O(\log n)$。

4.  **Hash Tables (哈希表)**
    * 这是数组和链表的终极结合体。
    * 通过**哈希函数**将数据映射到数组索引上，实现了接近 $O(1)$ 的瞬间查找速度。这是很多现代数据库索引的基础。

5.  **Tries (字典树/前缀树)**
    * 一种专门用于处理字符串的树形结构。查找一个单词的时间只取决于单词的长度，而与数据总量无关。

---

## 📺 补充学习资源 (Shorts)
*来源：Week 5 课程资料*

这一周的 Shorts 视频是理解复杂结构可视化的关键，特别是链表的指针操作非常容易出错：

* **Data Structures**: 宏观概述。
* **Structures**: 如何在 C 语言中定义 `struct`。
* **Singly-Linked Lists**: 单向链表的插入与删除操作。
* **Doubly-Linked Lists**: 双向指针的操作细节。
* **Hash Tables**: 哈希函数的设计与冲突解决。
* **Tries**: 字典树的构建过程。
* **Queues & Stacks**: 两种基础 ADT 的实现逻辑。