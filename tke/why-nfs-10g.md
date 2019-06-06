# 挂载的nfs为何是10G

### 挂载方式

集群创建的时候在控制台上设置

![](images/tke-mount-nfs.png)

挂载成功之后，容器和node节点看到的大小都为10G

### 具体原因

nfs的盘，默认的挂载大小为10G，支持自动扩容

### 扩容方式

<1T，容量到50%触发自动扩容，每次加100G; >1T,到80%触发自动扩容。每次加500G

### 收费方式

计费是根据实际的使用量，小于10G不收费，多于10G开始收费