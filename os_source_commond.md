## linux 查看硬件配置方面的一些命令

#### 系统：

1. uname -a 
	 查看内核/操作系统/CPU信息

2. head -n 1 /etc/issue
	/etc/issue 文件中存放的是linux版本信息

3. cat /proc/cpuinfo
	查看CPU信息

4. hostname
	计算机名字


#### 资源：

1. du -sh [目录名]
	查看指定目录的大小

2. grep MemTotal /proc/meminfo 
	查看内存总量

3. grep MemFree /proc/meminfo 
	查看空闲内存量

4. grep MemAvailable /proc/meminfo 
	查看空闲内存量

5. uptime
	查看系统运行时间、用户数、负载

#### 网络：

1. netstat -lntp 
	查看所有监听端口

#### 进程：
1. ps -ef
	查看所有进程


2. top
	实时显示进程状态

#### 用户：
1. cut -d: -f1 /etc/passwd
	查看系统所有用户

2. cut -d: -f1 /etc/group
	查看系统所有组

#### 服务：
1. chkconfig --list
	列出所有系统服务

2. chkconfig --list | grep on
	列出所有启动的系统服务

#### 程序
1. rpm -qa | grep xxx
	查看所有安装的软件包












