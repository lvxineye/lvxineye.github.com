title: 搭建Ubuntu服务器下的Java,Play Framework,Scala环境
date: 2015-03-25 17:14:09
categories: Server
tags: [Mac OSX,Ubuntu,Java,Scala,Play Framework,Postgresql]
---

在Mac OSX下如何在Terminal下部署Ubuntu服务器。前提是已经申请好Ubuntu服务器空间。

- 进入服务器

```
$ ssh -i [ssh-key 文件目录] root@ipaddress
```

- 安装解压工具**unzip**

```
$ apt-get install unzip
```

- 安装**openJDK**

```
$ sudo apt-get install openjdk-6-jdk
```

- 设置**jdk**环境变量

```
$ java -version
$ echo $JAVA_HOME
$ sudo echo export JAVA_HOME="/usr/lib/jvm/java-7-openjdk-amd64/" >> ~/.bashrc
$ source ~/.bashrc
$ echo $JAVA_HOME
$ javac (确认安装成功)
```

- 安装**Scala**

```
$ apt-get install scala
```

- 下载**Play!**压缩包

```
1. 从 http://www.playframework.com/download 获取一个需要安装版本(e.g. 2.1.4的地址：http://downloads.typesafe.com/play/2.1.4/play-2.1.4.zip)

2. $ wget http://downloads.typesafe.com/play/2.1.4/play-2.1.4.zip
```

- 解压**Play!**

```
$ unzip play-2.1.4.zip
$ mv play-2.1.4 /opt/
```

- 确认**Play!**是否可用

```
$ cd /opt/play-2.1.4/
$ ./play
```

- 设置**Play!**全局变量

```
$ ln -s /opt/play-2.1.4/play /usr/local/bin/
```

- 安装**git**

```
$ apt-get install git
```

- 安装**PostgreSQL**

```
$ apt-get install postgresql-9.1
**输入postgresql后按tab键列出所有可安装版本**
```

- 创建**PostgreSQL**的用户和数据库

```
$ psql -U postgres postgres
$ CREATE USER [username] WITH PASSWORD 'password'
$ CREATE DATABASE [dbname] WITH OWNER [username]
```
