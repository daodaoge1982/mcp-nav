# 如何贡献

我们欢迎任何形式的贡献！推荐新的 MCP 服务器、修复错误、改进文档均可。

## 推荐新服务器

推荐前请先确认该 MCP 服务器：
1. 是真实存在且可用的
2. 有公开的文档或源码
3. 不是重复收录

## 提交方式

### 方式一：提交 Issue
在 [GitHub Issues](https://github.com/your-username/mcp-nav/issues/new?template=add-server.md) 中提交，模板如下：

### 方式二：提交 Pull Request

直接编辑 `index.html`，在对应分类的 `mcpServers` 数组中添加条目：

```javascript
{
  name: '服务器名称',
  description: '简短描述（20字以内）',
  install: '安装命令',
  doc: '文档链接',
  tags: ['标签1', '标签2']
}
```

## MCP 服务器收录标准

- ✅ 有明确的用途和功能描述
- ✅ 有可用的安装命令
- ✅ 有官方文档或 GitHub 仓库
- ✅ 属于 MCP 协议兼容的服务器
- ❌ 不收录需要付费且无免费额度的服务
- ❌ 不收录有明显安全风险的服务器

## 推荐信息模板

```
名称：
官方名称（如有）：
描述：
官网/文档：
安装命令：
推荐标签（最多3个）：
适用场景：
```

感谢你的贡献！
