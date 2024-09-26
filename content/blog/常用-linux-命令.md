---
title: 常用 linux 命令
date: 2024-09-26T07:30:50.607Z
---

## 1. 上传和下载
### 1.1 上传

scp -p 22 xxx.tar  kd@1.1.1.1:/xx/xx


### 1.2 下载
scp -p 22 kd@1.1.1.1:/xx/xx  /abc/cd



## 2 压缩与解压
### 2.1 gunzip 

 gunzip 2023*/*.gz

### 2.2 tar

#### 2.2.1 tar 压缩和解压
tar cvf  xxx.tar xxxx

tar xvf   xxx.tar 


## 3.  find 查找关键字
find . -type f -print0 | xargs -0 grep -l 'EAP-Type-Identity'

## 4.  创建分组 用户
 groupadd abc
useradd -g abc -d /run/abc  -s /usr/bin/bash -m  user1
passwd user1

### 4.1 修改目录所有者
chown -R user1:abc /run/abc


## 5. ssh 连接
ssh -p 22 user1@1.1.1.1



## 6. tcpdump 抓包

#### 6.1 写日志
tcpdump  -xx -i  eth0 -vnn udp -w ./xxx.cap

tcpdump -s 0 -xx -i  eth0 -vnn udp -w ./xxxxx.cap


#### 6.2 抓地址和协议 打印出来

tcpdump  -xx -i  eth0 -vnn udp and host 11.1.1.1


tcpdump -i eth0 host 1.1.1.1 -w ./xxx.cap









