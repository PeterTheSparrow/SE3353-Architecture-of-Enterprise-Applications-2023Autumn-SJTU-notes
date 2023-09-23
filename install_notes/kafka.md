# Kafka的安装与配置

2023.09.20

by [PeterTheSparrow](www.github.com/PeterTheSparrow)

参考文章：
https://blog.csdn.net/yyx980927/article/details/132031745?spm=1001.2101.3001.6650.3&utm_medium=distribute.pc_relevant.none-task-blog-2%7Edefault%7EYuanLiJiHua%7EPosition-3-132031745-blog-117772904.235%5Ev38%5Epc_relevant_sort_base2&depth_1-utm_source=distribute.pc_relevant.none-task-blog-2%7Edefault%7EYuanLiJiHua%7EPosition-3-132031745-blog-117772904.235%5Ev38%5Epc_relevant_sort_base2&utm_relevant_index=4

## 1. 下载

直接下载了最新版的kafka。最新版本的kafka已经不需要额外安装zookeeper了。

## 2. 配置

解压文件夹。只需要修改两个配置文件：`zookeeper.properties`和`server.properties`。

这两个配置文件中，只需要修改`dataDir`和`log.dirs`两个参数即可。这两个参数代表着zookeeper和kafka的数据存储位置。

## 3. 启动

启动zookeeper

```bash
D:\softwware\kafka_2.13-3.5.1>bin\windows\zookeeper-server-start.bat config\zookeeper.properties
```

启动kafka

```bash
D:\softwware\kafka_2.13-3.5.1>bin\windows\kafka-server-start.bat config\server.properties
```