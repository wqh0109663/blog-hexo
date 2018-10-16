---
title: Ubantu16.04使用日记
date: 2018-09-13 23:08:01
tags:
    - Ubantu16.04 
    - linux
categories: Ubantu16.04
---
## 第二次安装ubantu，我装了些什么软件

### git
### Oraclejdk
  - sudo add-apt-repository ppa:webupd8team/java
  - sudo apt-get update
  - sudo apt-get install oracle-java8-installer

### maven
  - <localRepository>/home/wqh/repo</localRepository>
  - 在mirrors标签中添加
  ```
  <mirror>
    <id>nexus-aliyun</id>
    <mirrorOf>*</mirrorOf>
    <name>Nexus aliyun</name>
    <url>http://maven.aliyun.com/nexus/content/groups/public</url>
  </mirror>
  ```

### nginx
### tmux终端复用
### oh my zsh
  - 安装zsh
  - 再安装ohmyzsh
  ```
   sh -c "$(wget https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"
  ```
  - 插件的安装
    -  [zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions/blob/master/INSTALL.md)
    - [zsh-syntax-highlighting](https://github.com/zsh-users/zsh-syntax-highlighting/blob/master/INSTALL.md)
    - web-search  、sublime 、 z ，在~/.zshrc文件中添加

### BaiduPc-GoBaidu网盘
  - 先安装go语言环境
  ```
  sudo apt-get install python-software-properties
  sudo add-apt-repository ppa:gophers/go
  sudo apt-get update
  sudo apt-get install golang-stable git-core mercurial
  export GOROOT=/usr/local/go
  export GOBIN=$GOROOT/bin
  export PATH=$PATH:$GOBIN
  export GOPATH=$HOME/gopath (可选设置)
  ```
  - [下载地址](https://github.com/iikira/BaiduPCS-Go/releases)

### hexo搭建博客
  - [官网地址](https://hexo.io/zh-cn/index.html)
  - 安装nodejs环境
  - [安装参考地址](https://blog.csdn.net/y5492853/article/details/79529410)

### mysql
### mongodb
### shadowsocks-qt5翻墙必备
  - sudo add-apt-repository ppa:hzwhuang/ss-qt5

### wps的安装和其他
uGet，网易云，virtualbox，shutter，webstorm，clion，pycharm，从官网下载idea

### 安装谷歌浏览器 [博客地址](https://blog.csdn.net/qq_30164225/article/details/54632634)
### 系统监视器
  - sudo add-apt-repository ppa:fossfreedom/indicator-sysmonitor
  - sudo apt-get update
  - sudo apt-get install indicator-sysmonitor
  - net：{net}
### markdown 编辑器
  1.  atom
  2.  typora的安装
    - sudo add-apt-repository 'deb https://typora.io ./linux/'
    - update，然后install typora

### 另外还有
了xmind ，sougou输入法，workbench MySQL客户端（直接再ubantu软件中心下载） ，vim ，tree ， electric-wechat 软件中心下载

###  解压软件 ： rar unrar ,p7zip convmv
