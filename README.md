# 模型列表

- gpt-5.4
- gpt-5.3-codex-spark
- gpt-5.3-codex
- gpt-5.2-codex
- gpt-5.2
- gpt-5.1-codex-mini
- gpt-5.1-codex-max
- gpt-5.1-codex
- gpt-5.1
- gpt-5

不要使用不在列表中的模型名进行逃费，若被发现，我们将会限制你的账号。

任何不在列表中的模型都会被路由到gpt-5.1，

# Codex 部署教程

本仓库用于整理一套可直接上手的教程：

1. 安装并使用 Codex CLI
2. 安装 CC Switch，并使用 CC Switch 控制 Codex CLI 的 API 提供商
3. 安装 Visual Studio Code 的 Codex 插件

## 1. 安装并使用 Codex CLI

### 1.1 前置条件

- 已安装 Node.js 与 npm（用于安装 `@openai/codex`）
- 建议已安装 Git

> 官方说明：Codex CLI 在 macOS/Linux 可用；Windows 为实验性支持。  
> 在 Windows 上推荐使用 WSL 工作区运行 Codex。

### 1.2 安装

```bash
npm i -g @openai/codex
```

或：Windows系统下打开powershell

```bash
winget install OpenAI.Codex
```

可选：确认安装成功

```bash
codex --version
```


### 1.3 首次运行与登录

在你的项目目录下执行：

```bash
codex
```

首次启动会提示登录，可选两种方式：

- 使用 ChatGPT 账号登录
- 使用 API Key 登录

### 1.4 基本使用

进入项目后执行：

```bash
codex
```

### 1.5 更新 Codex CLI

```bash
npm i -g @openai/codex@latest
```

---

## 2. 安装 CC Switch，并用它控制 Codex CLI 的 API 提供商

### 2.1 安装 CC Switch

[CC Switch Release页](https://github.com/farion1231/cc-switch/releases)

按你的系统选择安装方式（推荐直接从 Releases 下载最新版本）：

- Windows：下载 `.msi` 或便携版 `.zip`
- macOS：Homebrew 或 Releases 安装包
- Linux：`.deb` / `.rpm` / `.AppImage` / `.flatpak`

### 2.2 在 CC Switch 中配置 Codex 提供商

1. 打开 CC Switch。
2. 在应用中选择 `Codex`。
3. 点击右上角 `+` 添加供应商。
4. 选择自定义配置
5. 填入自己的`API Key`、`API请求地址`（注意不是`官网链接`）。
6. 点击添加并保存。
7. 在供应商卡片点击“启用”完成切换。

API请求地址一般为

```
https://api.asxs.top/v1
```

模型名称可设为

```
gpt-5.3-codex
```

### 2.3 让配置对 Codex CLI 生效

需要重启终端后再启动Codex就能生效。

```bash
codex
```

发起一个简单请求，在[cdk激活页面](https://cdk.asxs.top/)即可查看请求日志。

---

## 3. 安装 Visual Studio Code 的 Codex 插件

### 3.1 安装步骤

1. 打开 VS Code 扩展市场。
2. 搜索并安装：`Codex – OpenAI’s coding agent`（发布者：OpenAI）。
3. 或直接通过 Marketplace 链接安装（见文末参考链接）。
4. 安装后如果侧边栏未出现 Codex，重启 VS Code。

### 3.2 登录与使用

安装后插件会提示登录：

- 使用 ChatGPT 账号登录
- 或使用 API Key

CC Switch也能控制Visual Studio Code的服务供应商

---

## 参考链接（官方/项目文档）

- VS Code Marketplace（Codex 插件）：https://marketplace.visualstudio.com/items?itemName=openai.chatgpt

- OpenAI Codex CLI（官方）：https://developers.openai.com/codex/cli
- OpenAI Codex IDE 插件（官方）：https://developers.openai.com/codex/ide
- OpenAI Codex GitHub：https://github.com/openai/codex
- CC Switch 项目主页：https://github.com/farion1231/cc-switch
- CC Switch 中文用户手册：https://github.com/farion1231/cc-switch/blob/main/docs/user-manual/zh/README.md
