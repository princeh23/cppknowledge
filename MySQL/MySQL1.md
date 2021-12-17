# 参考文章

- [整体类：掘金 贾不假](https://juejin.cn/post/6850037271233331208#heading-76)
- [程序员库森](https://github.com/cosen1024/Java-Interview)

# 整体性问题

- Conception：
  1. 架构：客户端、连接器、查询缓存、分析器、优化器、执行器、存储引擎
- Question：
  1. 一条查询语句是怎么执行的？/MySQL架构？
  2. 一条更新语句是怎么执行的？（两阶段提交）

# 基础/语法问题

- Conception：
  1. 数据库三范式
  2. char和varchar
  3. drop、delete、truncate
  3. 存储过程
  4. 巴斯-科德范式（BCNF第三范式的子集）、第四范式(4NF）和第五范式（5NF，又称完美范式）
- Question：
  1. 说说三范式？
  1. char和varchar区别？
  1. varchar为什么建议不超过255？
  1. SQL约束（对表中数据的一种约束）？
  1. drop、delete、truncate区别？
  1. in和exists区别
  1. 说说存储过程？

# 引擎

- Conception：
  1. InnoDB、MyISAM、Memory
- Question：
  1. 存储引擎对比？

# 索引

- Conception：

  1. **数据结构角度：**
  2. B+树索引、Full-Text全文索引、哈希索引、R-Tree索引
  3. **物理存储角度：**
  4. 聚簇索引：叶子节点存数据
  5. 非聚簇索引（辅助索引、二级索引）：叶子节点存主键
  6. **逻辑角度**：
  7. 唯一索引
  8. 普通索引
  9. 主键索引
  10. 单值索引、单列索引
  11. 联合索引、复合索引、多列索引
  12. 覆盖索引：查询语句的结果从索引中就可以取得，不需要回表
  13. 冗余索引、重复索引
  14. **一些规则：**
  15. 最左前缀原则
  16. 索引下推
  17. **不太常见：**
  18. 倒排索引、反向索引
  19. 倒序索引
  20. 前缀索引：把很长字段的前面的一部分作为索引
  21. 空间索引
- Question：

  1. 索引是什么？为什么要有索引？
  2. 索引的底层实现？
  3. 索引为什么用B+树？
  4. 索引的优缺点？
  5. 如何创建索引？
  6. 创建索引时候需要注意什么？
  7. 创建索引的原则
  8. 索引分类？
  9. 普通索引和唯一索引怎么选择？
  10. 什么是回表？
  11. 聚簇索引和非聚簇索引？
  12. 非聚簇索引一定会回表吗？
  13. 联合索引？为什么注意联合索引的顺序？
  14. 前缀索引？
  15. 说说最左前缀原则？
  16. 说说索引下推？
  17. 怎么查看有没有用到索引？
  18. 为什么推荐使用自增长主键作为索引？
  19. 使用索引一定能提高查询性能吗？
  17. 什么时候索引失效？什么时候不走索引？

# 事务

- Conception：
  1. 四个特性（ACID）
  2. 并发事务访问相同记录的情况（读读，读写写读，写写）
  3. 脏写脏读、不可重复读、幻读
  4. 4个隔离级别
  5. 当前读、快照读
  6. MVCC
  7. READ VIEW
- Question：
  1. 事务是什么？事务的四个特性？
  1. 事务四种隔离级别和三种读的问题解决了哪些？
  1. 说说脏读、不可重复读、幻读？
  1. 说说MVCC？有什么作用？
  1. 事务的实现原理/MySQL事务日志说一下？
  1. 可重复读解决幻读了吗？
  1. 在事务中可以混合使用存储引擎吗？
  1. 当前读、快照读？
  1. 什么是MVCC？
  1. MVCC的实现原理？

# 日志

- Conception：
  1. Write Ahead Loging技术
  2. 逻辑日志、物理日志
  3. redolog
  4. undolog
  5. binlog
  6. relay log、slow query log、error log
  7. gereral log
  7. 两阶段提交
- Question：
  1. WAL是什么？
  2. redolog是什么？binlog是什么？undolog是什么？relaylog是什么？
  3. 两阶段提交？Innodb事务为什么要两阶段提交

# 锁

- Conception：
  1. 全局锁
  2. 粒度分：
  3. 表锁（表锁、MDL、意向锁、AUTO-INC锁）
  4. 行锁（Record Lock记录锁、Gap Lock间隙锁、Next-key Lock临键锁）
  5. 页锁
  6. 属性/类别分：
  7. 读锁|共享锁、写锁|排他锁
  8. 乐观锁、悲观锁
  9. 状态分：
  10. 意向共享锁 意向排他锁
  11. 死锁
- Question：
  1. 锁的分类？
  1. 为什么加锁？
  1. InnoDB行锁怎么实现的？
  1. 死锁？
  1. 隔离级别与锁的关系？
  1. 优化锁的意见？

# 键

- Conception：
  1. 超键、候选键、主键、外键
- Question：
  1. 说说超键、候选键、主键、外键？
  1. 为什么推荐使用自增 id 作为主键？

# 分区分库分表

- Conception：
  1. 分区
  2. 分表（垂直拆分、水平拆分）
  3. 分库（主从）

- Question：
  1. 为什么分表？为什么分库？
  2. 垂直拆分？水平拆分？
  3. 分库分表方式？
  4. 分库分表中间件？

# 主从复制（同步）

- Conception：
  1. 主从复制
  2. 读写分离
  3. 主从延迟
- Question：
  1. 主从如何同步数据？（讲讲那个图）
  2. 同步策略
  3. 主从复制涉及到哪三个线程？
  4. 主从同步目的/作用
  5. 主从延迟原因？怎么解决？

# 问题

- Question：
  1. 为什么一条sql语句查询一直慢？
  1. 为什么一条sql语句查询偶尔慢？
  1. 删除数据表大小没变？（45讲13讲）
  1. 为什么不要使用长事务
  1. 数据库CPU飙升到500%怎么处理？
  1. 查询性能的优化方法？
  1. 超大分页怎么处理？
     - 靠缓存，可预测性的提前查到内容，缓存到redis
  1. 慢查询？怎么优化？

# 优化

- Question：
  1. 说说sql调优思路
  1. 大表数据查询怎么优化？
  1. 数据库设计方案优化？
  1. 关联查询如何优化？
  1. 如何优化查询过程中的数据访问？
  1. [explain优化](https://juejin.cn/post/6844904163969630221)

# 一些我暂时不知道放在哪的点

- buffer pool（moon聊技术34）

# 其他问题/概念

- [DDL, DML, DCL, TCL](https://www.cnblogs.com/heyonggang/p/9284271.html)
- [T-SQL](https://blog.csdn.net/weixin_37519752/article/details/80913773?spm=1001.2101.3001.6650.3&utm_medium=distribute.wap_relevant.none-task-blog-2%7Edefault%7ECTRLIST%7Edefault-3.wap_blog_relevant_default&depth_1-utm_source=distribute.wap_relevant.none-task-blog-2%7Edefault%7ECTRLIST%7Edefault-3.wap_blog_relevant_default)

