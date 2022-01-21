# 参考文章

- 程序员库森
- [CSDN Redis面试题](https://blog.csdn.net/zhaoxi2020/category_11053951.html?spm=1001.2014.3001.5482)

# 整体

- Conception：

  1. Redis、Memcached

- Question：

  1. **什么是Redis？**

     -  本质上是一个key-value类型的数据库，和memcached类似，加载到内存中进行操作，纯内存操作，性能出色，是已知的性能最快的key-value数据库
     - 优点：
       - 读写性能出色
       - 数据结构丰富
       - 支持数据持久化，AOF、RDB两种
       - 支持事务，所有操作是原子性的，可以通过MULTI和EXEC指令
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
  
     - String：二进制安全、可以包含任何数据，比如jpg图片或者序列化的对象（常规计数）
  
     - List：简单的字符串列表，按照插入顺序排序（最新回复）
  
     - Hash：键值对集合（）
  
     - Set：无序的去重集合（共同好友、共同关注）
  
     - SortedSet：可排序版的set（排行榜）
  
     - Bitmap：位图，一个以位为单位的数据
  
     - Hyperloglog：统计基数，有误差
  
     - Geospatial：地理位置信息（打车定位）
  
     - ```cpp
       SET runoob "菜鸟教程"
       GET runoob
       
       HMSET runoob field1 "Hello" field2 "World"
       HGET runoob field1
       
       lpush runoob redis
       lpush runoob mongodb
       lpush runoob rabbitmq
       lrange runoob 0 10
           
       sadd runoob redis
       sadd runoob rabbitmq
       smembers runoob
           
       zadd runoob 0 redis
       zadd runoob 0 mongodb
       ZRANGEBYSCORE runoob 0 1000
       ```

# 2种持久化

- Conception：
  1. AOF（Append Only File）
  2. AOF重写
  3. RDB（Redis DataBase）
  4. 混合持久化
- Question：
  1. **AOF、优点、缺点？**
     - 定义：以日志的形式记录每个操作，记录写指令不记录读指令，只许追加文件不允许修改，AOF保存的是appendonly.aof文件，恢复的时候从前到后执行一次
     - AOF重写：一直追加写文件会又来越大，重写机制可以进行文件压缩，只保留可以恢复数据的最小指令集
     - 机制：每次修改同步、每秒同步、不同步
     - 缺点：aof文件大，恢复速度慢；aof运行效率比rdb慢，每秒同步效率好
  1. **RDB、优点、缺点？**
     - 定义：指定时间间隔将数据快照写入磁盘，恢复的时候将快照文件直接读入内存
     - 优点：适合大规模、对数据完整性、一致性要求不高
     - 缺点：每隔一段时间才备份，Redis宕机的话会丢失数据
  1. **如何选择？**
     - 对数据不敏感，可以关闭持久化
     - 可以承受数分钟的损失，如做缓存，只开RDB
     - 做内存数据库，RDB、AOF都开启，RDB时候做数据备份，AOF保证数据不丢失
  1. **混合持久化？**
     - Redis4.0
     - 前半段是RDB格式全量数据，后半段是AOF增量数据
     - 优点：绝大部分是RDB，加载速度快，增量是AOF，避免了数据丢失
     - 缺点：兼容性差，Redis4.0之前不识别该aof文件；阅读性差，前半段是RDB
  1. **Redis持久化数据和缓存怎么做扩容？**
     - 如果Redis被当做缓存使用，使用一致性哈希实现动态扩容缩容。
     - 如果Redis被当做一个持久化存储使用，必须使用固定的keys-to-nodes映射关系，节点的数量一旦确定不能变化。否则的话（即Redis节点需要动态变化的情况），必须使用可以在运行时进行数据再平衡的一套系统，而当前只有Redis集群可以做到这样。
     - **看参考文章CSDN里有很多Redis面试题**

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