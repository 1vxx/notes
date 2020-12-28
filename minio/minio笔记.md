# Minio 笔记

> 1V



#### 官网

[https://docs.min.io/cn/]: 

#### 存放目录

选取一个盘，创建一个文件存放目录

#### 启动命令

```
minio.exe server X:\minioServer
```

```
windows后台启动： start /min minio.exe server X:\minioServer
```

#### Windows bat 启动示例

```
@echo off
title open-minio
set ENV_HOME="D:\Program Files\minio"
D:
color 0a
cd %ENV_HOME%
start /min minio.exe server X:\minioServer
```