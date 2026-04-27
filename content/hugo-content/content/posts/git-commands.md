---
title: "10个必学的 Git 命令 | 10 Essential Git Commands"
date: 2026-04-25
draft: false
tags: ["Git", "命令", "Commands", "教程"]
description: "新手必须掌握的10个 Git 命令，附带中英文说明和实际示例。10 essential Git commands every beginner must know, with examples."
---

## 为什么要学 Git 命令？

虽然有很多 Git 图形界面工具，但掌握命令行操作能让你更高效、更灵活地使用 Git。

## Why Learn Git Commands?

While GUI tools exist, knowing the command line makes you faster and more flexible.

---

## 1. `git init` — 初始化仓库

在当前目录创建一个新的 Git 仓库。

Initialize a new Git repository in the current directory.

```bash
git init
```

---

## 2. `git clone` — 克隆仓库

将远程仓库复制到本地。

Copy a remote repository to your local machine.

```bash
git clone https://github.com/username/repo-name.git
```

---

## 3. `git status` — 查看状态

查看当前哪些文件被修改、哪些待提交。

See which files are modified or staged for commit.

```bash
git status
```

---

## 4. `git add` — 添加到暂存区

将文件添加到下次提交的准备区域。

Stage files for the next commit.

```bash
git add filename.txt   # 添加单个文件
git add .              # 添加所有修改
```

---

## 5. `git commit` — 提交更改

将暂存区的内容保存为一次提交记录。

Save staged changes as a commit.

```bash
git commit -m "描述这次改动的内容"
```

---

## 6. `git push` — 推送到远程

将本地提交上传到 GitHub。

Upload local commits to GitHub.

```bash
git push origin main
```

---

## 7. `git pull` — 拉取最新内容

从远程仓库获取最新代码并合并到本地。

Fetch and merge the latest changes from remote.

```bash
git pull origin main
```

---

## 8. `git branch` — 管理分支

查看、创建或删除分支。

View, create, or delete branches.

```bash
git branch              # 查看所有分支
git branch new-feature  # 创建新分支
git branch -d old-feature # 删除分支
```

---

## 9. `git checkout` — 切换分支

切换到另一个分支。

Switch to a different branch.

```bash
git checkout new-feature
git checkout -b new-feature  # 创建并切换
```

---

## 10. `git log` — 查看提交历史

显示提交记录列表。

Show the commit history.

```bash
git log
git log --oneline  # 简洁版
```

---

## 快速备忘单 | Quick Cheat Sheet

| 命令 | 作用 |
|------|------|
| `git init` | 初始化仓库 |
| `git clone [url]` | 克隆仓库 |
| `git status` | 查看状态 |
| `git add .` | 暂存所有修改 |
| `git commit -m "msg"` | 提交 |
| `git push` | 推送到远程 |
| `git pull` | 拉取最新 |
| `git branch` | 查看分支 |
| `git checkout` | 切换分支 |
| `git log` | 查看历史 |
