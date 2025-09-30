# c/cpp大纲

***

## 📘 C/C++ 系统学习 GitBook 目录

### 1. 基础入门

* 1.1 开发环境与工具链
  * 编译器（gcc/g++, clang, MSVC）
  * 构建工具（make, cmake）
  * 调试工具（gdb, lldb, Visual Studio Debugger）
* 1.2 C 基础语法
  * 数据类型与变量作用域
  * 运算符与表达式
  * 控制结构 (if, switch, for, while)
  * 输入输出 (stdio.h)
* 1.3 函数与程序结构
  * 函数定义与声明
  * 参数传递方式
  * 头文件与多文件组织
  * 宏与内联函数
* 1.4 指针与内存
  * 指针基础与运算
  * 数组与字符串
  * 函数指针与回调
  * 动态内存分配 (malloc/free)
* 1.5 结构化数据
  * 结构体、共用体、枚举
  * 位域与内存布局

***

### 2. C 高级进阶

* 2.1 内存与底层
  * 内存对齐与填充
  * 多级指针与 void\*
  * 内存泄漏与调试工具
* 2.2 文件与输入输出
  * 文件读写 (fopen/fread/fprintf)
  * 文本与二进制文件
* 2.3 预处理器
  * 宏定义与条件编译
  * include guard 与 pragma once
* 2.4 C 标准库
  * string.h, stdlib.h, math.h
  * 时间与随机数
  * 静态库与动态库

***

### 3. C++ 基础

* 3.1 C++ 与 C 的区别
  * 引用、RAII、new/delete
  * iostream 输入输出
* 3.2 类与对象
  * 封装、构造/析构函数
  * this 指针与友元函数
* 3.3 继承与多态
  * 继承方式
  * 函数重载与覆盖
  * 虚函数与抽象类
  * 多重继承与虚继承
* 3.4 运算符重载
  * 算术运算符
  * 输入输出 << >>
  * 下标运算符 \[]

***

### 4. C++ 进阶

* 4.1 模板编程
  * 函数模板与类模板
  * 特化与偏特化
* 4.2 标准模板库 STL
  * 容器 (vector, map, set)
  * 迭代器与算法
  * 函数对象与 lambda
  * 智能指针 (unique\_ptr, shared\_ptr, weak\_ptr)
* 4.3 现代 C++ 特性
  * auto, decltype
  * 移动语义与右值引用
  * constexpr
  * 并发 (std::thread, std::async)
  * C++20 Concepts

***

### 5. 工程与实践

* 5.1 编译与构建
  * CMake
  * 多平台编译与条件编译
* 5.2 调试与优化
  * gdb/lldb 调试技巧
  * 内存调试工具
  * 性能分析 (perf, gprof)
* 5.3 设计模式与架构
  * 单例模式、工厂模式
  * 观察者模式、策略模式
  * RAII 与资源管理
* 5.4 网络与系统编程
  * Socket 编程
  * 多线程与进程间通信
  * 异步与事件驱动

***

### 6. 深入底层与扩展

* 6.1 操作系统相关
  * Linux 系统调用
  * 内核与用户态
* 6.2 编译原理与工具链
  * 编译、链接、加载流程
  * ELF 文件格式
* 6.3 高性能编程
  * Cache 优化与内存对齐
  * SIMD 与并行计算
  * OpenMP, TBB
* 6.4 跨学科扩展
  * C/C++ 与 Python (pybind11)
  * CUDA 与数值计算

***

### 7. 高级实践与未来趋势

* 7.1 测试与质量保障
  * 单元测试 (gtest, Catch2, doctest)
  * Mock 测试与集成测试
  * 静态分析 (clang-tidy, cppcheck)
  * 内存检测 (valgrind, ASan, UBSan)
* 7.2 并发与多线程编程
  * 基础：pthread/std::thread, mutex, 条件变量
  * 高级：原子操作 (std::atomic)、内存模型
  * 无锁编程与 lock-free 结构
  * 协程 (C++20 coroutine)
* 7.3 C++ 高级范式与趋势
  * 泛型编程与模板元编程 (TMP)
  * Concepts 与约束 (C++20)
  * constexpr 计算
  * 函数式编程思想 (lambda 链式、ranges)
  * 现代库生态 (Boost, fmt, spdlog, json, protobuf, gRPC)

***
