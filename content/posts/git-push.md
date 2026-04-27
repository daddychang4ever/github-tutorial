---
title: "如何将代码推送到 GitHub | How to Push Code to GitHub"
date: 2026-04-23
draft: false
tags: ["Git", "Push", "推送", "教程"]
description: "手把手教你将本地代码推送到 GitHub 远程仓库的完整流程。A complete walkthrough of pushing your local code to a GitHub remote repository."
---

## 推送的完整流程 | The Full Push Workflow

将本地修改推送到 GitHub 分为三步：**暂存 → 提交 → 推送**

The process has three steps: **Stage → Commit → Push**

```
修改文件 → git add → git commit → git push → GitHub
```

---

## 第一步：查看修改状态

```bash
git status
```

红色文件名 = 已修改但未暂存  
绿色文件名 = 已暂存待提交

Red filenames = modified but not staged  
Green filenames = staged and ready to commit

---

## 第二步：暂存文件

```bash
git add .           # 暂存所有修改
git add index.html  # 只暂存指定文件
```

---

## 第三步：提交

```bash
git commit -m "修复首页导航栏样式"
```

写清楚这次改了什么，方便以后查看历史记录。

Write a clear message describing what you changed.

---

## 第四步：推送到 GitHub

```bash
git push origin main
```

`origin` = 远程仓库的别名（默认名称）  
`main` = 分支名称

---

## 第一次推送新仓库

如果是全新的本地仓库，需要先关联远程仓库：

```bash
git remote add origin https://github.com/username/repo.git
git branch -M main
git push -u origin main
```

之后就只需要 `git push` 就够了。

After the first time, just run `git push`.

---

## 推送被拒绝怎么办？| Push Rejected?

**错误：`rejected - non-fast-forward`**

说明远程有你本地没有的新提交，先拉取再推送：

```bash
git pull origin main
git push origin main
```

---

## 验证推送成功 | Verify Success

去 GitHub 仓库页面刷新，应该能看到你刚才的提交记录和最新文件。

Go to your GitHub repository page and refresh — you should see your latest commit.

---

## 下一步 | Next Steps

- [学习分支管理](/posts/git-branch/)
- [理解 Pull Request](/posts/pull-request/)
