---
layout: post
title: 如何利用Socks5代理加速github访问
date: 2020-03-11 15:15:42 +0800
categories: blog
tags: [tricks,Network]
comments: true
---

# 如何利用Socks5代理加速github访问
## 前提条件
已经有socks5代理，有密钥
## 方法
在密钥目录添加config文件，加入如下内容

```
# github
Host github.com
ProxyCommand connect -H 127.0.0.1:3737 %h %p  # 3737 is my port number
HostName %h
Port 22
User git
IdentityFile  ~/.ssh/id_rsa 
IdentitiesOnly yes
```