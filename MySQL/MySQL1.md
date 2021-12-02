# 参考文章

- [掘金贾不假](https://juejin.cn/post/6850037271233331208#heading-76)

# 整体性问题

1. 概念：
   - 架构
2. 问题：

# 基础

- 数据库三范式
- 巴斯-科德范式（BCNF第三范式的子集）、第四范式(4NF）和第五范式（5NF，又称完美范式）
- char和varchar
- drop、delete、truncate

# 引擎

- InnoDB、MyISAM、Memory

# 索引

- 树索引、哈希索引

- 

- 聚簇索引、非聚簇索引（辅助索引、二级索引）

- 

- 唯一索引

- 普通索引

- 主键索引

- 

- 单值索引、单列索引

- 联合索引、复合索引、多列索引

- 覆盖索引

- 冗余索引、重复索引

- 

- 一些规则：最左前缀原则、索引下推

- 

- 倒排索引、反向索引（根据内容找主键，别的是根据主键找内容）
- 倒序索引（顺序反）
- 前缀索引（用一个列中的前几个字符建立索引）
- 全文索引
- 空间索引
- 什么时候索引失效？
- 

# 事务

- 四个特性（ACID）
- 并发事务访问相同记录的情况（读读，读写写读，写写）
- 脏写脏读、不可重复读、幻读（小林写的好）
- 4个隔离级别
- MVCC
- *

# 日志*

- Write Ahead Loging技术
- 逻辑日志、物理日志
- redolog
- undolog
- binlog
- relay log、slow query log、error log
- gereral log
- redolog和binlog的区别

# 锁

- 读锁|共享锁、写锁|排他锁
- 全局锁、页面锁、表锁、行锁
- 乐观锁、悲观锁
- 记录锁 间隙锁 临键锁*
- 死锁

- 意向共享锁 意向排他锁

# 键

- 超键、候选键、主键、外键

# 分库分表*

# 主从同步、主从复制、读写分离*

# 优化*

- 

# 其他问题/概念

- [DDL, DML, DCL, TCL](https://www.cnblogs.com/heyonggang/p/9284271.html)
- [T-SQL](https://blog.csdn.net/weixin_37519752/article/details/80913773?spm=1001.2101.3001.6650.3&utm_medium=distribute.wap_relevant.none-task-blog-2%7Edefault%7ECTRLIST%7Edefault-3.wap_blog_relevant_default&depth_1-utm_source=distribute.wap_relevant.none-task-blog-2%7Edefault%7ECTRLIST%7Edefault-3.wap_blog_relevant_default)

# 遗留问题

- 一致性读
- 快照读、当前读

- 索引实现的原理
- 两阶段提交

