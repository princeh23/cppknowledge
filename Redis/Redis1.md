# 参考文章

# 整体



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
  1. 

# 2种持久化

- Conception：
  1. AOF（Append Only File）
  2. RDB（Redis DataBase）
- Question：
  1. 

# 主从复制

# Sentinel哨兵集群

# Cluster分片集群 

# 淘汰策略

- Conception：
  1. 定时删除
  2. 惰性删除
  3. 定期删除

# 删除/替换策略 

- Concetion：
  1. noevction
  2. volatile-lru volatile-random volatile-ttl volatile-lfu
  3. allkeys-lru allkeys-randon allkeys-lfu

# 内存管理 

# 缓存问题

- Conception：
  1. 缓存和数据库的数据不一致
  2. 缓存雪崩
  3. 缓存击穿
  4. 缓存穿透
  5. 缓存预热、缓存降级
- Q

# 事务

# 分布式

# Redis6.0多线程