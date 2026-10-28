# LifeVerse 产品发现 MCP

[简体中文](README.zh-CN.md) · [English](README.md)

<p align="center">
  <img src="assets/icon.png" width="160" height="160" alt="LifeVerse 产品发现" />
</p>

LifeVerse 产品发现 MCP 是一个面向 AI 助手、智能体和大模型应用的公开远程
MCP 服务。它帮助用户发现、搜索、查看并推荐已经上线、可以立即体验的
LifeVerse AI 产品与互动体验。

- 永久公网地址：`https://lifeverse.gufreelancer.com/api/mcp`
- 传输协议：Streamable HTTP
- 登录与密钥：不需要
- 权限：只读，不读取账号、支付、订单或用户隐私数据
- 当前目录：11 个已公开产品
- 工具数量：4 个

## 快速连接

在支持远程 MCP 的客户端中加入以下配置：

```json
{
  "mcpServers": {
    "lifeverse": {
      "type": "streamable-http",
      "url": "https://lifeverse.gufreelancer.com/api/mcp"
    }
  }
}
```

不同客户端的配置文件位置可能不同，但公网地址和传输方式保持不变。完整中文
连接说明见 [LifeVerse MCP 使用页](https://lifeverse.gufreelancer.com/mcp)。

## 可以做什么

- `lifeverse_list_products`：列出所有已经公开、可以立即体验的产品，可按分类筛选。
- `lifeverse_search_products`：按照产品名、用途、能力、分类或自然语言需求搜索。
- `lifeverse_get_product`：按照公开 slug 查看一个产品的完整公开信息。
- `lifeverse_recommend_products`：根据用户的需求或场景推荐最匹配的产品。

例如可以直接向 AI 提问：

- “列出现在可以使用的 LifeVerse 产品。”
- “我想改善情绪和自我认知，有什么可以立即体验？”
- “推荐适合宠物记录、穿搭建议或人生规划的产品。”
- “我正在做自由职业，哪些 LifeVerse 产品适合我？”

## 中国大陆平台

- [魔搭社区永久公开页面](https://modelscope.cn/mcp/servers/lifeverse/lifeverse-product-discovery)
- Kimi 插件定义：[kimi.plugin.json](kimi.plugin.json)
- Kimi 自定义市场索引：[kimi-marketplace.json](kimi-marketplace.json)
- 千问代码助手 / Agent Plugins v1：[plugin.json](plugin.json)
- 通用远程 MCP 配置：[mcp.json](mcp.json)

Kimi Code：

```text
/plugins install https://github.com/lifeversegu/lifeverse-mcp
```

Qwen Code：

```bash
qwen extensions install lifeversegu/lifeverse-mcp
```

## 发现与验证入口

- 人类可读说明：https://lifeverse.gufreelancer.com/mcp
- AI 精简索引：https://lifeverse.gufreelancer.com/llms.txt
- AI 完整索引：https://lifeverse.gufreelancer.com/llms-full.txt
- 域名级 MCP 发现：https://lifeverse.gufreelancer.com/.well-known/mcp.json
- MCP Server Manifest：https://lifeverse.gufreelancer.com/mcp/server.json
- MCP Server Card：https://lifeverse.gufreelancer.com/api/mcp/server-card
- 官方 MCP Registry：https://registry.modelcontextprotocol.io/v0.1/servers/com.gufreelancer.lifeverse%2Fpublic-catalog/versions/latest
- mcpservers.org：https://mcpservers.org/servers/lifeversegu/lifeverse-mcp
- Walnut：https://walnut.world/w/lifeverse-product-discovery

## 安全边界

该服务只返回公开产品目录字段，不执行写操作，不访问账号、支付、订单、权益、
审核、未发布产品或私人用户数据。适用产品的风险提示仍以 MCP 返回的产品说明为准。

配置示例和文档使用 MIT License；LifeVerse 名称与 `assets/` 中的品牌图标不因
MIT License 授权给无关项目使用。
