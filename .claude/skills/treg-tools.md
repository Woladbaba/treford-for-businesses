---
description: Use treg to search, discover, and call 4,200+ external tools (SEO, enrichment, social, ads, scraping, generation) via the treg MCP server or CLI.
---

# Treg Tool Gateway

Treg is configured as an MCP server at `https://treg.to/mcp/` with team token auth (team: oluwole-s-team).

## MCP Tools Available

- `catalog_search` - search the tool catalog by job description
- `catalog_get` - get details, parameters, and pricing for a specific tool
- `call` - execute a tool call (credentials injected server-side)
- `call_media` - call tools that return media (images, audio, video)
- `call_result` - retrieve async generation results
- `resources_list` - list available resources
- `balance` - check team credit balance
- `my_tools` - list tools registered to the team
- `catalog_request` - request a tool that doesn't exist yet
- `feedback` - submit feedback
- `review` - review a tool's output
- `mark` - bookmark a tool
- `compare` - compare providers for the same capability

## Workflow

1. `catalog_search` with a description of what you need (e.g. "backlinks for a domain")
2. `catalog_get` with the tool ID to see parameters and cost
3. `call` with tool ID and parameters to execute

## Rules

- Read the cost before calling. Confirm expected total before large loops or generation tasks.
- Do not retry provider 4xx errors; fix the request. On 429/5xx, try the next provider.
- Found emails and phone numbers are unverified; flag this to the user.
- Never ask for or paste provider API keys into code.
- Use `Idempotency-Key` header on calls that might need retrying after a timeout.

## CLI (if installed)

```
treg catalog search "<job>"
treg catalog get <tool-id>
treg call <tool-id> --query key=value
treg balance
```

## Reference

- Skill guide: https://treg.to/skill.md
- Integration docs: https://treg.to/integrate.md
- CLI usage: https://github.com/superdesigndev/treg/blob/main/USAGE.md
