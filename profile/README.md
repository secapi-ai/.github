# SEC API

SEC API gives developers, researchers, and investment teams programmatic access to SEC filings, normalized company facts, ownership data, and filing search with source links.

## Choose An Interface

- [REST API](https://docs.secapi.ai/api-reference) for direct HTTP integrations and control over requests and responses.
- [SDKs](https://docs.secapi.ai/libraries-and-sdks) for JavaScript/TypeScript, Python, Go, and Rust applications.
- [CLI](https://docs.secapi.ai/cli) for terminal exploration, scripts, and JSON pipelines.
- [Hosted MCP](https://docs.secapi.ai/mcp-workflows) for an MCP-aware client or agent.
- [Agent skills](https://github.com/secapi-ai/secapi-skills) for repeatable, evidence-aware research workflows.

## First Successful Request

[Create an API key](https://secapi.ai/signup), set it in your environment, then use the [CLI](https://docs.secapi.ai/cli) to retrieve the latest annual filing for Apple:

```bash
export SECAPI_API_KEY="secapi_live_..."
secapi filings latest --ticker AAPL --form 10-K
```

The response identifies the filing for a workflow you can extend to a section, statement, or search query. The [first request guide](https://docs.secapi.ai/first-request-flows) covers the same path in more detail.

## Representative Workflows

- [Resolve an issuer and retrieve its latest filing](https://docs.secapi.ai/first-request-flows), then retain the returned filing metadata when you cite or analyze it.
- [Extract a filing section](https://docs.secapi.ai/tutorials/semantic-search-risk-factors), such as Item 1A risk factors, or search filing text for a disclosure topic.
- [Read normalized statements and company facts](https://docs.secapi.ai/api-reference/statements/get-v1-statements-all) alongside their filing provenance.
- [Track institutional ownership changes](https://docs.secapi.ai/tutorials/monitor-13f-holdings) and [insider activity](https://docs.secapi.ai/api-reference/insiders/get-v1-insiders).
- [Build a filing monitor](https://docs.secapi.ai/tutorials/build-filing-monitor) for a company, form, or disclosure workflow.

## Compatibility And Support

SDKs are available for JavaScript/TypeScript, Python, Go, and Rust. Use `secapi` in new CLI scripts; `omni-sec` remains a compatibility alias. Market-data capabilities depend on the applicable plan and provider entitlements.

[Documentation](https://docs.secapi.ai) · [API reference](https://docs.secapi.ai/api-reference) · [Pricing](https://secapi.ai/pricing) · [Status](https://status.secapi.ai) · [Support](https://secapi.ai/support)
