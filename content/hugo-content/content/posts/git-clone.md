---
title: "如何克隆 GitHub 仓库 | How to Clone a GitHub Repository"
date: 2026-04-24
draft: false
tags: ["Git", "Clone", "克隆", "教程"]
description: "详细讲解如何使用 git clone 命令将 GitHub 仓库复制到本地电脑。Learn how to use git clone to copy a GitHub repository to your local computer."
---

## 什么是克隆？| What is Cloning?

克隆（Clone）就是将 GitHub 上的远程仓库完整复制一份到你的本地电脑，包括所有文件和历史记录。

Cloning means copying a remote GitHub repository to your local machine — including all files and history.

---

## 找到仓库地址 | Find the Repository URL

1. 打开你要克隆的 GitHub 仓库页面
2. 点击绿色的 **Code** 按钮
3. 选择 **HTTPS** 标签
4. 复制地址（格式如 `https://github.com/username/repo.git`）

---

## 执行克隆命令 | Run the Clone Command

打开终端（Terminal / PowerShell），进入你想存放项目的目录，然后运行：

```bash
git clone https://github.com/username/repository-name.git
```

例如克隆 Vue.js 官方仓库：

```bash
git clone https://github.com/vuejs/vue.git
```

---

## 克隆到指定文件夹 | Clone into a Specific Folder

默认会创建与仓库同名的文件夹，如果想自定义文件夹名：

```bash
git clone https://github.com/username/repo.git my-folder-name
```

---

## 克隆后的目录结构 | After Cloning

克隆完成后，进入项目目录：

```bash
cd repository-name
```

查看文件列表：

```bash
ls        # Mac/Linux
dir       # Windows
```

---

## SSH vs HTTPS 克隆方式

| 方式 | 优点 | 缺点 |
|------|------|------|
| HTTPS | 简单，无需配置 | 每次需要输入密码 |
| SSH | 配置后免密操作 | 需要提前配置 SSH Key |

新手推荐使用 **HTTPS**，熟悉后再配置 SSH。

Beginners should use **HTTPS**. Set up SSH later for convenience.

---

## 常见错误 | Common Errors

**`Permission denied (publickey)`**  
说明你在用 SSH 但没有配置 SSH Key，换用 HTTPS 地址即可。

**`Repository not found`**  
检查 URL 是否正确，或者私有仓库需要先登录授权。

---

## 下一步 | Next Steps

- [学习基础 Git 命令](/posts/git-commands/)
- [将本地修改推送回 GitHub](/posts/git-push/)
