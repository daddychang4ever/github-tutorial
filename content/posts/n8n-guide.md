---
title: "n8n 入门教程：免费开源的 AI 工作流自动化工具 | n8n Beginner's Guide"
date: 2026-04-28
draft: false
tags: ["n8n", "自动化", "AI工具", "开源", "GitHub热门"]
description: "n8n 是 GitHub 上最热门的开源工作流自动化工具，400+ 集成，可替代 Zapier。本文教你免费搭建自动化工作流，连接 AI 模型处理日常任务。"
---

## 什么是 n8n？

n8n 是一个开源的**工作流自动化平台**，可以将不同的应用和服务连接起来自动执行任务。简单来说，就是：

> 当 A 发生时，自动执行 B，然后通知 C

**GitHub 星标：117,000+**，是 Zapier 的免费开源替代品。

## What is n8n?

n8n is an open-source workflow automation platform that connects apps and services to automate tasks. Think "when X happens, automatically do Y and notify Z." It's a free, self-hosted alternative to Zapier with 400+ integrations.

---

## n8n 能做什么？| What Can n8n Do?

一些实际使用场景：

- 📧 **邮件自动分类**：收到邮件 → AI 分析内容 → 自动归档或回复
- 📊 **数据同步**：表格数据自动同步到数据库
- 🤖 **AI 客服**：接收用户消息 → 调用 GPT/Claude → 自动回复
- 📱 **社交媒体**：定时自动发布内容到多个平台
- 🔔 **监控告警**：网站宕机 → 立即发送 Telegram 通知

---

## 三种使用方式 | 3 Ways to Use n8n

| 方式 | 费用 | 适合人群 |
|------|------|---------|
| n8n Cloud | 免费试用，后付费 | 不想自己部署 |
| 本地运行 | 完全免费 | 开发测试 |
| 自托管（Docker）| 完全免费 | 长期使用推荐 |

---

## 快速开始：本地运行 | Quick Start: Run Locally

### 前提条件
- 安装 Node.js 18+

### 安装 n8n

```bash
npm install n8n -g
```

### 启动

```bash
n8n start
```

浏览器打开 `http://localhost:5678`，注册账号即可使用。

---

## Docker 部署（推荐）| Docker Deployment (Recommended)

```bash
docker run -it --rm \
  --name n8n \
  -p 5678:5678 \
  -v ~/.n8n:/home/node/.n8n \
  docker.n8n.io/n8nio/n8n
```

---

## 创建第一个工作流 | Create Your First Workflow

我们来做一个简单的例子：**定时获取天气，发送到 Telegram**

### 第一步：添加触发节点
1. 点击 **+** 添加节点
2. 搜索 **Schedule Trigger**
3. 设置每天早上 8 点触发

### 第二步：获取天气
1. 添加 **HTTP Request** 节点
2. URL 填写：`https://wttr.in/Shanghai?format=3`（免费天气 API）

### 第三步：发送 Telegram
1. 添加 **Telegram** 节点
2. 填入 Bot Token 和 Chat ID
3. 消息内容填：`今日天气：{{ $json.data }}`

### 第四步：保存并激活
点击右上角 **Save** → **Activate**，工作流开始运行。

---

## 接入 AI 模型 | Connect AI Models

n8n 内置支持 OpenAI、Claude、Gemini 等 AI 节点：

1. 添加 **AI Agent** 节点
2. 选择模型（OpenAI / Anthropic / Gemini）
3. 填入 API Key
4. 输入系统提示词，就可以在工作流中调用 AI 了

---

## 常见工作流模板 | Popular Workflow Templates

访问 [n8n.io/workflows](https://n8n.io/workflows) 可以直接导入社区分享的现成模板，包括：

- AI 邮件助手
- GitHub Issue 自动分类
- RSS 订阅 → AI 摘要 → 推送通知
- 社交媒体内容自动化

---

## 相关链接 | Links

- GitHub：[github.com/n8n-io/n8n](https://github.com/n8n-io/n8n)
- 官网：[n8n.io](https://n8n.io)
- 模板库：[n8n.io/workflows](https://n8n.io/workflows)

---

## 相关文章 | Related Posts

- [OpenClaw 入门教程](/posts/openclaw-guide/)
- [2026年最好用的10个免费开发者工具](/posts/free-developer-tools/)
- [GitHub Actions 自动化入门](/posts/github-actions/)
