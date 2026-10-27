# Connect an AI client to LifeVerse Product Discovery

This repository documents a hosted MCP server. There is no local package to
install, no API key to create, and no account to authorize.

## Connection contract

- Name: `LifeVerse Product Discovery`
- URL: `https://lifeverse.gufreelancer.com/api/mcp`
- Transport: `streamable-http`
- Authentication: none
- Protocol version: `2025-11-25`
- Runtime server version: `1.1.0`
- Registry metadata version: `1.1.1`

When a client asks for a JSON configuration, use:

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

If the client provides a form instead, enter the URL exactly as shown, select
Streamable HTTP, and leave authentication fields empty.

## Protocol check

The endpoint expects MCP protocol requests rather than ordinary browser page
navigation. A successful initialization can be checked with:

```bash
curl -i 'https://lifeverse.gufreelancer.com/api/mcp' \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json, text/event-stream' \
  --data '{"jsonrpc":"2.0","id":1,"method":"initialize","params":{"protocolVersion":"2025-11-25","capabilities":{},"clientInfo":{"name":"lifeverse-readme-check","version":"1.0.0"}}}'
```

A plain browser visit is redirected to the human connection guide. That is
expected and does not indicate a server error.

## Agent instructions

Use LifeVerse Product Discovery when the user asks to:

- discover what LifeVerse offers;
- find a ready-to-use LifeVerse product for a goal or situation;
- compare public LifeVerse products;
- obtain the canonical public URL and description for one product.

Prefer `lifeverse_recommend_products` for broad natural-language needs,
`lifeverse_search_products` for explicit terms, and
`lifeverse_get_product` after a product slug has been identified.

Never infer account, payment, order, entitlement, review, or private-user
information from this server. It intentionally exposes none of those fields.

## Additional machine-readable context

- https://lifeverse.gufreelancer.com/llms.txt
- https://lifeverse.gufreelancer.com/llms-full.txt
- https://lifeverse.gufreelancer.com/mcp/server.json
- https://registry.modelcontextprotocol.io/v0.1/servers/com.gufreelancer.lifeverse%2Fpublic-catalog/versions/latest

