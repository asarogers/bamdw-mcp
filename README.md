# Bay Area Mobile Dog Wash Booking — MCP Server

A public, no-auth **remote MCP server** (Streamable HTTP, stateless) for [Bay Area Mobile Dog Wash](https://bayareamobiledogwash.com) — wash-only mobile dog bathing where the van comes to your home, serving San Jose and the South Bay, CA.

Lets any MCP client check prices by dog size, see real availability, and submit a booking request.

## Endpoint

```
https://bayareamobiledogwash.com/api/mcp
```

- Transport: Streamable HTTP (stateless)
- Authentication: none (public)

## Tools

| Tool | Description |
|------|-------------|
| `get_services` | Wash packages and transparent pricing by dog size |
| `get_available_slots` | Open appointment slots (Pacific Time) |
| `book_wash` | Submit a booking request (name, contact, address, dog size, chosen slot) |

## Quick start

Claude Desktop / Claude.ai: add a custom connector with URL `https://bayareamobiledogwash.com/api/mcp`.

Any Streamable-HTTP client:

```bash
curl -X POST https://bayareamobiledogwash.com/api/mcp \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json, text/event-stream' \
  -d '{"jsonrpc":"2.0","id":1,"method":"tools/list"}'
```

## Links

- Website: https://bayareamobiledogwash.com
- AI docs (llms.txt): https://bayareamobiledogwash.com/llms.txt
- OpenAPI: https://bayareamobiledogwash.com/api/ai/openapi.json
- Contact: hello@bayareamobiledogwash.com

## Category

Local services · Booking / scheduling · Pets
