mydocker 是一个用go+cgo编写的容器，出于个人兴趣用来学习docker的原理。

本人编译及运行环境：
- go 1.13
- ubuntu 14.04/19.01
- rootfs 放到 /root/rootfs/下面

rootfs 可以放到自己喜欢的路径下，确保代码中的path和此路径一致即可，每个发行版的rootfs也会有些许差异。

查看帮助：
```bash
go build -mod=vendor .
sudo ./mydocker -h
```

增加namespace，进行资源的隔离

增加cgroup，进行资源的限制(memory,cpu,cpuset)

增加aufs包装镜像

增加卷挂载支持

增加容器简单打包(commit)

增加容器后台运行(-d)

增加查看容器(ps)

增加进入容器(exec)

增加容器终止(stop)

增加删除容器(rm)

增加开始容器(start)

隐藏init命令(cobra->cli)