# FDA Data MCP

**Connect AI agents to clean, queryable FDA data in minutes.**

This repo is the public quickstart for the FDA Data MCP endpoint used by Claude, Cursor, Windsurf, and OpenAI-compatible agent workflows.

- Canonical endpoint: `https://www.regdatalab.com/mcp`
- Sign up for API key: https://www.regdatalab.com/signup
- Full docs: https://www.regdatalab.com/docs

---

## 30-second quickstart (Claude Code)

```bash
claude mcp add fda-data https://www.regdatalab.com/mcp --transport http --header "Authorization: Bearer YOUR_API_KEY"
```

Then in Claude Code, run `/mcp` and confirm `fda-data` appears.

---

## MCP config JSON (Claude Desktop / Cursor / Windsurf)

```json
{
  "mcpServers": {
    "fda-data": {
      "url": "https://www.regdatalab.com/mcp",
      "headers": {
        "Authorization": "Bearer YOUR_API_KEY"
      }
    }
  }
}
```

---

## Verify it works

After connecting, ask your agent:

- “Find FDA facilities for Pfizer”
- “Show recent FDA recalls for Medtronic”
- “Search 510(k) clearances for product code XYZ”

If you get structured results, setup is complete.

---

## What you can do with FDA Data MCP

- Company resolution + alias normalization
- FDA facility lookup (drug/device registrations)
- Recalls and enforcement actions
- Inspections, citations, and compliance actions
- 510(k), PMA, NDC, and Drugs@FDA workflows

See all tools and parameters: https://www.regdatalab.com/docs#tools

---

## Common issues

### 401 Unauthorized
- Check your API key format and value
- Confirm header is exactly: `Authorization: Bearer YOUR_API_KEY`

### Connected, but no tools show
- Re-open/restart your client
- Re-run the add command and check `/mcp`

### Old endpoint in examples
Always use:

`https://www.regdatalab.com/mcp`

---

## Canonical links

- Website: https://www.regdatalab.com
- Connect guide: https://www.regdatalab.com/connect.md
- Tool docs: https://www.regdatalab.com/docs
- LLM context: https://www.regdatalab.com/llms.txt
- Full LLM context: https://www.regdatalab.com/llms-full.txt
- Pricing: https://www.regdatalab.com/pricing

---

## Repo scope

This repo is intentionally lightweight for public onboarding and discovery.
Core product/server implementation is maintained in a separate private repository.
