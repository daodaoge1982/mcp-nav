# MCP Navigator

> 🌐 Model Context Protocol 资源导航站 | 收录最全的 MCP 服务器资源

[![Deploy](https://img.shields.io/badge/Deploy-GitHub%20Pages-blue?style=flat-square)](https://pages.github.com/)
[![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)](./LICENSE)
[![MCP Servers](https://img.shields.io/badge/MCP%20Servers-30%2B-orange?style=flat-square)]()

## 📖 简介

MCP Navigator 是一个开放的中文 MCP（Model Context Protocol）资源导航站，收录 AI 时代主流的 MCP 服务器，提供安装命令、配置说明和文档链接，帮助你快速找到并接入需要的 MCP 工具。

## ✨ 功能

- 🔍 **实时搜索** — 键盘快捷键 (⌘K / Ctrl+K) 呼出，毫秒级过滤
- 🌙 **深色/浅色主题** — 自动记忆偏好
- 📱 **响应式设计** — 完美适配手机、平板、PC
- 📦 **30+ 服务器** — 覆盖开发、协作、数据、云服务等 9 大分类
- 🚀 **快速上手** — 3 步完成 MCP 接入

## 🚀 快速开始

### 方式一：在 AI 助手中使用

以 OpenClaw 为例，编辑 `~/.openclaw/workspace/config/mcporter.json`：

```json
{
  "mcpServers": {
    "gate-cex-pub": {
      "baseUrl": "https://api.gatemcp.ai/mcp"
    },
    "gate-info": {
      "baseUrl": "https://api.gatemcp.ai/mcp/info"
    },
    "gate-news": {
      "baseUrl": "https://api.gatemcp.ai/mcp/news"
    }
  }
}
```

重启 AI 助手即可。

### 方式二：使用 mcporter CLI

```bash
# 安装 mcporter
npm install -g mcporter

# 添加服务器
mcporter config add gate-cex-pub --url https://api.gatemcp.ai/mcp

# 查询行情
mcporter call gate-cex-pub.cex_spot_get_spot_tickers currency_pair=BTC_USDT
```

### 方式三：在 Claude Desktop 中使用

编辑 `~/.config/Claude/claude_desktop_config.json`：

```json
{
  "mcpServers": {
    "filesystem": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-filesystem", "/path/to/folder"]
    },
    "github": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-github"],
      "env": { "GITHUB_TOKEN": "your-token-here" }
    }
  }
}
```

## 📂 项目结构

```
mcp-nav/
├── index.html          # 导航站主页面（单文件，无需构建）
├── README.md           # 项目说明
├── CONTRIBUTING.md     # 贡献指南
└── .gitignore
```

## 🤝 贡献

欢迎推荐新的 MCP 服务器！请参考 [CONTRIBUTING.md](./CONTRIBUTING.md)。

## 📄 协议

MIT License © 2024 MCP Navigator

## 🔗 相关链接

- [Model Context Protocol 官方](https://modelcontextprotocol.io)
- [MCP Python SDK](https://github.com/modelcontextprotocol/python-sdk)
- [awesome-mcp](https://github.com/yuna-nakamura/awesome-mcp)
