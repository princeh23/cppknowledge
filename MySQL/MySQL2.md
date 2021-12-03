# 参考文章

- [掘金贾不假](https://juejin.cn/post/6850037271233331208#heading-76)

# 整体性问题

- Conception：
  1. 架构

- Question + Answer：

# 基础/语法问题

- Conception：
  1. 数据库三范式
  2. char和varchar
  3. drop、delete、truncate
  4. 巴斯-科德范式（BCNF第三范式的子集）、第四范式(4NF）和第五范式（5NF，又称完美范式）
- Question + Answer：
  1. 

# 引擎

- Conception：
  1. InnoDB、MyISAM、Memory
- Question + Answer：
  1. 存储引擎对比？

# 索引

- Conception：

    数据结构角度：

  1. B+树索引、Full-Text全文索引、哈希索引、R-Tree索引
  2. 物理存储角度：
  3. 聚簇索引、非聚簇索引（辅助索引、二级索引）
  4. 逻辑角度：
  5. 唯一索引
  6. 普通索引
  7. 主键索引
  8. 单值索引、单列索引
  9. 联合索引、复合索引、多列索引
  10. 覆盖索引
  11. 冗余索引、重复索引
  12. 一些规则：
  13. 一些规则：最左前缀原则、索引下推
  14. 不太常见
  15. 倒排索引、反向索引（根据内容找主键，别的是根据主键找内容）
  16. 倒序索引（顺序反）
  17. 前缀索引（用一个列中的前几个字符建立索引）
  18. 空间索引

- Question + Answer：

  1. 索引是什么？为什么要有索引？
  2. 索引的优缺点？
  3. 索引分类？
  4. 什么时候索引失效？

# 事务

- Conception：
  1. 四个特性（ACID）
  2. 并发事务访问相同记录的情况（读读，读写写读，写写）
  3. 脏写脏读、不可重复读、幻读（小林写的好）
  4. 4个隔离级别
  5. MVCC
  6. 当前读、快照读
- Question + Answer：
  1. 

# 日志

- Conception：
  1. Write Ahead Loging技术
  2. 逻辑日志、物理日志
  3. redolog
  4. undolog
  5. binlog
  6. relay log、slow query log、error log
  7. gereral log
  8. redolog和binlog的区别

# 锁

- Conception：
  1. 全局锁（FTWRL Flush tables with read lock）
  2. 表锁（表锁、MDL、意向锁、AUTO-INC锁）
  3. 行锁（Record Lock记录锁、Gap Lock间隙锁、Next-key Lock临键锁）
  4. 读锁|共享锁、写锁|排他锁
  5. 意向共享锁 意向排他锁
  6. 乐观锁、悲观锁
  7. 记录锁 间隙锁 临键锁
  8. 死锁
- Question + Answer：
  1. 

# 键

- Conception：
  1. 超键、候选键、主键、外键

# 分区分库分表

- Conception：
  1. 分区
  2. 分表（垂直拆分、水平拆分）
  3. 分库（主从）

# 主从复制（同步）

- 

# 优化*

- Question + Answer：
  1. 

# 其他问题/概念

- [DDL, DML, DCL, TCL](https://www.cnblogs.com/heyonggang/p/9284271.html)
- [T-SQL](https://blog.csdn.net/weixin_37519752/article/details/80913773?spm=1001.2101.3001.6650.3&utm_medium=distribute.wap_relevant.none-task-blog-2%7Edefault%7ECTRLIST%7Edefault-3.wap_blog_relevant_default&depth_1-utm_source=distribute.wap_relevant.none-task-blog-2%7Edefault%7ECTRLIST%7Edefault-3.wap_blog_relevant_default)

# 遗留问题

- 一致性读 READVIEW
- 两阶段提交

