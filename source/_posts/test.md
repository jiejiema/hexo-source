---
title: Mac 安装MongoDB redis
date: 2019.3.26
tags: soft
description: 使用homebrew安装，便于维护
---

Homebrew是macOS下的软件包管理器，类似于ubuntu的apt，是使用mac系统必备的开发者工具。

## 安装

访问[Homebrew](https://brew.sh/index_zh-cn) 官网获取安装命令。
安装完成后先执行以下命令安装 curl 和 wget。

``` bash
brew install curl
brew install wget
curl --version
wget --version
```

## 常用命令 

``` bash
brew list # 列出当前已经安装的包
brew search $FORMULA # 搜索一个想安装的包
brew info $FORMULA # 列出指定包的相关信息
brew info # 显示安装了包数量，文件数量，和总占用空间
brew deps --installed --tree # 查看已安装的包的依赖，树形显示

brew install $FORMULA # 安装指定包
brew uninstall $FORMULA # 卸载指定包

brew update # 升级brew自身和源仓库
brew outdated # 列出有哪些包可以更新
brew upgrade $FORMULA # 更新指定的包
brew upgrade # 更新所有的可更新包

brew cleanup $FORMULA # 清理指定包的旧版本及安装文件
brew cleanup # 清理所有包的旧版本及安装文件
brew cleanup -n # 查看可清理的旧版本包，不执行实际操作

brew pin $FORMULA # 锁定某个包
brew unpin $FORMULA # 取消锁定

brew cask install/info/list... # 这一系列的命令用来管理以二进制方式分发的包，比如docker和oracle jdk
brew tap # 用来添加第三方源仓库，类似apt的ppa，不加参数将列出已经添加的源仓库
```

## 安装MongoDB 
安装redis 即 把 mongodb 替换为 redis
``` bash
brew install mongodb
brew services run mongodb #启动服务
brew services list  # 查看当前服务列表
```