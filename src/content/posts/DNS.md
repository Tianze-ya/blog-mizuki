---
title: 加速器无法访问Github
published: 2024-12-01
description: 解决加速器无法访问Github
image: ./cover.jpg
tags:
  - 网络
category: 教程
draft: false
pinned: false
lang: zh-CN
---

# 简介
解决加速器无法访问Github

# 一键脚本
```bash
echo "nameserver 114.114.114.114" | sudo tee -a /etc/resolv.conf

printf "\
199.232.68.133 raw.githubusercontent.com\n\
199.232.68.133 user-images.githubusercontent.com\n\
199.232.68.133 avatars2.githubusercontent.com\n\
199.232.68.133 avatars1.githubusercontent.com\n" | sudo tee -a /etc/hosts
```