---
title: C语言笔记
date: 2026-02-23
draft: "false"
author: Sanjin
summary: 记一下c语言的用法
tags:
  - CS50
  - C
  - 计算机基础
  - 笔记
categories:
  - Study Logs
---
## C语言数据处理
### 宏定义
```
#define pi 3.14
```
用字符串代替数字
### typedef 把一个长的变量类型名字换成短的
```
typedef unsigned char uint8_t;
uint8_t a;
```
### struct 打包不同类型的数据
```
// 定义带有标签的结构体类型，名为 MyStruct
struct MyStruct {
    char x; 
    int y; 
    float z;
};

struct MyStruct StructName; // 声明结构体变量
struct MyStruct *p;         // 声明结构体指针

StructName.x = 'A';
StructName.y = 66;
StructName.z = 1.23;

p = &StructName;            // 将地址赋值给 p

p->x // 获取A
```
或者可以使用typedef
```
// 使用 typedef 给这个结构体起个正式的名字叫 MyStruct struct这个整体就是一个数据类型
typedef struct {
    char x; 
    int y; 
    float z;
} MyStruct; 

// --------- 下面就不需要再写 struct 了！---------

MyStruct StructName; // 直接用别名声明变量
MyStruct *p;         // 直接用别名声明指针

StructName.x = 'A';
StructName.y = 66;
StructName.z = 1.23;

p = &StructName;     // 赋值地址
```
### enum
### 1. 最基本的用法

我们可以把相关的状态打包在一起，定义一个枚举：


```
// 定义一个叫 LED_Status 的枚举
enum LED_Status {
    OFF,    // 默认代表 0
    ON,     // 默认代表 1
    BLINK   // 默认代表 2
};

// 使用它来声明变量
enum LED_Status currentStatus;

// 赋值
currentStatus = ON;  // 其实等价于 currentStatus = 1;

// 用在判断里，代码变得极其好读！
if (currentStatus == ON) {
    // 执行开灯逻辑
}
```

**底层揭秘：** 在 C 语言眼里，`enum` 里的单词本质上就是**整数（`int`）**。默认情况下，第一个词等于 `0`，后面依次递增 `1`。也就是说，上面的 `OFF` 就是 `0`，`ON` 就是 `1`，`BLINK` 就是 `2`。

---

### 2. 自定义数字（不一定非要从 0 开始）

如果你不想按 0, 1, 2 这样顺延，你完全可以自己规定数字：

```
enum ErrorCode {
    SUCCESS = 200,      // 成功
    NOT_FOUND = 404,    // 找不到
    SERVER_ERROR = 500  // 服务器错误
};
```

如果你只给第一个赋值，后面的依然会自动 `+1`：


```
enum Weekday {
    MONDAY = 1, // 指定为 1
    TUESDAY,    // 自动变成 2
    WEDNESDAY   // 自动变成 3
};
```

```
// 用 typedef 给枚举起个别名叫 State
typedef enum {
    STOP = 0,
    RUNNING = 1,
    PAUSE = 2
} State;

// 现在用起来就跟 int、char 一样简单清爽了！
State motor1 = RUNNING; 
State motor2 = STOP;
```