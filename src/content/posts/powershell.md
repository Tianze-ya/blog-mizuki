---
title: PowerShell7的配置
published: 2025-12-06
description: 跨平台命令行自动化工具
image: ./cover.jpg
tags:
  - 工具
category: 软件
draft: false
pinned: false
lang: zh-CN
---

# 简介
PowerShell 7 是微软开发的跨平台命令行工具，基于.NET Core构建，支持Windows、Linux和macOS系统。它提供了强大的自动化脚本功能、对象管道处理、丰富的模块生态系统，是系统管理和DevOps的重要工具。

# 使用
[Github](https://github.com/PowerShell/PowerShell)
下载
```bash
winget install --id Microsoft.PowerShell --source winget
```
配置文件`$PROFILE`

# 配置
`settings.json`
```json
{
    "$help": "https://aka.ms/terminal-documentation",
    "$schema": "https://aka.ms/terminal-profiles-schema",
    "actions": 
    [
        {
            "command": 
            {
                "action": "copy",
                "singleLine": false
            },
            "id": "User.copy.644BA8F2"
        },
        {
            "command": "paste",
            "id": "User.paste"
        },
        {
            "command": 
            {
                "action": "splitPane",
                "split": "auto",
                "splitMode": "duplicate"
            },
            "id": "User.splitPane.A6751878"
        },
        {
            "command": "find",
            "id": "User.find"
        }
    ],
    "alwaysShowNotificationIcon": false,
    "copyFormatting": "none",
    "copyOnSelect": true,
    "defaultInputScope": "alphanumericHalfWidth",
    "defaultProfile": "{574e775e-4f2a-5b96-ac1e-a2962a402336}",
    "experimental.detectURLs": true,
    "focusFollowMouse": false,
    "initialCols": 80,
    "initialRows": 20,
    "keybindings": 
    [
        {
            "id": "User.copy.644BA8F2",
            "keys": "ctrl+c"
        },
        {
            "id": "User.find",
            "keys": "ctrl+shift+f"
        },
        {
            "id": "User.paste",
            "keys": "ctrl+v"
        },
        {
            "id": "User.splitPane.A6751878",
            "keys": "alt+shift+d"
        }
    ],
    "newTabMenu": 
    [
        {
            "type": "remainingProfiles"
        }
    ],
    "profiles": 
    {
        "defaults": 
        {
            "backgroundImage": "E:/mine/photo/background/20221005201441886.jpg",
            "backgroundImageOpacity": 0.5,
            "colorScheme": "One Half Dark",
            "experimental.retroTerminalEffect": false,
            "font": 
            {
                "face": "Maple Mono NL NF CN",
                "size": 15,
                "weight": "semi-light"
            },
            "opacity": 20,
            "padding": "8",
            "suppressApplicationTitle": true,
            "useAcrylic": true
        },
        "list": 
        [
            {
                "guid": "{574e775e-4f2a-5b96-ac1e-a2962a402336}",
                "hidden": false,
                "name": "PowerShell",
                "source": "Windows.Terminal.PowershellCore",
                "startingDirectory": "E:\\workspace"
            },
            {
                "commandline": "%SystemRoot%\\System32\\cmd.exe",
                "guid": "{0caa0dad-35be-5f56-a8ff-afceeeaa6101}",
                "hidden": false,
                "name": "Commnd",
                "startingDirectory": "E:\\workspace"
            }
        ]
    },
    "schemes": [],
    "showTabsInTitlebar": true,
    "showTerminalTitleInTitlebar": true,
    "tabWidthMode": "equal",
    "themes": [],
    "useAcrylicInTabRow": true,
    "windowingBehavior": "useAnyExisting"
}
```



# oh-my-posh
[Home | Oh My Posh](https://ohmyposh.dev/)
```bash
winget install JanDeDobbeleer.OhMyPosh --source winget
```


配置文件中添加
```
oh-my-posh init pwsh | Invoke-Expression
```

*推荐主题：powerlevel10k_rainbow*
# 模块 
## PSCompletions
```bash
Install-Module PSCompletions -Scope CurrentUser
scoop bucket add abyss https://github.com/abgox/abyss
scoop install abyss/sigoden.Argc-completions
```
配置文件中添加
```
Import-Module PSCompletions
```


### 巧思
