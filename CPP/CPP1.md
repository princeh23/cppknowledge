# 基础

- Conception：
  1. C和C++区别、和Java区别、和python区别
  2. 预处理、编译、汇编、链接
  3. 动态链接、静态链接
  4. 动态编译、静态编译
  5. 动态联编、静态联编
  6. 动态绑定、静态绑定
  7. 动态内存分配、静态内存分配
- Question：
  1. C和C++有什么区别？
  2. C++和Python的区别？
  3. C++和Java的区别？
  4. 动态链接、静态链接？

# C++基础语法

- Conception：
  1. **定义相关**
  2. 声明、定义
  3. 全局变量、局部变量
  4. **指针相关**
  5. 指针、引用
  6. 指针、句柄
  7. 函数传递参数（形参、实参  值传递、指针传递、引用传递）
  8. 悬挂指针、野指针
  9. 指针常量、常量指针
  10. 指针数组、数组指针
  11. 函数指针
  12. **关键字相关**
  13. static
  14. #define 
  15. typedef
  16. const 指针常量、常量指针 顶层const、底层const
  17. volatile、mutable、explicit
  18. inline
  19. #ifdef、#else、#endif、#ifndef
  20. extern"C"
  21. **函数相关**
  22. sizeof、strlen
  23. strcpy、sprintf、memcpy
  24. **其他**
  25. 异常处理（try catch throw exception类）
- Question：
  1. 声明、定义？
  2. 全局变量和局部变量有什么区别？操作系统和编译器怎么知道？
  3. 指针和引用？
  4. 指针和句柄？
  5. 数组中a和&a有什么区别？
  6. 指针相关（常量指针/指针常量、悬挂指针/野指针、指针数组/数组指针、函数指针）
  7. static关键字？
  8. inline
  9. const
  10. const和#define区别
  11. typedef和define区别
  12. #ifdef、#else、#endif、#ifndef
  13. extern"C"
  14. volatile
  15. sizeof、strlen的区别？
  16. strcpy、sprintf、memcpy的区别？

# C++面向对象

- Conception：
  1. struct和class
  2. 访问权限public private protected
  3. 三大特征：封装、继承、多态
  4. 静态多态/静态绑定、动态多态/动态绑定
  5. 1
  6. 初始化、赋值
  7. 直接初始化、拷贝初始化
  8. 构造函数（默认构造函数、重载构造函数、拷贝构造函数、移动构造函数）
  9. 拷贝构造函数、赋值运算符
  10. this指针
  11. 成员初始化列表
  12. 
  13. 析构函数
  14. 
  15. 虚函数、纯虚函数、虚函数表、虚函数指针
  16. 
  17. 继承 组合
  18. 
  19. 重载、隐藏、重写/覆盖
  20. 
  21. 四个强制类型转换符（static_cast、dynamic_cast、const_cast、reinterpret_const）
  22. RTTI
  23. 
  24. 空类相关
  25. 
  26. 模板函数、模板类
  27. 模板函数、模板类的特例化
  28. 
  29. 深拷贝、浅拷贝
  30. 友元函数、友元类
  31. final、override 
  
- Question：
  1. 结构体？
  2. C和C++的struct有什么不同？
  3. C++中struct和class的区别？
  4. 面向对象三大特征？
  5. 多态的实现方式？
  6. 动态多态/动态绑定作用？必要条件？如何实现？
  7. 访问权限？
  8. 初始化、赋值？
  9. 直接初始化、拷贝/复制初始化？
  10. 为什么基类的构造函数不能为定义为虚函数？
  
  11. 构造函数能抛出异常吗？
  12. 拷贝构造函数、赋值运算符区别？
  13. 虚函数
  14. 纯虚函数？
  15. 虚函数表
  16. 如何让一个类不能被实例化？
  17. 为什么基类的虚构函数需要定义为虚函数？
  18. 析构函数能抛出异常吗？
  19. 多继承存在的问题？如何消除多继承中的二义性？
  20. 重载、隐藏、重写/覆盖
  
  21. 强制类型转换符？
  22. RTTI？
  23. sizeof一个空类的值为多少？
  24. 空类有哪些成员函数？
  25. 模板函数、模板类的特例化

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
  1. C++的内存分区？
  2. new/delete和malloc/free？
  3. delete和delete[]有什么区别？
  4. malloc申请的内存是否可以使用delete，new申请的内存是否可以使用free？
  5. 内存块太小导致new、malloc分配失败怎么办？
  6. 内存泄露？
  7. 内存的分配方式？
  8. 堆栈区别？
  9. 静态内存分配、动态内存分配？
  10. 如何构造一个类，使其只能在堆/栈上分配内存？
  11. 浅拷贝、深拷贝？
  12. 字节对齐、结构体对齐？

# C++ STL

- Conception：
  1. 容器、算法、迭代器、空间配置器、仿函数、适配器
  1. vector
  1. list
  1. deque
  1. map、set、multimap、multiset
  1. unordered_map、unordered_set
  1. 迭代器
- Question：
  1. STL是什么？
  2. STL两级空间配置器/内存优化？
  3. 容器有哪些？
  4. vector底层原理？
  5. vector中size和capacity区别？
  6. vector中reserve和resize区别？
  7. vector中的元素可以是引用吗？
  8. vector使迭代器失效的情况？
  9. vector1.5/2倍扩容原因？
  10. vector如何释放空间？
  11. 为什么vector的插入操作可能导致迭代器失效？
  12. 频繁的push_back()对vector性能的影响？
  13. list的底层实现原理？
  14. deque的底层实现原理？
  15. vector、list、deque适用场景？
  16. map、set、multiset、multimap底层原理？
  17. 为何map和set的插入删除效率比其他序列容器高，而且每次insert之后，以前保存的iterator不会失效？
  18. map的插入方式？
  19. map中find和[]的区别？
  20. map和vector中[]的区别？
  21. unordered_map、unordered_set、unordered_multimap、unordered_multiset底层原理？
  22. 迭代器底层实现原理？
  23. 迭代器的型别？
  24. 迭代器的种类？
  25. 各种容器删除一个元素？
  26. 迭代器失效？
  27. 容器适配器？
  28. 如何在共享内存上使用STL？

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
  1. 智能指针？
  1. 右值引用、移动构造、完美转发?

# 情景设计题

- Conception：
  1. 1
- Question：
  1. 设置地址为为0x67a9 的整型变量的值为0xaa66？
  1. 手写实现智能指针?