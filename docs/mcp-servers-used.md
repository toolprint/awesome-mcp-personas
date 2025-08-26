# MCP Servers in Active Use

> Cross-reference of MCP servers currently used in personas
> **Last Updated**: 2025-08-25

## Summary

| Total Servers | Total Personas | Most Used Server |
|---------------|----------------|------------------|
| 8 | 5 | Git (3 personas) |

---
what
## Active Servers by Usage

### High Usage (3+ personas)
| Server | Package | Personas Count | Environment |
|--------|---------|----------------|-------------|
| **Git** | `uvx mcp-server-git` | 3 | None |

### Medium Usage (2 personas)
| Server | Package | Personas Count | Environment |
|--------|---------|----------------|-------------|
| **Slack** | `uvx slack-mcp-server` | 2 | `SLACK_BOT_TOKEN` |

### Low Usage (1 persona)
| Server | Package | Personas Count | Environment |
|--------|---------|----------------|-------------|
| **Linear** | `npx -y @modelcontextprotocol/server-linear` | 1 | `LINEAR_API_KEY` |
| **Trello** | `npx -y @modelcontextprotocol/server-trello` | 1 | `TRELLO_API_KEY`, `TRELLO_TOKEN` |
| **Filesystem** | `npx -y @modelcontextprotocol/server-filesystem` | 1 | None |
| **Fetch** | `npx -y @modelcontextprotocol/server-fetch` | 1 | None |
| **Memory** | `npx -y @modelcontextprotocol/server-memory` | 1 | None |
| **Playwright** | `npx -y @modelcontextprotocol/server-playwright` | 1 | None |
| **Docker** | `npx -y @modelcontextprotocol/server-docker` | 1 | None |

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
- **Common Tools**: `git_status`, `git_add`, `git_commit`, `git_diff`, `git_log`

### Slack MCP Server  
- **Source**: https://github.com/korotovsky/slack-mcp-server
- **Package**: `uvx slack-mcp-server`
- **Environment**: `SLACK_BOT_TOKEN`
- **Used in**:
  - [software-development-assistant](../personas/software-development-assistant/) - Team communication
  - [qa-engineer](../personas/qa-engineer/) - Test reporting
- **Common Tools**: `conversations_add_message`, `conversations_history`, `channels_list`

### Linear MCP Server
- **Source**: https://github.com/modelcontextprotocol/servers
- **Package**: `npx -y @modelcontextprotocol/server-linear`
- **Environment**: `LINEAR_API_KEY`
- **Used in**:
  - [linear-project-manager](../personas/linear-project-manager/) - Issue tracking
- **Common Tools**: `list_teams`, `list_projects`, `create_issue`, `update_issue`

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
- **Common Tools**: `read`, `write`, `list`, `create_directory`

### Fetch MCP Server
- **Source**: https://github.com/modelcontextprotocol/servers/tree/main/src/fetch
- **Package**: `npx -y @modelcontextprotocol/server-fetch`
- **Environment**: None required
- **Used in**:
  - [intern](../personas/intern/) - Web requests
- **Common Tools**: `fetch`, `get`

### Memory MCP Server
- **Source**: https://github.com/modelcontextprotocol/servers/tree/main/src/memory
- **Package**: `npx -y @modelcontextprotocol/server-memory`
- **Environment**: None required
- **Used in**:
  - [intern](../personas/intern/) - Data persistence
- **Common Tools**: `store`, `retrieve`, `search`

### Playwright MCP Server
- **Source**: https://github.com/modelcontextprotocol/servers
- **Package**: `npx -y @modelcontextprotocol/server-playwright`
- **Environment**: None required
- **Used in**:
  - [qa-engineer](../personas/qa-engineer/) - Browser automation
- **Common Tools**: `navigate`, `click`, `fill`, `screenshot`

### Docker MCP Server
- **Source**: https://github.com/modelcontextprotocol/servers
- **Package**: `npx -y @modelcontextprotocol/server-docker`
- **Environment**: None required
- **Used in**:
  - [qa-engineer](../personas/qa-engineer/) - Container testing
- **Common Tools**: `list_containers`, `create_container`, `start_container`

---

## Cross-Reference Matrix

| Persona | Git | Slack | Linear | Trello | Filesystem | Fetch | Memory | Playwright | Docker |
|---------|-----|-------|--------|--------|------------|-------|---------|------------|--------|
| software-development-assistant | ✅ | ✅ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ |
| intern | ✅ | ❌ | ❌ | ❌ | ✅ | ✅ | ✅ | ❌ | ❌ |
| linear-project-manager | ✅ | ❌ | ✅ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ |
| trello-project-manager | ❌ | ❌ | ❌ | ✅ | ❌ | ❌ | ❌ | ❌ | ❌ |
| qa-engineer | ❌ | ✅ | ❌ | ❌ | ❌ | ❌ | ❌ | ✅ | ✅ |

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