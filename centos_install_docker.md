# centos系统升级docker版本教程

####1. 备份数据卷，容器，镜像
	简单的说就是挂载路径，以及/var/lib/docker/路径下的所有东西都备份。/var/lib/docker/路径下，容器，镜像，网络配置等等一系列的东西都在这下面。
	cp -r source_path target_path

####2. stop　docker 
	192.168.61.91上采用 kill -9 pid

####3. uninstall docker
	1) sudo yum list installed | grep docker
	
	2) 将以上命令的执行结果删除掉：
		sudo yum remove -y .....

####4. install docker
	1) add repo在路径/etc/yum.repo.d/docker.repo
		[dockerrepo]
		name=Docker Repository
		baseurl=https://yum.dockerproject.org/repo/main/centos/7/
		enabled=1
		gpgcheck=1
		gpgkey=https://yum.dockerproject.org/gpg

	2) sudo yum update　根据内核是否满足条件(大于等于3.10)执行该操作

	3) sudo yum install docker-engine

####5. start docker
	systemctl docker start
