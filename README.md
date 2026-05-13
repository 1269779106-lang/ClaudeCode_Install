# Claude Code 安装包 + CC-Switch 大模型切换工具

一站式解决方案：快速安装 Claude Code CLI，通过 CC-Switch 轻松接入国内外主流大模型。

---

## 项目简介

本项目提供 Claude Code 命令行工具的离线安装包，以及 CC-Switch API 代理切换工具，帮助开发者快速搭建 AI 编程环境，并灵活切换不同的大模型服务商。

### 为什么需要这个项目？

- **Claude Code** 是 Anthropic 官方推出的 AI 编程助手命令行工具，但国内下载安装不便
- **CC-Switch** 可以让你在多个 AI 服务商之间自由切换，无需反复修改配置
- 一套工具，支持 Claude、GPT、Gemini、DeepSeek、MIMO 等主流大模型

---

## 包含内容

| 文件 | 说明 |
|------|------|
| `claude.exe` | Claude Code CLI v2.1.123（Windows 离线安装包） |
| `CC-Switch-v3.14.1-Windows-Portable.zip` | CC-Switch 便携版（解压即用） |
| `安装说明.txt` | Claude Code 安装步骤 |
| `CC-Switch配置说明.txt` | CC-Switch 详细配置指南 |

---

## 支持的大模型

### Anthropic Claude 系列

| 模型 | 服务商 | 说明 |
|------|--------|------|
| Claude 4 Opus | Anthropic 官方 | 最强推理能力 |
| Claude 4 Sonnet | Anthropic 官方 | 平衡性能与速度 |
| Claude 4 Haiku | Anthropic 官方 | 快速响应 |
| DeepSeek-V4 Pro | DeepSeek 代理 | Anthropic 兼容接口 |
| MIMO v2.5 Pro | 小米 MIMO 代理 | 国内高速访问 |

### OpenAI GPT 系列（通过 Codex）

| 模型 | 服务商 | 说明 |
|------|--------|------|
| GPT-5.5 | OpenAI 官方 | 最新旗舰模型 |
| GPT-5.4 | OpenAI 官方 | 适合代码审查 |
| GPT-5.5 | 第三方代理 | api.1475258.xyz |
| GPT-5.5 | 第三方代理 | aimapi.cloud |

### Google Gemini 系列

| 模型 | 服务商 | 说明 |
|------|--------|------|
| Gemini | Google 官方 | 谷歌大模型 |

### 其他兼容模型

通过 Anthropic 兼容接口，还可以接入：
- **智谱 GLM** - 国产大模型
- **百川 Baichuan** - 国产大模型
- **月之暗面 Moonshot (Kimi)** - 国产大模型
- **零一万物 Yi** - 国产大模型
- **通义千问 Qwen** - 阿里大模型
- **文心一言 ERNIE** - 百度大模型
- **讯飞星火 Spark** - 科大讯飞大模型
- **豆包 Doubao** - 字节跳动大模型

> 只要服务商提供 Anthropic 或 OpenAI 兼容的 API 接口，都可以通过 CC-Switch 接入。

---

## 快速开始

### 第一步：安装 Claude Code

1. 下载 `claude.exe`
2. 复制到 `C:\Users\<你的用户名>\.local\bin\`
3. 将该目录添加到系统 PATH
4. 打开新终端，运行 `claude --version` 验证

详细步骤请参考 `安装说明.txt`

### 第二步：安装 CC-Switch

1. 下载 `CC-Switch-v3.14.1-Windows-Portable.zip`
2. 解压到任意目录
3. 运行 `cc-switch.exe`

### 第三步：配置大模型

1. 打开 CC-Switch
2. 点击 "+" 添加配置
3. 选择 API 类型（Claude/Codex/Gemini）
4. 填入 API Key 和 Base URL
5. 激活配置

详细配置请参考 `CC-Switch配置说明.txt`

---

## 配置示例

### 使用 DeepSeek 代理

```
API 类型: Claude
Base URL: https://api.deepseek.com/anthropic
API Key: 你的 DeepSeek API Key
模型: deepseek-v4-pro[1M]
```

### 使用小米 MIMO 代理

```
API 类型: Claude
Base URL: https://token-plan-cn.xiaomimimo.com/anthropic
API Key: 你的 MIMO Token
模型: mimo-v2.5-pro[1M]
```

### 使用 OpenAI 官方

```
API 类型: Codex
认证方式: ChatGPT 账号登录
网站: https://chatgpt.com/codex
```

---

## 文件结构

```
~/.cc-switch/                    # CC-Switch 配置目录
├── cc-switch.db                 # 配置数据库
├── settings.json                # 全局设置
├── logs/                        # 日志目录
│   └── cc-switch.log
└── backups/                     # 自动备份
```

---

## 常见问题

**Q: Claude Code 连接失败？**
A: 检查 API Key 是否正确、Base URL 是否可访问、网络是否正常。

**Q: 如何切换不同模型？**
A: 在 CC-Switch 主界面点击要使用的配置即可切换。

**Q: 配置保存在哪里？**
A: `%USERPROFILE%\.cc-switch\cc-switch.db`（SQLite 数据库）。

**Q: 如何备份配置？**
A: 备份 `%USERPROFILE%\.cc-switch\` 整个文件夹。

更多问题请参考 `CC-Switch配置说明.txt`

---

## 系统要求

- Windows 10 或更高版本
- 网络连接（访问 API 服务商）

---

## 相关链接

- [Claude Code 官方文档](https://docs.anthropic.com/en/docs/claude-code)
- [Anthropic 官网](https://www.anthropic.com)
- [OpenAI 官网](https://openai.com)
- [DeepSeek 官网](https://www.deepseek.com)

---

## 许可说明

- Claude Code 由 Anthropic 开发，使用请遵守其服务条款
- CC-Switch 由社区开发，请遵循其开源协议

---

## 更新日志

### 2025-05-13
- 初始版本发布
- 包含 Claude Code CLI v2.1.123
- 包含 CC-Switch v3.14.1 便携版
- 添加中文配置说明
