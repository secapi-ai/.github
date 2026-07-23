# SEC API

SEC API is the data interface for teams that need to turn SEC disclosures into inspectable research and production workflows. Retrieve filings, issuer records, financial statements, and ownership data through REST, SDKs, the CLI, or MCP.

## Retrieve a filing

Create an API key in the [SEC API dashboard](https://secapi.ai/app), then make a server-side request:

```bash
export SECAPI_API_KEY="secapi_..."
curl --fail-with-body -sS \
  -H "x-api-key: $SECAPI_API_KEY" \
  "https://api.secapi.ai/v1/filings/latest?ticker=AAPL&form=10-K&view=agent"
```

The response identifies the latest matching Apple 10-K. Treat it as a dated source, not a permanent answer: retain the accession number, filing date, filing URL, and request ID with any analysis because a newer filing can change the result.

## Choose an interface

- [REST API](https://docs.secapi.ai/api-reference) for direct HTTP integrations.
- [JavaScript, Python, Go, and Rust SDKs](https://docs.secapi.ai/libraries-and-sdks) for application code using the public REST contract.
- [CLI](https://docs.secapi.ai/cli) for terminal research, scripts, and automation.
- [Hosted MCP](https://docs.secapi.ai/mcp-install) for MCP-compatible clients. Authenticated tool calls use the same `x-api-key` header.

## Build with SEC API

- [Resolve an issuer, retrieve a filing, and extract a section](https://docs.secapi.ai/first-request-flows)
- [Retrieve normalized financial statements](https://docs.secapi.ai/api-reference/statements/get-v1-statements-all)
- [Monitor 13F holdings changes](https://docs.secapi.ai/tutorials/monitor-13f-holdings)
- [Analyze insider transactions](https://docs.secapi.ai/api-reference/insiders/get-v1-insiders)
- [Find disclosures with semantic search](https://docs.secapi.ai/tutorials/semantic-search-risk-factors)
- [Build a filing monitor](https://docs.secapi.ai/tutorials/build-filing-monitor)

Machine data requests use `x-api-key`; do not send a machine key as `Authorization: Bearer` or expose it in browser code. Start with the [documentation](https://docs.secapi.ai), review [pricing](https://secapi.ai/pricing), check [status](https://status.secapi.ai), or get [support](https://secapi.ai/support).
