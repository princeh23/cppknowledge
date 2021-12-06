# 整体性

- Conception：
  1. OSI七层、TCP/IP四层、五层
- Question：
  1. 每一层的作用 ？
  2. 每一层的常见协议？
  3. 每一层传输的基本数据单元（流、段、包、帧、01电信号）？
  3. 为什么要分层？

# HTTP

- Conception：
  1. HTTP定义
  2. HTTP状态码
  3. HTTP请求方式
  4. HTTP请求/相应报文
  5. HTTP1.0
  6. HTTP1.1
  7. HTTPS（SST/TLS）
  8. HTTP2.0
  9. HTTP3.0
  9. DNS
  10. Cookie/Session
  11. 数字签名、数字证书
- Question：
  1. 如何理解HTTP？
  2. 说一下HTTP常见的请求方式？
  3. GET/POST区别？
  4. GET请求中URL编码的意义？
  5. HTTP状态码？（301、302）
  6. HTTP请求/相应报文格式、常见字段？
  7. HTTP请求的完整过程？
  8. HTTP1.0问题？
  9. HTTP1.1优点？
  10. HTTP1.1改进？
  11. HTTP1.1问题？
  12. HTTPS做了什么（三点）？
  13. HTTPS缺点？
  14. HTTP2.0改进？
  15. HTTP2.0问题？
  16. HTTP3.0改进？
  17. HTTP和HTTPS的区别？
  18. HTTP1.0和HTTP1.1的区别？
  19. 长连接和短连接？
  20. HTTP1.1和HTTP2.0的区别？
  21. HTTP2.0和HTTP3.0的区别？
  22. SSL/TLS
  23. SST/TLS握手过程 /HTTPS工作过程/HTTPS原理？
  24. Cookie和Session是什么？如何配合？区别？
  25. 分布式Session问题？
  15. 数字签名、数字证书？

# DNS

- Conception：
  1. 递归查询、迭代查询
  2. 负载均衡、负载分配
  3. 根服务器、顶级域服务器、权威服务器
  4. DNS缓存/域名缓存
- Question：
  1. DNS工作原理？
  2. DNS解析过程？
  3. DNS查询方式？
  4. DNS负载均衡？
  5. DNS域名缓存？

# TCP UDP

- Conception：
  1. TCP/UDP
  2. 三次握手
  3. 四次挥手
  3. TCP保活机制/保活计时器
  4. 超时重传、快速重传
  5. 滑动窗口
  6. 流量控制
  7. 拥塞控制（慢启动、拥塞避免、快速重传、快速恢复）
  8. 半连接、全连接队列
  8. 拆包、粘包
  9. MTU、MSS、RTO、RTT
  10. Socket
- Question：
  1. TCP/UDP区别？
  2. TCP特点、UDP特点 ？
  2. TCP/UDP对应的场景？
  3. TCP/UDP对应的协议？
  4. TCP/UDP头部？
  5. 三次握手
     - 过程？
     - 为什么是三次？
     - 为什么不是两次?
     - 为什么不是四次？
     - 第一二三次丢包各会发生什么？
  6. 四次挥手
     - 过程？
     - 为什么四次？
     - TIME_WAIT为什么2MSL？/为什么要等待2MSL?
     - TIME_WAIT太多怎么办？
     - TIME_WAIT是服务器还是客户端的状态？
  7. TCP如何保证的可靠性？
  8. 超时重传、快速重传？
  8. 为什么快速重传选择3次ACK？（阿秀80）
  9. 滑动窗口？
  10. 流量控制？
  11. 拥塞控制（慢启动、拥塞避免、快速重传、快速恢复）？
  12. 半连接队列、全连接队列？
  12. 拆包、粘包？
  13. 一些名词：MTU、MSS、RTO、RTT？
  14. 如何优化三次握手、四次挥手（小林）？
  15. Socket见网络编程

# IP

- Conception：
  1. ABCDE五类地址
  2. 子网掩码
  3. ARP、RARP、DHCP、ICMP
- Question：
  1. IP地址分类？
  2. Ping的作用？
  3. ARP协议的工作原理？
  4. 对ARQ协议的理解？
  4. RARP工作原理？

# 安全性问题

- Conception：
  1. SYN洪泛攻击
  2. DDos攻击（Distributed Denial of Service）
  3. XSS攻击（cross-site scripting）
  4. SQL注入
  5. CSRF攻击
- Question：
  1. SYN洪泛攻击？
  1. DDos攻击？
  2. Xss攻击？
  3. SQL注入？
  4. CSRF攻击？

# 遗留问题

- 服务器缓存？（阿秀9）

