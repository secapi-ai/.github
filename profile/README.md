# SEC API by Turos

SEC API is the data interface for teams that need to turn SEC disclosures into inspectable research and production workflows. Retrieve filings, issuer records, financial statements, and ownership data through REST, SDKs, the CLI, or MCP. SEC API is built by [Turos](https://www.turos.app); the production API host is `https://api.turos.app`, and `https://api.secapi.ai` remains a permanently supported alias.

## Retrieve a filing

Create an API key in the [Turos console](https://console.turos.app/app), then make a server-side request:

```bash
export SECAPI_API_KEY="secapi_..."
curl --fail-with-body -sS \
  -H "x-api-key: $SECAPI_API_KEY" \
  "https://api.turos.app/v1/filings/latest?ticker=AAPL&form=10-K&view=agent"
```

The response identifies the latest matching Apple 10-K. Treat it as a dated source, not a permanent answer: retain the accession number, filing date, filing URL, and request ID with any analysis because a newer filing can change the result.

## Choose an interface

- [REST API](https://www.turos.app/docs/api-reference) for direct HTTP integrations.
- [JavaScript](https://www.turos.app/docs/sdks/javascript), [Python](https://www.turos.app/docs/sdks/python), [Go](https://www.turos.app/docs/sdks/go), and [Rust](https://www.turos.app/docs/sdks/rust) SDKs for application code using the public REST contract.
- [CLI](https://www.turos.app/docs/sdks/cli) for terminal research, scripts, and automation (`npm install -g @secapi/cli` or `brew install secapi-ai/tap/secapi`).
- [Hosted MCP](https://www.turos.app/docs/build/mcp) at `https://api.turos.app/mcp` for MCP-compatible clients. Authenticated tool calls use the same `x-api-key` header.

## Build with SEC API

- [Set up an account and make a first request](https://www.turos.app/docs/account-setup)
- [Retrieve normalized financial statements](https://www.turos.app/docs/api-reference/all-financial-statements)
- [Monitor 13F holdings changes](https://www.turos.app/docs/api-reference/compare-13f-quarters)
- [Analyze insider transactions](https://www.turos.app/docs/api-reference/search-insider-filings)
- [Find disclosures with semantic search](https://www.turos.app/docs/api-reference/semantic-filing-search)
- [Build a filing monitor](https://www.turos.app/docs/api-reference/compile-monitor-from-prompt)

Machine data requests use `x-api-key`; do not send a machine key as `Authorization: Bearer` or expose it in browser code. Start with the [documentation](https://www.turos.app/docs), review [pricing](https://www.turos.app/pricing/), check [status](https://status.turos.app), or get [support](https://www.turos.app/docs/admin/support).
