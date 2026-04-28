---
title: "如何配置 SSH Key 连接 GitHub | How to Set Up SSH Key for GitHub"
date: 2026-04-27
draft: false
tags: ["GitHub", "SSH", "SSH Key", "安全", "教程"]
description: "手把手教你生成 SSH Key 并配置到 GitHub，再也不用每次输入密码。Step-by-step guide to generating an SSH key and adding it to GitHub for password-free access."
---

## 为什么要用 SSH Key？

使用 HTTPS 连接 GitHub 每次推送都需要输入账号密码（或 Token），而配置 SSH Key 之后，**完全免密操作**，更安全也更方便。

## Why Use SSH Key?

HTTPS requires entering your credentials every push. With SSH Key configured, you get **password-free access** — more secure and convenient.

---

## 第一步：检查是否已有 SSH Key

在终端运行：

```bash
ls ~/.ssh
```

如果看到 `id_rsa.pub` 或 `id_ed25519.pub`，说明已经有 Key 了，跳到第三步。

If you see `id_rsa.pub` or `id_ed25519.pub`, you already have a key — skip to Step 3.

---

## 第二步：生成 SSH Key

运行以下命令（把邮箱替换成你的 GitHub 注册邮箱）：

```bash
ssh-keygen -t ed25519 -C "your@email.com"
```

全程按回车使用默认设置即可（不需要设置密码）。

Press Enter through all prompts to use defaults (no passphrase needed).

生成完成后会有两个文件：
- `~/.ssh/id_ed25519`（私钥，**不要泄露**）
- `~/.ssh/id_ed25519.pub`（公钥，上传到 GitHub）

---

## 第三步：复制公钥内容

**Mac / Linux：**
```bash
cat ~/.ssh/id_ed25519.pub
```

**Windows PowerShell：**
```powershell
cat ~/.ssh/id_ed25519.pub
```

复制输出的全部内容（以 `ssh-ed25519` 开头）。

Copy the entire output (starts with `ssh-ed25519`).

---

## 第四步：添加到 GitHub

1. 登录 GitHub，点右上角头像 → **Settings**
2. 左侧菜单点 **SSH and GPG keys**
3. 点 **New SSH key**
4. Title 填写备注名（如 `My Laptop`）
5. Key 栏粘贴刚才复制的公钥内容
6. 点 **Add SSH key**

---

## 第五步：测试连接

```bash
ssh -T git@github.com
```

看到以下提示说明配置成功：

```
Hi username! You've successfully authenticated, but GitHub does not provide shell access.
```

---

## 第六步：切换仓库为 SSH 地址

已有的仓库需要把 remote 地址从 HTTPS 改为 SSH：

```bash
git remote set-url origin git@github.com:username/repository.git
```

之后 `git push` 就完全免密了。

---

## 常见问题 | FAQ

**Q: `Permission denied (publickey)` 错误**  
A: 检查公钥是否正确添加到 GitHub，或重新运行 `ssh -T git@github.com`。

**Q: Windows 上找不到 `~/.ssh` 目录**  
A: `~` 对应 `C:\Users\你的用户名\`，即 `C:\Users\你的用户名\.ssh\`。

---

## 下一步 | Next Steps

- [学习基础 Git 命令](/posts/git-commands/)
- [如何将代码推送到 GitHub](/posts/git-push/)
