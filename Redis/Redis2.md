# 参考文章

# 整体

- Conception：

  1. Redis、Memcached

- Question：

  1. **什么是Redis？**

     -  本质上是一个key-value类型的数据库，和memcached类似，加载到内存中进行操作，纯内存操作，性能出色，是已知的性能最快的key-value数据库
     - 优点：
       - 读写性能出色
       - 支持数据持久化，AOF、RDB两种
       - 支持事务，所有操作是原子性的，可以通过MULTI和EXEC指令
       - 数据结构丰富
       - 支持主从复制、读写分离
     - 缺点：
       - 内存有限，不适合海量数据的高性能读写
       - 宕机会导致从机未能及时同步

  1. **Redis和Memcached相比？**

     - |          | Memcached          | Redis                               |
       | -------- | ------------------ | ----------------------------------- |
       | 数据类型 | 简单的字符串       | string、list、hash、set、sorted set |
       | 持久化   | 不支持             | AOF、RDB                            |
       | 网络IO   | 非阻塞IO           | IO多路复用                          |
       | 集群模式 | 没有原生的集群模式 | 主从同步                            |

  1. **Redis为什么这么快？** 

     -  使用内存存储，没有磁盘IO的开销
     - 单线程处理请求，避免线程切换和锁资源的开销
     - 使用IO多路复用技术，使用epoll
     - 数据结构丰富，可以直接应用的优化数据
     - 冷热数据分离，热数据在内存中，冷数据在磁盘

  1. **为什么用Redis做缓存？**

     - 高性能
       - 热点数据直接操作缓存，速度快
     - 高并发
       - 缓存支持的并发数比数据库多，把数据库中的部分数据转移到缓存中，部分请求直接访问缓存

  1. **Redis应用场景？**

     - 缓存
     - 排行榜
     - 计数器：点击量、播放数
     - 分布式
     - 社交网络中的点、踩

# 数据类型

- Conception：
  1. 数据类型：底层实现
  2. string：SDS
  3. list：双向链表、压缩链表
  4. hash：压缩链表、哈希表/字典、
  5. set：哈希表/字典、整数集合
  6. zset：压缩链表、跳表
  7. GEO、Bitmap、HyperLogLog
  8. quicklist（双向链表）、listpack（压缩链表）
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

# 删除/替换/内存淘汰策略 

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