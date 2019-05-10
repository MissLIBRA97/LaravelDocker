# LaravelDocker
Dev environment docker for laravel with NGINX, MySQL and PHP.

为laravel编排的docker。包含nginx mysql php phpmyadmin。
<!-- TOC -->

- [LaravelDocker](#laraveldocker)
- [1. 配置要求：](#1-配置要求)
- [2. 安装：](#2-安装)
    - [修改参数文件](#修改参数文件)
    - [安装](#安装)
    - [开始使用](#开始使用)
- [3. 使用：](#3-使用)
    - [3.1. 启动：](#31-启动)
    - [3.2. 停止：](#32-停止)
- [4. 疑难杂症：](#4-疑难杂症)

<!-- /TOC -->
# 1. 配置要求：
    docker环境
# 2. 安装：

> git clone https://github.com/MissLIBRA97/LaravelDocker.git

## 修改参数文件

    > cd bin && cp env-example .env
    > cd bin && copy env-example .env (Windows)

windows 需要将 .env 文件中

    > COMPOSE_PATH_SEPARATOR=:

改为

    > COMPOSE_PATH_SEPARATOR=;

mysql默认安装最新版本 需要修改版本的 需要在.env中修改：

    > MYSQL_VERSION=X.X

mysql默认账户密码：

> default：secret

mysql默认账户：

> root：root

## 安装

    > docker-compose up --build -d

若期间有错 排除错误后重新运行即可。
安装配置过程大约需要十分钟。

## 开始使用

网站目录在 ./local
使用php artisan等php命令时 请先进入workspace容器
workspace容器默认挂载了./local目录

    > docker-compose exec workspace bash

# 3. 使用：

## 3.1. 启动：

在./bin/目录下运行：

    > docker-compose up -d

## 3.2. 停止：

在./bin/目录下运行：

    > docker-compose down


# 4. 疑难杂症：

