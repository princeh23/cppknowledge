## Linux函数

- Linux数据下
- Question：
  1. Linux/Windows下数据的接收和发送
     - Linux：write、read
     - Windows：send()、recv
  2. **调用read（socketfd，buffer，n）时，返回0的情况？**
     - socketfd：读取的文件的描述符；buffer：写入的数据的缓冲区地址；n：要读取的数据的字节数
     - 返回值表示实际读取的字节数目
     - 如果返回值为 0，表示 EOF(end-of-file)，这在网络中表示对端发送了 FIN 包，要处理断连的情况；
     - 如果返回值为 -1，表示出错。

## Linux命令

- Conception：
  1. [每天一个Linux命令](https://www.cnblogs.com/peida/archive/2013/03/13/2956992.html)
- Question：
  1. **常用命令？**
     - ls、mkdir、cp
     - pwd：显示文件路径
     - chmod：修改文件权限
     - grep：正则匹配
     - netstat：网络相关信息 [详解](https://www.cnblogs.com/ggjucheng/archive/2012/01/08/2316661.html)
     - telnet：远程登陆命令
     - ln：创建文件链接
     - find：查找文件
     - rm：删除一个文件或者目录
     - df：查看磁盘使用情况
     - free：查看内存使用情况
  2. **Linux下进程相关命令？**
     - ps：查出进程号
     - top
     - kill
  3. **linux下改变文件权限的命令有哪些？**
     - chmod（change mode）
     - chgrp（change group）
     - chown
     - [讲解](https://www.cnblogs.com/cwwmmv/p/10535175.html)
  4. **如果发现系统负载过高，应该怎么排查原因，如何解决？**
     - 查看占用CPU高的进程：top
     - 查看进程下的线程：ps -mp pid -o THREAD,tid,time/ top -H -p pid
     - 查看堆栈信息：jstack -l pid > test.txt
     - [讲解](https://blog.csdn.net/weixin_39456575/article/details/113780635)
  5. **kill -9 发生了什么？**
     - kill -Signal pid
     - pid可以用ps命令查
     - kill默认-15：需要关闭，自行退出
     - -9：被终结立刻退出，强制杀死进程
