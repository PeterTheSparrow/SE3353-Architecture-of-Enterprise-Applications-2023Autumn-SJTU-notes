# Redis

2023.10.09

不想用linux虚拟机，所以使用了WSL2（ubuntu22.04）来安装redis。

参考：[官方文档：WSL2安装redis](https://redis.io/docs/getting-started/installation/install-redis-on-windows/)

高（sha3）贵（bi1）的windows！

## install redis

```bash
curl -fsSL https://packages.redis.io/gpg | sudo gpg --dearmor -o /usr/share/keyrings/redis-archive-keyring.gpg

echo "deb [signed-by=/usr/share/keyrings/redis-archive-keyring.gpg] https://packages.redis.io/deb $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/redis.list

sudo apt-get update
sudo apt-get install redis
```

## run redis

```bash
sudo service redis-server start
```

跑起来居然是这个死样子，没有显示redis的图标，我还以为挂了呢：

```bash
cdm@DESKTOP-FK33F9A:/$ sudo service redis-server start
Starting redis-server: redis-server.
cdm@DESKTOP-FK33F9A:/$ sudo service redis-server status
 * redis-server is running
```

## connect to redis

```bash
cdm@DESKTOP-FK33F9A:/$ redis-cli
127.0.0.1:6379> ping
PONG
127.0.0.1:6379>
```

可以看出：
- Redis 服务器默认监听本地主机（127.0.0.1）上的端口 6379，这是为了提供本地访问，并确保安全性。

## shutdown redis

方法：
- 通过redis-cli连接服务器后执行shutdown命令，则执行停止redis服务操作。

```bash
cdm@DESKTOP-FK33F9A:/$ sudo service redis-server status
[sudo] password for cdm:
 * redis-server is running
cdm@DESKTOP-FK33F9A:/$ redis-cli
127.0.0.1:6379> shutdown
not connected>
cdm@DESKTOP-FK33F9A:/$ sudo service redis-server status
 * redis-server is not running
```