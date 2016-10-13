# SuitAgent-UpdateToole

### 用途

SuitAgent局域网升级工具，用于让用户更加方便的在[SuitAgent](:https://github.com/cqyijifu/OpenFalcon-SuitAgent)不在互联网环境时的升级。



### 怎么使用

该项目下有一个二进制文件：`suitAgentUpdateTool`，这是用Go开发的二进制文件，运行环境为`Linux 64 位`环境。把它放入局域网中，**能联网的机器上**运行

```sh
./suitAgentUpdateTool
```



即可。默认端口是`9090`。也可以指定一个端口:

```sh
./suitAgentUpdateTool -port=8080
```

运行后，终端会输出如下的信息：

```sh
[root@test opt]# ./suitAgentUpdateWebServer
download file to /tmp/SuitAgentTemp/update.zip
======================================================
Choose One Url To Set SuitAgent Update Url :
http://192.168.46.22:9090/update.zip
http://172.17.42.1:9090/update.zip
======================================================
```



然后只需要把输出的下载路径，选取一个合适的，配置到`SuitAgent`中即可。



### 运行过程



运行`suitAgentUpdateTool` -> 自动下载最新的升级包到临时目录 -> 启动web服务提供下载服务

