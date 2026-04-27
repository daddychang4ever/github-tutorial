---
title: "如何安装 Git | How to Install Git"
date: 2026-04-26
draft: false
tags: ["Git", "安装", "Windows", "Mac", "Linux"]
description: "详细介绍在 Windows、Mac、Linux 系统上安装和配置 Git 的完整步骤。Step-by-step guide to installing and configuring Git on Windows, Mac, and Linux."
---

## 什么是 Git？

Git 是一个免费的开源**版本控制系统**，GitHub 正是基于 Git 运作的。在使用 GitHub 之前，你需要先在本地安装 Git。

## What is Git?

Git is a free, open-source **version control system** that powers GitHub. Before using GitHub locally, you need to install Git on your machine.

---

## Windows 安装 | Installing on Windows

1. 访问 [git-scm.com](https://git-scm.com/download/win)
2. 下载 Windows 安装包（自动识别64位/32位）
3. 运行安装程序，全部保持默认设置，一路 Next
4. 安装完成后打开 **PowerShell** 验证：

```bash
git --version
```

看到类似 `git version 2.x.x` 即表示安装成功。

---

## Mac 安装 | Installing on Mac

打开终端（Terminal），运行：

```bash
xcode-select --install
```

或者使用 Homebrew：

```bash
brew install git
```

---

## Linux 安装 | Installing on Linux

Ubuntu / Debian：

```bash
sudo apt-get update
sudo apt-get install git
```

CentOS / Fedora：

```bash
sudo yum install git
```

---

## 配置 Git 身份 | Configure Your Identity

安装完成后，必须设置你的用户名和邮箱（这会出现在每次提交记录中）：

After installation, set your name and email (they appear in every commit):

```bash
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```

验证配置 | Verify configuration:

```bash
git config --list
```

---

## 常见问题 | FAQ

**Q: 安装后命令不识别怎么办？**  
A: 关闭当前终端窗口，重新打开一个新窗口再试。

**Q: After install, command not found?**  
A: Close your terminal and open a new one. The PATH needs to refresh.

---

## 下一步 | Next Steps

- [学习基础 Git 命令](/posts/git-commands/)
- [将本地项目推送到 GitHub](/posts/git-push/)
