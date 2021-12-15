# 参考文章

# 整体

- Conception：
  1. Redis、Memcached
- Question：
  1. 什么是Redis？
  1. Redis应用场景？
  1. Redis为什么这么快？ 
  1. 优点？缺点？

# 数据类型

- Conception：
  1. 数据类型：底层实现
  2. string：SDS
  3. list：双向链表、压缩链表
  4. hash：压缩链表、哈希表/字典、
  5. set：哈希表/字典、整数集合
  6. zset：压缩链表、跳表
  6. GEO、Bitmap、HyperLogLog
  7. quicklist（双向链表）、listpack（压缩链表）
- Question：
  1. 八种数据类型？应用场景？

# 2种持久化

- Conception：
  1. AOF（Append Only File）
  2. RDB（Redis DataBase）
- Question：
  1. AOF、优点、缺点？
  1. RDB、优点、缺点？
  1. 如何选择？

# 3种过期键删除策略

- Conception：
  1. 定时删除
  2. 惰性删除
  3. 定期删除
- Question：
  1. 

# 删除/替换策略 

- Concetion：
  1. noevction
  2. volatile-lru volatile-random volatile-ttl volatile-lfu
  3. allkeys-lru allkeys-randon allkeys-lfu

# 缓存问题

- Conception：
  1. 缓存和数据库的数据不一致
  2. 缓存雪崩
  3. 缓存击穿
  4. 缓存穿透
  5. 缓存预热、缓存降级
- Question：
  1. 

# 部署方式/高可用方案

- Conception：
  1. 单机模式
  2. 主从
  3. 哨兵
  4. Cluster集群

# 主从

- Conception：
  1. 主从同步
- Question：
  1. 

# Sentinel哨兵集群

- Conception：
  1. 哨兵
- Question：
  1. 哨兵作用？选举过程？

# Cluster分片集群 

- Conception：
  1. 哈希槽
- Question：
  1. 怎么存放数据？

# 事务

- Conception：
  1. 
  1. 相关命令
- Question：
  1. 什么是Redis事务？

# 分布式锁

- Conception：
  1. Redis、MySQL、Zookeeper分布式锁
- Question：
  1. 

# 单线程、Redis6.0多线程

- Conception：
  1. 
- Question：
  1. 

# 优化

- Question：
  1. 如何提高 Redis 命中率？
  2. 怎么优化 Redis 的内存占用？

# todo

- 容灾