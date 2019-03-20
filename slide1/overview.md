
# 后端总览 

## 网络
* 网络协议的分层

### OSI model
<img src="./assets/OSI-Model.jpg" width="640">


### 网络协议的编码
<img src="./assets/IPS data encapsulation.png" width="640">

### big and little endian

<img src="./assets/big and little endian.png" width="640">


### 网络协议分类:
* 文本协议 (http)
    * <img src="./assets/HTTP_RequestMessageExample.png" width="640">
* 二进制协议 (tcp, grpc)



## 操作系统
* Protection ring:
* system call:
* 端口号:
    * 前1024个端口号是系统占用的, 后面可以用户自己去领, 不需要sudo权限

* 进程
    * 僵尸进程: 父进程关闭没有正确回收子进程

* 线程
    * race condition:

* 执行文件

* IO
    * poll
    * epoll

* sockets
* 环境变量


### protection ring

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/2/2f/Priv_rings.svg/1920px-Priv_rings.svg.png" width="640">


### system call

<img src="./assets/what is system call.png" width="640">

应用程序请求网络

<img src="./assets/system-call.png" width="640">



### sockets (套接字):

sockets 使用来创建网络连接的一个关键, 目前基本上所有的网络连接都是基于TCP和UDP的. 操作系统底层实现了sockets
的基本实现. 基于TCP/UDP协议上层实现的协议都是用sockets来实现的. programming sockets 的关键就是ip + port + 
协议类型.
然后可以通过 byte stream 来操作数据.

### 环境变量
环境变量一种可以被应用程序感知的机制, 系统的进程基本上都是由其他进程fork出来的, 子进程自动继承父进程的环境变量.

```
export ANDROID_SDK_ROOT=$HOME/workspace/tools/android_sdk
export PATH=$ANDROID_SDK_ROOT/tools:$ANDROID_SDK_ROOT/platform-tools:$PATH

// 
NODE_ENV=PRODUCTION node app.js

// 
process.env.NODE_ENV
```


## 虚拟化

* docker
* traditional virtualization


## 架构 
* 后端常用架构
    * https://www.digitalocean.com/community/tutorials/5-common-server-setups-for-your-web-application

* 微服务
* monolithic 

## 数据库
* SQL:
    * mysql, 

* NoSQL:
    * mongodb, redis

## 其他

* 缓存
    * 客户端缓存
        * http, cache api (就browser环境来说)
    * 服务端缓存
        * 静态页面缓存
        * 数据库缓存
        * 动态数据缓存

* RPC (remote procedure call)

* 消息队列

* 网关
    * https://blog.risingstack.com/building-an-api-gateway-using-nodejs/
    
* 代理

## reference 

* book: *Attacking.Network.Protocols.2017.12*