# RESEARCH.md

> Comprehensive research, rationale, and mapping for MCP Persona Packages  
> **Updated**: August 25, 2025

---

## 0. Project Overview

This repository defines **MCP Persona Packages**: ready-to-use configurations that bundle together
- `mcp.json` files (server runners + environment variables as placeholders)
- `persona.yaml` files (Claude-code style persona definitions with toolsets)

Each persona represents a role in a company (developer, project manager, IT support, etc.) and
is equipped with a set of **MCP servers** and **toolsets** that capture their common workflows.

The intent is to accelerate how teams use MCP-enabled agents by giving them curated “content packs”
that combine servers, tools, and best practices into a drop-in bundle.

---

## 1. Inputs and Sources

### Persona Registry
- **Claude-code subagents registry (wshobson/agents)**  
  👉 https://github.com/wshobson/agents

### MCP Server Registries
- **wong2/awesome-mcp-servers**  
  👉 https://github.com/wong2/awesome-mcp-servers
- **punkpeye/awesome-mcp-servers**  
  👉 https://github.com/punkpeye/awesome-mcp-servers
- **toolsdk-ai/awesome-mcp-registry**  
  👉 https://github.com/toolsdk-ai/awesome-mcp-registry
- **smithery-ai/reference-servers**  
  👉 https://github.com/smithery-ai/reference-servers
- **Model Context Protocol — Official Examples & Integrations**  
  👉 https://modelcontextprotocol.io/examples

### Mirrors/Indices
- [MCPServers.org](https://mcpservers.org)  
- [mcp.so](https://mcp.so)  
- [lobehub.com MCP registry](https://lobehub.com/mcp)

---

## 2. Schema Conventions

- **Persona names**: lowercase, hyphenated, ending with `-assistant` (e.g. `software-developer-assistant`).
- **Toolset names**: lowercase, hyphenated, broad themes (e.g. `release-prep-team-nudges`).
- **Tool names**: exact MCP names, namespaced as `server.tool`.
- **mcp.json**: must use **remote runners** (`npx` for Node, `uvx` for Python). No local directories.
- **Env vars**: always shown as `"<placeholder>"`. Never commit secrets.
- **Toolset descriptions**: must include examples of representative tasks.

---

## 3. Directory Structure Example

```
/RESEARCH.md
/README.md
/personas/
  /software-developer-assistant/
    mcp.json
    persona.yaml
  /project-manager-assistant/
    mcp.json
    persona.yaml
  /it-support-assistant/
    mcp.json
    persona.yaml
```

---

## 4. Toolset Design Guidance

- 3–5 **themes** per persona (not single tasks).
- Each toolset can mix tools from multiple servers.
- Max 10 tools per toolset (ideally 5–7).
- Each toolset must include a description with **examples**.

---

## 5. Servers Mapped to Current Personas

### Git MCP Server
- **Repo**: https://github.com/modelcontextprotocol/servers  
- **Docker Hub**: https://hub.docker.com/r/mcp/git  
- **Runner**: `uvx mcp-server-git`  
- **Env**: None  
- **Persona usage**: `software-developer-assistant`

### Slack MCP Server
- **Repo**: https://github.com/bahakizil/slack_mcp_server  
- **PyPI**: https://pypi.org/project/slack-mcp-server/  
- **Runner**: `uvx slack-mcp-server`  
- **Env**: `SLACK_BOT_TOKEN`  
- **Persona usage**: all three personas

### Jira MCP Server
- **Repo**: https://github.com/tom28881/mcp-jira-server  
- **NPM**: https://www.npmjs.com/package/jira-mcp-server  
- **Runner**: `npx jira-mcp-server`  
- **Env**: `JIRA_HOST`, `JIRA_EMAIL`, `JIRA_API_TOKEN`  
- **Persona usage**: `project-manager-assistant`, `it-support-assistant`

---

## 6. Tool Research Requirements

**IMPORTANT**: Tool names must always be verified from the actual MCP server documentation. Do not rely on assumed or cached tool names.

### Research Process for Tools
When validating tool names in a persona:
1. Identify the MCP server package (e.g., `slack-mcp-server`)
2. Look up the package documentation on GitHub, npm, or PyPI
3. Find the actual tool names from the README or documentation
4. Verify the tool naming format matches `{server_name}.{actual_tool_name}`

### Example: Slack MCP Server
According to the [slack-mcp-server documentation](https://github.com/korotovsky/slack-mcp-server):
- Available tools: `conversations_history`, `conversations_replies`, `conversations_add_message`, `conversations_search_messages`, `channels_list`
- Note: Tool names follow Slack API conventions with `conversations_` and `channels_` prefixes

### Tool Naming Format
The format is always: `{server_name_in_mcp_json}.{actual_tool_name_from_docs}`
- Example: If server name in mcp.json is "slack" and tool is "conversations_add_message", the toolId would be "slack.conversations_add_message"

### Common MCP Servers (always verify current tools)
- **Git MCP** (`mcp-server-git`): Check GitHub for current tool list
- **Slack MCP** (`slack-mcp-server`): Check GitHub for current tool list  
- **Jira MCP**: Various implementations exist, verify specific package
- **Linear MCP** (`@modelcontextprotocol/server-linear`): Check official docs
- **Trello MCP** (`@modelcontextprotocol/server-trello`): Check official docs

---

## 7. Current Persona to Server Mapping

| Persona | Servers | Why this set |
|---------|---------|--------------|
| **software-developer-assistant** | Git, Slack | Developers constantly branch/commit and share updates in Slack. |
| **project-manager-assistant** | Jira, Slack | PMs triage work, run reports in Jira, and announce updates in Slack. |
| **it-support-assistant** | Jira, Slack | Support teams open incidents in Jira and broadcast updates in Slack. |

---

## 8. Candidate Servers for Future Personas

### Data / Analytics
- [postgres-mcp](https://github.com/modelcontextprotocol/servers/tree/main/postgres)
- [sqlite-mcp](https://github.com/modelcontextprotocol/servers/tree/main/sqlite)
- [tinybird-mcp](https://github.com/tinybirdco/mcp-tinybird)
- [qdrant-mcp](https://github.com/qdrant/mcp-server)

### DevOps / Infrastructure
- [cloudflare-mcp](https://github.com/cloudflare/mcp-server)
- [sentry-mcp](https://github.com/getsentry/mcp-server)
- [docker-mcp](https://github.com/modelcontextprotocol/servers/tree/main/docker)

### Marketing / Research
- [brave-search-mcp](https://github.com/brave/mcp-server)
- [reader-mcp](https://github.com/modelcontextprotocol/servers/tree/main/reader)
- [notion-mcp](https://github.com/NotionAI/mcp-server)
- [confluence-mcp](https://github.com/atlassian/mcp-confluence)

### Finance / Sales Ops
- [stripe-mcp](https://github.com/stripe/mcp-server)
- [salesforce-mcp](https://github.com/salesforce/mcp-server)

---

## 9. Expansion Roadmap

Personas we can add next (with candidate servers):
- **data-analyst-assistant**: Postgres, Tinybird, Qdrant
- **ui-engineer-assistant**: Playwright, ExaSearch, Shadcn
- **qa-engineer-assistant**: Playwright, Docker, Recoll
- **devops-engineer-assistant**: Cloudflare, Docker, Sentry
- **observability-engineer-assistant**: Sentry, Axiom, Grafana
- **marketer-assistant**: Brave Search, Reader, Notion, Confluence
- **sales-operations-assistant**: Salesforce, Stripe, Google Sheets
- **finance-analyst-assistant**: Postgres, Stripe, Excel exporter
- **legal-ops-assistant**: Notion, Confluence, Recoll

---

## 10. Server Discovery Checklist

When adding new servers:
1. Prefer **official/company-maintained** repos (Stripe, Atlassian, Cloudflare).  
2. Look for published packages (`npm`, `PyPI`, Docker images).  
3. Check repo activity (commits, issues closed, stars).  
4. Verify tool names in the `mcp.json` or codebase.  
5. Document required env vars with `"<placeholder>"`.  

---

## 11. Environment Variables (Placeholders Only)

| Server | Env vars |
|--------|----------|
| Slack MCP | `SLACK_BOT_TOKEN` |
| Jira MCP | `JIRA_HOST`, `JIRA_EMAIL`, `JIRA_API_TOKEN` |
| Git MCP | None |

---

## 12. Key Takeaways

- **Toolset = theme**: not single tasks, but workflows (3–5 per persona).  
- **Cross-server mixing**: one toolset may use Git + Slack or Jira + Slack together.  
- **Remote runners only**: `npx` for Node, `uvx` for Python; never rely on local paths.  
- **Environment variables**: placeholders only; secrets never committed.  
- **Expansion**: roadmap is clear for data, infra, marketing, finance personas.  
- **Clarity**: keeping consistent conventions ensures contributors can expand personas safely.
