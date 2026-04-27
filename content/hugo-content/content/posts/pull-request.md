---
title: "什么是 Pull Request？| What is a Pull Request?"
date: 2026-04-22
draft: false
tags: ["GitHub", "Pull Request", "PR", "协作"]
description: "详细介绍 GitHub Pull Request 的概念、创建流程和代码审查最佳实践。A detailed guide to GitHub Pull Requests — what they are, how to create one, and code review best practices."
---

## 什么是 Pull Request？

Pull Request（简称 PR）是 GitHub 上最核心的协作功能。当你完成了某个功能或修复，通过 PR 通知项目维护者："我改了这些内容，请帮我审查并合并到主分支。"

## What is a Pull Request?

A Pull Request (PR) is GitHub's core collaboration feature. When you finish a feature or fix, a PR notifies the project maintainer: "Here's what I changed — please review and merge it."

---

## PR 的工作流程 | PR Workflow

```
Fork 仓库 → 创建分支 → 修改代码 → 推送分支 → 发起 PR → 代码审查 → 合并
```

---

## 第一步：Fork 仓库

对于别人的项目，先点仓库右上角的 **Fork** 按钮，将其复制到自己账号下。

For someone else's project, click **Fork** to copy it to your account.

---

## 第二步：创建新分支

不要直接在 `main` 分支修改，创建一个专属分支：

```bash
git checkout -b fix-typo-readme
```

---

## 第三步：修改并推送

```bash
# 修改文件后
git add .
git commit -m "修复 README 中的拼写错误"
git push origin fix-typo-readme
```

---

## 第四步：在 GitHub 创建 PR

1. 去你的 Fork 仓库页面
2. GitHub 会自动提示 **"Compare & pull request"**，点击它
3. 填写 PR 标题和描述，说明你改了什么、为什么改
4. 点击 **Create pull request**

---

## 好的 PR 描述应包含 | A Good PR Description Includes

- **改了什么** What was changed
- **为什么改** Why it was changed  
- **如何测试** How to test it
- **相关截图**（如有界面变化）Screenshots if UI changed

---

## 代码审查 | Code Review

维护者会查看你的代码，可能会：
- ✅ 直接合并
- 💬 留下评论要求修改
- ❌ 关闭 PR（不接受这个改动）

收到修改意见后，继续在同一分支上修改推送，PR 会自动更新。

---

## 合并后清理分支 | Clean Up After Merge

PR 合并后，删除已完成的分支：

```bash
git branch -d fix-typo-readme
git push origin --delete fix-typo-readme
```

---

## 下一步 | Next Steps

- [学习 GitHub Issues](/posts/github-issues/)
- [了解 GitHub Actions 自动化](/posts/github-actions/)
