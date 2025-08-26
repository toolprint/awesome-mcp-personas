# MCP Servers in Active Use

> Cross-reference of MCP servers currently used in personas
> **Last Updated**: 2025-08-26

## Summary

| Total Servers | Total Personas | Most Used Server |
|---------------|----------------|------------------|
| 9 | 6 | Git (3 personas) |

---
what
## Active Servers by Usage

### High Usage (3+ personas)
| Server | Package | Personas Count | Environment |
|--------|---------|----------------|-------------|
| **Git** | `uvx mcp-server-git` | 3 | None |
| **Slack** | `uvx slack-mcp-server` | 3 | `SLACK_BOT_TOKEN` |
| **Filesystem** | `npx -y @modelcontextprotocol/server-filesystem` | 3 | None |

### Medium Usage (2 personas)

### Low Usage (1 persona)
| Server | Package | Personas Count | Environment |
|--------|---------|----------------|-------------|
| **Linear** | `npx -y @modelcontextprotocol/server-linear` | 1 | `LINEAR_API_KEY` |
| **GitHub** | `npx -y @modelcontextprotocol/server-github` | 1 | `GITHUB_PERSONAL_ACCESS_TOKEN` |
| **Trello** | `npx -y @modelcontextprotocol/server-trello` | 1 | `TRELLO_API_KEY`, `TRELLO_TOKEN` |
| **Fetch** | `npx -y @modelcontextprotocol/server-fetch` | 2 | None |
| **Memory** | `npx -y @modelcontextprotocol/server-memory` | 1 | None |
| **Playwright** | `npx -y @modelcontextprotocol/server-playwright` | 2 | None |
| **Docker** | `npx -y docker-mcp` | 1 | None |

---

## Server Details & Tool Usage

### Git MCP Server
- **Source**: https://github.com/modelcontextprotocol/servers/tree/main/src/git
- **Package**: `uvx mcp-server-git`
- **Environment**: None required
- **Used in**:
  - [software-development-assistant](../personas/software-development-assistant/) - Version control workflows
  - [intern](../personas/intern/) - Basic git operations
  - [linear-project-manager](../personas/linear-project-manager/) - Code integration
- **Common Tools**: `git_status`, `git_add`, `git_commit`, `git_diff`, `git_log`, `git_branch`

### Slack MCP Server  
- **Source**: https://github.com/korotovsky/slack-mcp-server
- **Package**: `uvx slack-mcp-server`
- **Environment**: `SLACK_BOT_TOKEN`
- **Used in**:
  - [software-development-assistant](../personas/software-development-assistant/) - Team communication
  - [qa-engineer](../personas/qa-engineer/) - Test reporting
  - [linear-project-manager](../personas/linear-project-manager/) - Project notifications and coordination
- **Common Tools**: `conversations_add_message`, `conversations_history`, `channels_list`, `users_list`, `conversations_create`, `reactions_add`

### Linear MCP Server
- **Source**: https://github.com/modelcontextprotocol/servers
- **Package**: `npx -y @modelcontextprotocol/server-linear`
- **Environment**: `LINEAR_API_KEY`
- **Used in**:
  - [linear-project-manager](../personas/linear-project-manager/) - Issue tracking
- **Common Tools**: `list_teams`, `list_projects`, `create_issue`, `update_issue`

### GitHub MCP Server
- **Source**: https://github.com/github/github-mcp-server
- **Package**: `npx -y @modelcontextprotocol/server-github`
- **Environment**: `GITHUB_PERSONAL_ACCESS_TOKEN`
- **Used in**:
  - [linear-project-manager](../personas/linear-project-manager/) - Code integration
- **Common Tools**: `create_issue`, `list_pull_requests`, `get_pull_request`, `create_pull_request_comment`, `list_repositories`, `get_repository`

### Trello MCP Server
- **Source**: https://github.com/modelcontextprotocol/servers  
- **Package**: `npx -y @modelcontextprotocol/server-trello`
- **Environment**: `TRELLO_API_KEY`, `TRELLO_TOKEN`
- **Used in**:
  - [trello-project-manager](../personas/trello-project-manager/) - Board management
- **Common Tools**: `list_boards`, `create_card`, `update_card`, `move_card`

### Filesystem MCP Server
- **Source**: https://github.com/modelcontextprotocol/servers/tree/main/src/filesystem
- **Package**: `npx -y @modelcontextprotocol/server-filesystem`
- **Environment**: None required
- **Used in**:
  - [intern](../personas/intern/) - File operations
  - [qa-engineer-docs](../personas/qa-engineer-docs/) - Test report generation
  - [linear-project-manager](../personas/linear-project-manager/) - Documentation management
- **Common Tools**: `read_text_file`, `write_file`, `list_directory`, `create_directory`

### Fetch MCP Server
- **Source**: https://github.com/modelcontextprotocol/servers/tree/main/src/fetch
- **Package**: `npx -y @modelcontextprotocol/server-fetch`
- **Environment**: None required
- **Used in**:
  - [intern](../personas/intern/) - Web requests
  - [qa-engineer-docs](../personas/qa-engineer-docs/) - Documentation research
- **Common Tools**: `fetch`

### Memory MCP Server
- **Source**: https://github.com/modelcontextprotocol/servers/tree/main/src/memory
- **Package**: `npx -y @modelcontextprotocol/server-memory`
- **Environment**: None required
- **Used in**:
  - [intern](../personas/intern/) - Knowledge graph for learning and context building
- **Common Tools**: `create_entities`, `add_observations`, `search_nodes`, `read_graph`

### Playwright MCP Server
- **Source**: https://github.com/modelcontextprotocol/servers
- **Package**: `npx -y @modelcontextprotocol/server-playwright`
- **Environment**: None required
- **Used in**:
  - [qa-engineer](../personas/qa-engineer/) - Browser automation
  - [qa-engineer-docs](../personas/qa-engineer-docs/) - Test automation and documentation
- **Common Tools**: `navigate`, `click`, `fill`, `screenshot`, `evaluate`, `wait`

### Docker MCP Server
- **Source**: https://github.com/QuantGeekDev/docker-mcp
- **Package**: `npx -y docker-mcp`
- **Environment**: None required
- **Used in**:
  - [qa-engineer](../personas/qa-engineer/) - Container testing
- **Common Tools**: `list_containers`, `create_container`, `start_container`

---

## Cross-Reference Matrix

| Persona | Git | Slack | Linear | GitHub | Trello | Filesystem | Fetch | Memory | Playwright | Docker |
|---------|-----|-------|--------|--------|--------|------------|-------|---------|------------|--------|
| software-development-assistant | ✅ | ✅ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ |
| intern | ✅ | ❌ | ❌ | ❌ | ❌ | ✅ | ✅ | ✅ | ❌ | ❌ |
| linear-project-manager | ❌ | ✅ | ✅ | ✅ | ❌ | ✅ | ❌ | ❌ | ❌ | ❌ |
| trello-project-manager | ❌ | ❌ | ❌ | ❌ | ✅ | ❌ | ❌ | ❌ | ❌ | ❌ |
| qa-engineer | ❌ | ✅ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ✅ | ✅ |
| qa-engineer-docs | ❌ | ❌ | ❌ | ❌ | ❌ | ✅ | ✅ | ❌ | ✅ | ❌ |

---

## Maintenance Notes

### Server Status
- All servers are actively maintained
- No deprecated servers in use
- All packages verified as installable

### Consistency Issues
- Tool naming verified across all personas
- Environment variables consistently use placeholders
- All installations use remote runners

### Updates Needed
- None currently identified

---

## Usage Guidelines

### For Persona Developers
- Check this document before adding new servers to personas
- Ensure consistent tool naming when using existing servers
- Update this document when adding/removing server usage

### For Validation
- Cross-reference tool names against this registry
- Verify environment variable consistency
- Check for orphaned server references

---

*This document is automatically updated during persona validation.*