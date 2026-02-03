---
title: Scoop
published: 2025-12-06
description: Windows命令行软件包管理器
image: ./cover.jpg
tags:
  - 工具
category: 软件
draft: false
pinned: false
lang: zh-CN
---

# 简介
✦ Scoop 是一个专为 Windows 系统设计的命令行软件包管理器，类似于 macOS 上的 Homebrew 或 Linux 上的apt。它让用户能够轻松地从命令行安装、更新和管理各种开发工具和应用程序，无需手动下载和配置。Scoop 的主要特点包括：

* 简单易用：通过简单的命令如 scoop install package 即可安装软件
* 自动管理 PATH：安装的软件会自动添加到系统环境变量
* 版本控制：可以轻松切换软件的不同版本
* 社区维护：拥有丰富的软件仓库和活跃的社区支持
* 无需管理员权限：默认安装到用户目录，避免权限问题

✦ Scoop 特别适合开发者快速搭建开发环境，常用的命令包括 scoop search（搜索软件）、scoop update（更新软件）和 scoop uninstall（卸载软件）

# 下载
```bash
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
Invoke-RestMethod -Uri https://get.scoop.sh | Invoke-Expression
```

# 使用aiar
```bash
scoop install aria2
```

取消下载时的警告
```bash
scoop config aria2-warning-enabled false
Add-Content $PROFILE '$env:PATH += ";C:\Users\tianze\scoop\shims"'
```

