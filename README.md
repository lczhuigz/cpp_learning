# C++ 学习示例 (cpp-learning)

本仓库包含了系统学习 C++ 编程的完整示例代码，按章节循序渐进地组织，从基础语法到面向对象编程、模板编程、继承派生、异常处理等高级主题。

## 项目结构

```
cpp_learning/
├── chapter01/          # 入门：Hello World、宏定义、多文件编译
├── chapter02/          # 基本数据类型与类型转换
├── chapter03/          # 流程控制：if/for/while/switch/goto
├── chapter04/          # 数组、结构体、枚举、typedef
├── chapter05/          # 指针与内存管理
├── chapter06/          # 内联函数与引用
├── chapter07/          # 函数、模板与重载
├── chapter08/          # 矩阵运算（多文件示例）
├── chapter09/          # 类与面向对象编程
├── chapter10/          # 时间类练习
├── chapter11/          # 智能指针与字符串类
├── chapter12/          # 继承与派生
├── chapter13/          # 模板编程
├── chapter14/          # 错误处理与异常
└── chapter15/          # 高级特性：友元、RTTI、类型转换
```

## 章节内容简介

| 章节 | 主要内容 | 典型示例 |
|------|----------|----------|
| chapter01 | 编译运行、宏定义、多文件编译 | `hello.cpp`, `multi-file/` |
| chapter02 | 数据类型、隐式转换、精度丢失 | `conversion.cpp`, `overflow.cpp` |
| chapter03 | 条件分支、循环控制 | `if.cpp`, `for.cpp`, `switch.cpp` |
| chapter04 | 数组、结构体、枚举、CMake | `array.cpp`, `enum.cpp`, `cmake-demo/` |
| chapter05 | 指针操作、内存分配、栈与堆 | `pointer.cpp`, `new-delete.cpp` |
| chapter06 | 内联函数、引用用法 | `inline.cpp`, `reference.cpp` |
| chapter07 | 函数重载、模板函数、函数指针 | `template1.cpp`, `function-overload.cpp` |
| chapter08 | 矩阵点乘优化（SIMD/NEON） | `matoperation.cpp`, `matoperation.hpp` |
| chapter09 | 类、构造函数、析构函数、静态成员 | `constructor.cpp`, `static.cpp` |
| chapter10 | 时间类实现练习 | `example1/` ~ `example5/` |
| chapter11 | 智能指针、运算符重载 | `unique_ptr.cpp`, `shared_ptr.cpp` |
| chapter12 | 继承、多态、虚函数 | `derive.cpp`, `virtual.cpp` |
| chapter13 | 类模板、模板特化、非类型参数 | `mattemplate.cpp`, `specialization.cpp` |
| chapter14 | 断言、异常处理、错误返回 | `assert.cpp`, `error1.cpp` ~ `error5.cpp` |
| chapter15 | 友元类、嵌套类、RTTI、类型转换 | `friend1.cpp`, `rtti.cpp`, `const_cast.cpp` |

## 环境依赖

- **C++ 编译器**：推荐 GCC (g++)、MinGW、MSYS2 或 Visual Studio 的 `cl`
- **CMake**：用于构建含 `CMakeLists.txt` 的多文件项目（可选）
- **标准**：支持 C++17 及以上

## 快速开始

### 单文件编译

```bash
# Linux/macOS
g++ -std=c++17 -O2 -Wall chapter01/hello.cpp -o bin/hello
./bin/hello

# Windows
g++ -std=c++17 -O2 -Wall chapter01/hello.cpp -o bin/hello.exe
.\bin\hello.exe
```

### 多文件编译

```bash
g++ -std=c++17 chapter01/multi-file/main.cpp chapter01/multi-file/mul.cpp -o bin/multi
./bin/multi
```

### 使用 CMake 构建

适用于包含 `CMakeLists.txt` 的目录（如 `chapter04/cmake-demo/`）：

```bash
mkdir -p build && cd build
cmake ..
cmake --build .
```

生成的可执行文件位于 `build` 目录或子目录中。

## 示例说明

- **单文件示例**：直接在对应章节目录下找到 `.cpp` 文件编译运行
- **多文件示例**：部分章节包含子目录（如 `chapter01/multi-file/`），需同时编译多个源文件
- **CMake 示例**：含 `CMakeLists.txt` 的目录可使用 CMake 统一构建

## 添加新示例

1. 在对应 `chapterX/` 目录下添加源文件
2. 多文件示例建议创建子目录并添加 `CMakeLists.txt`
3. 代码中添加适量注释，便于学习理解

## 许可

本仓库为个人学习示例代码，使用或转载时请注明出处并联系作者获取许可。