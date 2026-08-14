# CompCode

**Commission plans as code.** CompCode is the first sales compensation platform
where plans are created, modified, and versioned through an API — not a
proprietary UI. Author a plan in your editor, simulate it against real deals,
and deploy it the same way you ship anything else.

→ [compcode.ai](https://compcode.ai) · [Docs](https://compcode.ai/docs) · [API reference](https://api.compcode.ai/docs)

## MCP server

[`@compcode/mcp`](https://www.npmjs.com/package/@compcode/mcp) exposes the full
commission lifecycle as native tools for Claude Code, Cursor, and any Model
Context Protocol client — plans, quotas, assignments, simulation, statements,
and payroll export, backed by live CRM data.

```bash
claude mcp add compcode -e COMPCODE_API_KEY=ws_your_key -- npx -y @compcode/mcp
```

Source: [compcode-ai/mcp](https://github.com/compcode-ai/mcp)

There is also a remote transport if you'd rather not run a local process —
`POST https://api.compcode.ai/v1/mcp` (Streamable HTTP, workspace API key as a
bearer token). Same tool contract, pick whichever fits your client.

## CRM integrations

Commission calculation runs against live deal data from **Attio**, **HubSpot**,
and **Salesforce**. Deals sync in through webhooks (or polling, on Salesforce),
and every calculation carries a full audit trace back to the tier and rule that
produced it.

## For agents

The API is designed to be driven by coding agents as a first-class client:

| Resource | URL |
| --- | --- |
| Agent rules file | [`api.compcode.ai/CLAUDE.md`](https://api.compcode.ai/CLAUDE.md) |
| Full docs, markdown | [`api.compcode.ai/llms-full.txt`](https://api.compcode.ai/llms-full.txt) |
| OpenAPI spec | [`api.compcode.ai/v1/openapi.json`](https://api.compcode.ai/v1/openapi.json) |
| Site index | [`compcode.ai/llms.txt`](https://compcode.ai/llms.txt) |

Drop `CLAUDE.md` into your project and your agent knows how to talk to the API.

---

Questions or bug reports: [open an issue](https://github.com/compcode-ai/mcp/issues).
