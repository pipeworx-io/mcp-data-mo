# mcp-data-mo

Missouri Open Data (data.mo.gov) Socrata MCP.

Part of [Pipeworx](https://pipeworx.io) — an MCP gateway connecting AI agents to 983+ live data sources.

## Tools

| Tool | Description |
|------|-------------|
| `datasets` | Search the Missouri Open Data catalog of open datasets by keyword. Returns each dataset\'s resource_id, name, description, category and update date — pass the resource_id to query/metadata. |
| `query` | Run a Socrata SoQL query against a Missouri Open Data dataset by resource_id (e.g. "gfq7-aa86"). Filter with where/select/group/order (SoQL clauses, without the leading $) plus limit/offset. Returns matching rows as JSON. |
| `metadata` | Get a Missouri Open Data dataset\'s schema + metadata (columns, types, row count, category, last-updated) by resource_id, e.g. "gfq7-aa86". |

## Quick Start

Add to your MCP client (Claude Desktop, Cursor, Windsurf, etc.):

```json
{
  "mcpServers": {
    "data-mo": {
      "url": "https://gateway.pipeworx.io/data-mo/mcp"
    }
  }
}
```

Or connect to the full Pipeworx gateway for access to all 983+ data sources:

```json
{
  "mcpServers": {
    "pipeworx": {
      "url": "https://gateway.pipeworx.io/mcp"
    }
  }
}
```

## Using with ask_pipeworx

Instead of calling tools directly, you can ask questions in plain English:

```
ask_pipeworx({ question: "your question about Data Mo data" })
```

The gateway picks the right tool and fills the arguments automatically.

## More

- [All tools and guides](https://github.com/pipeworx-io/examples)
- [pipeworx.io](https://pipeworx.io)

## License

MIT
