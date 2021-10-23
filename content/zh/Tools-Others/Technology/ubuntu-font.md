---
title: "Ubuntu字体"
date: 2021-10-21T23:48:23+08:00 
type: blog
tags: ["Ubuntu","系统"]
---

#  Ubuntu 字体

## 引言

众所周知，`Ubuntu` 是一个著名的Linux开源发行版。但是，开源……这就意味着，那些不开源的字体用不了！

所以，本着~~开源~~务实的精神，我们要安装字体。（除非你想每天都被你的老师叫过去解决PPT的各种奇奇怪怪的问题）

而字体文件？当然是，Windows！~~虽然，有些blabla~~

## 复制字体

1. 如果你的网络不好，可以选择从一台安装有Windows系统的计算机进行拷贝。将 `C:\Windows\Fonts` 目录中的所有文件拷贝到移动介质中待用。
2. 如果你的网络尚可或者你身边并没有一台Windows电脑，则可以[点击这里](https://gitee.com/xu-xihe/windos-fonts)进行下载后解压。

## 安装字体

1. 移动所有字体文件致 `/usr/share/fonts/` 或者其子文件夹中。注意，如果你想要进行分类的话，可以自行新建子文件夹。
2. 修改字体文件权限，使得所有用户都可以访问，请执行 `sudo chmod -R /usr/share/fonts/{yourname} 755`。若不清楚是否执行成功，请跳过并继续。
3. 运行 `mkfontscale` 。若提示 `mkfontscale: command not found`，则先执行 `sudo apt-get install ttf-mscorefonts-installer` 后重试。
4. 运行 `mkfontdir` 和 `fc-cache -fv`。
5. 打开字体管理器，确认安装。
