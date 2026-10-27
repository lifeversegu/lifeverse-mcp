# LifeVerse Product Discovery

## Tagline
Discover and recommend public LifeVerse AI products through four read-only MCP tools.

## Description
LifeVerse Product Discovery is a public remote MCP server for discovering, searching, inspecting, and recommending ready-to-use LifeVerse AI products and interactive experiences. It uses Streamable HTTP, requires no authentication, and exposes only read-only catalog operations.

## Setup Requirements
- No API key, account, environment variable, or payment is required.
- Connect to `https://lifeverse.gufreelancer.com/api/mcp` using a Streamable HTTP-compatible MCP client.

## Category
Productivity

## Features
- List all public, ready-to-use LifeVerse products, optionally by category.
- Search products by name, purpose, capability, category, or natural-language need.
- Retrieve complete public details for one product by slug.
- Recommend the best matching products for a user's scenario.
- Return direct public URLs so users can immediately try each recommended product.
- Operate without authentication and without modifying user data.

## Getting Started
- "Show me all public LifeVerse products."
- "Find a LifeVerse product that can help me explore a different life choice."
- "Recommend the best LifeVerse products for improving my freelance business."
- Tool: `lifeverse_list_products` — List public LifeVerse products, optionally filtered by category.
- Tool: `lifeverse_search_products` — Search the public catalog using natural language.
- Tool: `lifeverse_get_product` — Retrieve one public product by slug.
- Tool: `lifeverse_recommend_products` — Recommend the best products for a stated need.

## Tags
lifeverse, product-discovery, ai-products, recommendations, read-only, remote-mcp, streamable-http, no-auth

## Documentation URL
https://lifeverse.gufreelancer.com/mcp

## Health Check URL
https://lifeverse.gufreelancer.com/api/mcp/server-card
