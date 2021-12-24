# 基础

- Conception：
  1. C和C++区别、和Java区别、和python区别
  1. 预处理、编译、汇编、链接
  2. 静态链接、动态链接
  3. 动态编译、静态编译
  4. 动态联编、静态联编
  5. 动态绑定 静态绑定
- Question：
  1. C和C++有什么区别？
     - C++是面向对象的语言，C是面向过程的语言
     - C++引入new/delete的概念，取代了C中malloc/free的概念
     - C++引入引用，C没有
     - C++引入类，C没有
     - C++引入函数重载，C没有
  2. C++和Python的区别？
  3. C++和Java的区别？

# C++基础语法

- Conception：
  
  1. 声明、定义
  2. 指针、引用
  3. 函数传递参数（形参、实参  值传递、指针传递、引用传递）
  4. 指针常量、常量指针
  5. 指针数组、数组指针
  6. 悬挂指针、野指针
  7. 函数指针
  8. static
  9. #define 
  10. typedef
  11. const 指针常量、常量指针 顶层const、底层const
  12. volatile、mutable、explicit
  13. inline
  14. #ifdef、#else、#endif、#ifndef
  15. sizeof、strlen
  16. strcpy、sprintf、memcpy
  17. extern"C"
  18. 异常处理（try catch throw exception类）
  
- Question：

  1. 数组中a和&a有什么区别？

     - ```cpp
       int a[10]; 
       int (*p)[10] = &a;
       
       a是数组名，也是数组元素首地址;
       a+1表示地址+1，表示a[1]的地址;
       *(a + 1) = a[1];
       
       &a是数组的指针，类型为int (*)[10]（数组指针）
       &a + 1表示数组首地址加上整个数组的偏移，表示a尾元素再下一个元素的地址
       ```

  2. 数组指针、指针数组？

     - http://c.biancheng.net/view/335.html

  3. static关键字？

     - 

  4. 

# C++面向对象

- Conception：
  1. 三大特征
  2. 访问权限public private protected
  3. struct和class
  4. 构造函数（默认构造函数、重载构造函数、拷贝构造函数、移动构造函数）
  5. this指针
  6. 成员初始化列表
  7. 拷贝构造函数、复制运算符
  8. 析构函数
  9. 初始化、复制
  10. 拷贝初始化、直接初始化
  11. 多态（继承+虚函数实现） 静态多台 动态多态
  12. 虚函数、纯虚函数、虚函数表、虚函数指针
  13. 继承 组合
  14. 覆盖、重载、重写、重定义（隐藏）
  15. 动态绑定 静态绑定
  16. 深拷贝、浅拷贝
  17. 友元函数、友元类
  18. 四个强制类型转换符（static_cast、dynamic_cast、const_cast、reinterpret_const、）
  19. final、override 
  20. RTTI
  1. 模板函数、模板类
- Question：
  1. 

# C++内存管理

- Conception：
  1. 内存分区：堆栈全局常量代码区
  1. 堆和栈
  1. new/delete和malloc/free
  1. malloc、calloc、realloc
  1. 内存对齐
  1. 内存泄露
  1. 空类大小、类大小、对象大小
  1. 对象复用、零拷贝
- Question：
  1. 

# C++ STL

- Conception：
  1. 容器、算法、迭代器、空间配置器、仿函数、适配器
  1. vector
  1. list
  1. deque
  1. map、set、multimap、multiset
  1. unordered_map、unordered_set
  1. 迭代器：迭代器失效
- Question：
  1. 

# C++11

- Conception：
  1. 智能指针
  1. nullptr
  2. Lambda表达式
  3. 右值引用&&
  3. 移动构造、完美转发
  4. constexpr
  4. auto、decltype
  4. for()
  4. tuple
- Question：
  1. 

# 情景设计题

- Conception：
  1. 1
- Question：
  1. 