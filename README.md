# Fylings MCP Server

> Search, verify and screen **1,000,000+ African companies** — plus their **government contracts** — from any AI agent.

The **Fylings MCP server** gives Claude, ChatGPT, Cursor and any [Model Context Protocol](https://modelcontextprotocol.io) client live access to African company intelligence: companies across **18 official registries**, **government-procurement** records, and **OFAC/UN sanctions** screening — with the registry **source**, the **date checked**, and a **confidence** signal on every result.

Fylings never fabricates data: a value the registrar doesn't publish is left `null`, not guessed.

**Live · remote · no API key required.**

## Connect

It's a remote (Streamable HTTP) server. For clients with native remote-MCP support (Claude.ai, Cursor, VS Code), add the endpoint:

```
https://www.fylings.com/api/mcp
```

For Claude Desktop or any stdio client, bridge it with `mcp-remote`:

```json
{
  "mcpServers": {
    "fylings": {
      "command": "npx",
      "args": ["mcp-remote", "https://www.fylings.com/api/mcp"]
    }
  }
}
```

## Tools

| Tool | What it does |
|---|---|
| `search_companies` | Search 18 African registries by name or registration number — ranked by quality (listed, best-detailed companies first). |
| `get_company` | Fetch a full company record by country code + registration number. |
| `get_company_procurement` | List the government contracts a company has won — buyer, title, value, date. |
| `screen_sanctions` | Screen any name against the OFAC SDN, OFAC Consolidated and UN Security Council lists. |

## What's behind it

- **1,000,000+ companies** across **18 African registries** (Nigeria, Tanzania, Mauritius, Ghana, Zambia, Madagascar, Kenya, Senegal, Uganda, Angola and more)
- **500,000+ government-procurement awards** matched to the companies that won them
- **OFAC / UN sanctions** screening with match confidence
- **Provenance on every record** — source · last-checked date · confidence

## Links

- Website — https://www.fylings.com
- MCP — https://www.fylings.com/mcp
- API — https://www.fylings.com/api
- Official MCP Registry — `io.github.HeyZod/fylings`

---

Built by [Fylings](https://www.fylings.com) — African company intelligence.
