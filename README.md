# SE3353-Architecture of Enterprise Applications-2023秋

2023年秋季上海交通大学软件学院课程应用系统体系架构（SE3353）笔记。

## 关于仓库

1. 本仓库分为如下几个部分：
   - **install_notes**：安装核弹的记录（os:windows10）
   - **notes**：第一部分 服务器端应用程序开发
   - **notes_database**： 第二部分 数据库
   - **notes_operation_and_maintenance**：第三部分 运维
   - release.pdf：最终版本的pdf，可以直接下载拿去考试
   - WebApplicationDevelopment：互联网应用开发技术的相关笔记（本课程的前置课程，包含一定私货，仅放置于此）
2. 本笔记在编写的时候，第一部分后端相关内容和第二部分数据库相关内容不少是在[2022-2023-1-Application-System-Architecture](https://github.com/Musicminion/2022-2023-1-Application-System-Architecture)的基础上进行编写的，征得原作者同意。在此向其致以诚挚的谢意！
3. 作者水平有限，并且很多内容也是上课仓促记录或者是飞书转文字，因此难免差错；如果存在知识点的错误，欢迎指正
4. **任何转载请引用本仓库**！**严禁用于商业用途**！
5. 仅供学习使用；如果您认为存在侵权，请联系我


## 关于课程

### 课程内容

企业级应用系统体系架构，包括三个部分：
1. 服务器端应用程序开发
   1. 架构与实例池管理 
   2. 异步通信：Kafka消息中间件
   3. 异步通信：web socket
   4. 事务管理
   5. 数据库事务管理
   6. java多线程编程
   7. 分布式缓存
   8. 全文搜索
   9. web服务
   10. 微服务架构
2. 数据库进阶
   1. 数据库设计
   2. MySQL索引与缓存管理
   3. MySQL备份与恢复
   4. MySQL分区
   5. NoSQL数据库1-MongoDB
   6. NoSQL数据库2-Neo4j
   7. NoSQL数据库3-VectorDB & LSM
   8. NoSQL数据库4-TSDB(influxDB)
   9. 云数据库：GaussDB
   10. 数据湖
3. 系统部署与运维
   1. 集群部署
   2. 云计算
   3. graphql
   4. 容器化
   5. 分布式并行处理框架1-Hadoop
   6. 分布式并行处理框架2-Spark
   7. 分布式并行处理框架3-Storm
   8. 分布式并行处理框架4-分布式文件系统
   9. 分布式并行处理框架5-分布式数据库HBase
   10. 分布式并行处理框架6-分布式数据仓库Hive
   11. 分布式并行处理框架7-flink

### 考核

1. 期末考试：40%
2. 平时作业：5% * 12  = 60%

笔者本课程得分：

| 期末考试 | 平时作业 | 总分 |
| -------- | -------- | ---- |
| 91/100 | 59.5/60 | 96 |

考核本身是全开卷；资料要自己准备；但是打印slides意义其实并不大，因为其中冗余信息较多（例如code），考试主要考应用系统体系架构的设计思想，而不是代码的实现（coding的部分体现在平时作业中）；很多考点也出自板书，slides上无处可寻；同时，slides的量非常大，检索起来极为困难。

因此笔者编写了这套笔记；这套笔记基本涵盖了所有的考点（今年所有考题几乎全部命中）；既可以作为**考试的开卷材料**，同时也可以作为**课程配套讲义**使用。