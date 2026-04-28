---
title: "OpenClaw 入门教程：GitHub 最火 AI 助手完整安装指南 | OpenClaw Setup Guide"
date: 2026-04-28
draft: false
tags: ["AI", "OpenClaw", "AI助手", "开源", "GitHub热门"]
description: "OpenClaw 是2026年 GitHub 增速最快的开源项目，365k+ stars。本文手把手教你安装配置这个跨平台个人 AI 助手，支持微信、Telegram、Discord 等20+聊天软件。"
---

## 什么是 OpenClaw？

OpenClaw 是 2026 年 GitHub 上增速最快的开源项目之一，目前已超过 **365,000 颗星**。它是一个运行在你自己设备上的**个人 AI 助手**，最大特点是：

- **本地优先**：数据不上传，隐私完全由你掌控
- **全平台支持**：Windows / Mac / Linux
- **多渠道接入**：微信、QQ、Telegram、Discord、WhatsApp、Line 等 20+ 平台
- **随时在线**：24 小时在后台运行，随时响应

## What is OpenClaw?

OpenClaw is one of the fastest-growing open-source projects on GitHub in 2026, with 365,000+ stars. It's a personal AI assistant you run on your own devices — local-first, always-on, and connected to the messaging apps you already use.

---

## 为什么这么火？| Why So Popular?

- 数据完全本地，不依赖任何云服务
- 支持接入 Claude、GPT、DeepSeek 等各种大模型
- 一个助手同时管理你所有的聊天平台
- 可以执行浏览器操作、运行代码、管理文件

项目从 2025 年 12 月的一个周末小项目，到 2026 年 2 月突破 10 万星，速度之快创下 GitHub 历史纪录。

---

## 安装步骤 | Installation

### 前提条件 | Prerequisites

- Node.js 18+（[nodejs.org](https://nodejs.org) 下载）
- 一个 API Key（OpenAI / Claude / DeepSeek 任选一个）

### 一键安装 | One-line Install

**Mac / Linux：**
```bash
curl -fsSL https://openclaw.ai/install.sh | sh
```

**Windows（PowerShell）：**
```powershell
iwr https://openclaw.ai/install.ps1 | iex
```

安装完成后运行引导程序：

```bash
openclaw onboard
```

这会一步步引导你配置 AI 模型、连接聊天平台。

---

## 连接 Telegram（最简单的入门方式）

1. 在 Telegram 搜索 `@BotFather`，发送 `/newbot`
2. 按提示创建 bot，复制 Token
3. 在 OpenClaw 配置中填入 Token：

```bash
openclaw onboard
# 选择 Telegram，粘贴 Token
```

4. 启动：

```bash
openclaw start
```

现在给你的 Telegram bot 发消息，它就会用 AI 回复你了！

---

## 接入 AI 模型 | Connect AI Models

OpenClaw 支持多种模型，推荐国内用户使用 **DeepSeek**（便宜且速度快）：

```bash
openclaw config set ai.provider deepseek
openclaw config set ai.key YOUR_DEEPSEEK_API_KEY
```

或者使用 Claude：

```bash
openclaw config set ai.provider anthropic
openclaw config set ai.key YOUR_CLAUDE_API_KEY
```

---

## 常用命令 | Useful Commands

```bash
openclaw start      # 启动
openclaw stop       # 停止
openclaw status     # 查看运行状态
openclaw doctor     # 检查配置问题
openclaw update     # 更新到最新版本
```

---

## 注意事项 | Security Notes

- 建议只在自己的设备上运行，不要暴露在公网
- 不要把配置文件（含 API Key）上传到 GitHub
- 定期运行 `openclaw doctor` 检查安全配置

---

## 相关链接 | Links

- GitHub 仓库：[github.com/openclaw/openclaw](https://github.com/openclaw/openclaw)
- 官方文档：[docs.openclaw.ai](https://docs.openclaw.ai)

---

## 相关文章 | Related Posts

- [GitHub 上最值得收藏的免费资源合集](/posts/github-free-resources/)
- [2026年最好用的10个免费开发者工具](/posts/free-developer-tools/)
