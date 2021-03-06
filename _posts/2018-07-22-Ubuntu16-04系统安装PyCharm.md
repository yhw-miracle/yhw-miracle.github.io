---
layout: post
title: Ubuntu16.04系统安装PyCharm
date: 2018-07-22 00:00:00 +0800
tags: [ubuntu, pycharm]
categories: 问题解决
author: 痛点就是起点
---

> 本文为`痛点就是起点`原创文章，可以随意转载，但需注明出处。

随着人工智能的发展，python 越来越流行。作为年轻一代的互联网技术人员，学习 python 就变得十分必要。俗话说，“工欲善其事必先利其器”，在学习 python 之前，一个好的 IDE 将会使编程效率得到大幅度提高。本人在进行 python 开发时，强烈建议 pycharm 编辑器。

### pycharm
pycharm 主要分为专业版和社区版，专业版是收费的，有 30 天试用期，当然专业版功能非常强大；而社区版是免费的，是专业版的阉割版，但基本上可以满足学习和开发的需要。pycharm 具有跨平台性，可以在 windows、linux、mac系统下使用。其官方链接为 [PyCharm](https://www.jetbrains.com/pycharm/) 。

### 安装过程
pycharm 安装十分简单，windows 系统下只需要简单的一路“next”，即可成功安装。本人以 pycharm 社区版在 Ubuntu 16.04 系统安装为例，介绍其安装过程。首先介绍一种最简单的安装方式，只需要两条命令即可，分别为:

```bash
sudo add-apt-repository ppa:mystic-mirage/pycharm
```

![](images/2018/XR6zLENFy4WAZlVAFkwFV3zs.png)


```bash
sudo apt-get install pycharm-community
```

这种方式可能由于镜像源的问题，我在安装时网速很慢，安装进程严重耽误，故我放弃这种安装方式，采用官网安装包解压安装的方式。

* 首先在官网上下载 pycahrm 在 linux 系统的软件包。

* 下载完 pycharm 安装包后，如图所示，将其解压到 Linux 系统下某个路径下，这里我是解压到 /usr/local/ 目录下。
解压命令为：

```bash
sudo tar -zxvf pycharm-community-2018.1.4.tar.gz -C /usr/local/
```

![](images/2018/Db_FgbgW3ailrm2teuaryPNr.png)

![](images/2018/zn8Nlp40rVrJz_opjSBIM4Nw.png)


* 进入到 /usr/local/pycharm-community-2018.1.4/bin/ 目录下，运行 pycharm.sh 文件即可打开 pycharm 查询，首次运行会弹出初始设置界面，只要进行相应的设置即可。相应的 linux 命令为：

```bash
cd /usr/local/pycharm-community-2018.1.4/bin/
./pycharm.sh
```

![](images/2018/8e9jpPJWpDD2oPHIjE8vc9dS.png)

![](images/2018/veNihRw8WdrlX_33KfW2Tw0J.png)


* 以上过程完成后，恭喜你，你已经完成 pycharm 在 Ubuntu 16.04 系统下的安装，可以使用 pycharm 编辑器了。但是，以上步骤有一个问题，就是每次启动 pycharm 时都需要在 Terminal 运行 ./pycharm.sh 命令，有没有可以直接点击桌面图标，像 windows 系统那样便捷启动方式？答案是有的。这需要在 /usr/share/applications/ 下创建 pycharm 的快捷方式 pycharm.desktop（姑且这么理解吧），然后在 pycharm.desktop 文件下键入以下内容，启动 pycarm 时，右键将其锁定在桌面上。创建快捷方式的命令是：

```bash
sudo gedit /usr/share/applications/pycharm.desktop
```

![](images/2018/Y0YSUQcPIsaeHBNBj9pHlbJ0.png)

![](images/2018/WeijxqZPKha2rOoCtuNFxGIf.png)


现在，你可以在 Ubuntu 16.04 系统下尽情享受 pycharm 编辑器了。
