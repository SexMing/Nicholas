# 如何设置dns永久有效

#### 1. 修改network配置文件(/etc/network/interfaces)


1) 将DNS信息直接添加到网卡配置文档里

>　iface eth0 inet static 
>    address 192.168.0.100 
>    netmask 255.255.255.0 
>    gateway 192.168.0.1 
>    dns-search example.com 
>    dns-nameservers 192.168.0.1 8.8.8.8 

2) 重启networking服务后即可正常访问
> 	sudo /etc/init.d/networking restart 


-------------

#### ２. 修改/etc/resolvconf/resolv.conf.d/head文件

在该文件的最下面添加两行
> nameserver:192.168.61.91
> nameserver:114.114.114.114

> resolvconf -u

还有问题求助　
> man resolvconf 