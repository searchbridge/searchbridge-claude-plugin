# SearchBridge for Claude

Connect Claude to [SearchBridge](https://www.searchbridge.ai), the AI representation intelligence and GEO platform. Once connected, Claude can explore your brand's SearchBridge data — how your brand and its competitors show up in AI-generated answers, KPI scores and competitor rankings — through read-only, permission-scoped queries. Claude only sees the brands your SearchBridge account is authorized for, and it cannot change any data.

## Requirements

- A SearchBridge account with access to at least one brand. To get one, contact [info@searchbridge.ai](mailto:info@searchbridge.ai).
- Claude Code, or any Claude app that supports plugins or custom connectors.

## Install

From the plugin directory, search for **SearchBridge** and install it.

Or add this repository as a marketplace in Claude Code:

```
/plugin marketplace add searchbridge/searchbridge-claude-plugin
/plugin install searchbridge@searchbridge
```

The plugin connects to the hosted SearchBridge MCP server at `https://intelligence.searchbridge.ai/api/mcp`. Nothing runs locally.

## Sign in

The first time Claude uses a SearchBridge tool, you are asked to sign in with your SearchBridge account (OAuth). Access is read-only (`searchbridge:read` scope) and limited to the brands you are permitted to see. You can revoke access at any time by disconnecting the server in Claude.

## Tools

All tools are read-only.

| Tool | What it does |
|---|---|
| `describe_data_surface` | Explore available SearchBridge data: what you can query and how. |
| `deep_tracking_query` | Analyze Deep Tracking KPI scores and official APS for a brand. |
| `competitive_query` | Analyze official Competitive Tracking results and competitor rankings. |
| `run_query` | Query SearchBridge brand data with a structured, read-only query. |
| `batch_queries` | Compare SearchBridge data by running several queries in one call. |
| `resolve_values` | Find matching SearchBridge data values to use in queries. |

## Example prompts

- "How visible is my brand in AI answers this month compared with last month?"
- "Who are my top competitors in AI search for my main product category?"
- "Which topics are we weakest on, and which competitor wins them?"

## Privacy and support

- Privacy policy: https://www.searchbridge.ai/privacy
- Terms: https://www.searchbridge.ai/terms
- Support: [info@searchbridge.ai](mailto:info@searchbridge.ai)

## License

The files in this repository are released under the [MIT License](LICENSE). "SearchBridge", "Search Bridge" and the SearchBridge logo are trademarks of Search Bridge S.r.l. SB and are not covered by this license.
