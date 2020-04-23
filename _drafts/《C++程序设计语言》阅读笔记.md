## 前言

“我根本不会c++”

## 第一章

看完之后，发现我确实不会c++，要彻底放弃算法竞赛训练出来的编程思想和习惯了。希望读完后面的章节之后能能理解C++的设计思想和编程风格并能运用合适的语法特性写出优雅的程序，Go！

## 第二章

### 初始化

在c++中，初始化最好使用{}，确保不发生导致信息丢失的类型转换

```c++
double d2{2.3}; //instead of double d2=2.3
int i1 {7.2};//error
complex<double> z{d1,d2};//right
```

但是auto要和=配合，因为不存在类型转换

### constexpr

编译时求值？常量？没看懂

### nullptr

空指针都用这个

### 异常

#### throw

第13章

### 第三章

#### initializer_list<T>

用于使用列表初始化

```c++
vector v1={1,2,3};
vector::vector(std::initializer_list<int> list):{……}
```

