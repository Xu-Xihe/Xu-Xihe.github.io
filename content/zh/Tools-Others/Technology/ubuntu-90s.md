---
title: "Ubuntu关机1min30s"
date: 2021-10-21T23:24:13+08:00
type: blog
tags: ["Ubuntu","系统"]
---

# Ubuntu关机1min30s

通常情况下，他会显示一个啥啥啥 is running，然后后面有一个括号 `(..s/1min30s)` 这种。

## 解决方法

虽然我们并不知道为啥，但是我们确实有一种解决的方法。

1. 用root权限（其实就是加个 `sudo`）编辑 ` /etc/systemd/system.conf`，找到里面有一个 `DefaultTimeoutStopSec=90s`，把行首的 `#` 去掉，并改成 `DefaultTimeoutStopSec=1ms`，保存，退出。
2. 执行 `sudo systemctl daemon-reload` 更新配置文件。
