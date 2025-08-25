# MCP Servers Registry

> Comprehensive list of Model Context Protocol servers from various registries
> **Last Updated**: 2025-08-25

## Table of Contents

- [Official Servers](#official-servers)
- [Company-Maintained Servers](#company-maintained-servers)
- [Browser & Automation](#browser--automation)
- [Communication & Messaging](#communication--messaging)
- [Data & Analytics](#data--analytics)
- [Development Tools](#development-tools)
- [DevOps & Infrastructure](#devops--infrastructure)
- [Documentation & Content](#documentation--content)
- [File & Storage](#file--storage)
- [Project Management](#project-management)
- [Search & Research](#search--research)
- [Security & Compliance](#security--compliance)
- [Testing & Quality](#testing--quality)
- [Utility Servers](#utility-servers)

---

## Official Servers

Servers maintained by the Model Context Protocol team.

### Core Reference Servers

| Server | Description | Installation | Repository |
|--------|-------------|--------------|------------|
| **Everything** | Reference/test server with prompts, resources, and tools | `npx -y @modelcontextprotocol/server-everything` | [GitHub](https://github.com/modelcontextprotocol/servers/tree/main/src/everything) |
| **Fetch** | Web content fetching and conversion for efficient LLM usage | `npx -y @modelcontextprotocol/server-fetch` | [GitHub](https://github.com/modelcontextprotocol/servers/tree/main/src/fetch) |
| **Filesystem** | Secure file operations with configurable access controls | `npx -y @modelcontextprotocol/server-filesystem` | [GitHub](https://github.com/modelcontextprotocol/servers/tree/main/src/filesystem) |
| **Git** | Tools to read, search, and manipulate Git repositories | `uvx mcp-server-git` | [GitHub](https://github.com/modelcontextprotocol/servers/tree/main/src/git) |
| **Memory** | Knowledge graph-based persistent memory system | `npx -y @modelcontextprotocol/server-memory` | [GitHub](https://github.com/modelcontextprotocol/servers/tree/main/src/memory) |
| **Sequential Thinking** | Dynamic and reflective problem-solving through thought sequences | `npx -y @modelcontextprotocol/server-sequentialthinking` | [GitHub](https://github.com/modelcontextprotocol/servers/tree/main/src/sequentialthinking) |
| **Time** | Time and timezone conversion capabilities | `npx -y @modelcontextprotocol/server-time` | [GitHub](https://github.com/modelcontextprotocol/servers/tree/main/src/time) |

---

## Company-Maintained Servers

Official servers maintained by companies for their services.

| Server | Company | Description | Installation | Repository |
|--------|---------|-------------|--------------|------------|
| **GitHub** | GitHub | Official GitHub MCP Server | `npx -y @modelcontextprotocol/server-github` | [GitHub](https://github.com/github/github-mcp-server) |
| **Stripe** | Stripe | Interact with Stripe API | `npx -y @stripe/agent-toolkit` | [GitHub](https://github.com/stripe/agent-toolkit) |
| **AWS Core** | AWS | Core AWS MCP server with prompt understanding and management | TBD | [GitHub](https://github.com/awslabs/mcp/tree/main/src/core-mcp-server) |
| **Cloudflare** | Cloudflare | Cloudflare API integration | `npx -y @cloudflare/mcp-server` | [GitHub](https://github.com/cloudflare/mcp-server) |
| **Sentry** | Sentry | Sentry error tracking integration | `npx -y @getsentry/mcp-server` | [GitHub](https://github.com/getsentry/mcp-server) |
| **Linear** | Linear | Linear issue tracking integration | `npx -y @modelcontextprotocol/server-linear` | [GitHub](https://github.com/modelcontextprotocol/servers) |
| **Trello** | Atlassian | Trello board management | `npx -y @modelcontextprotocol/server-trello` | [GitHub](https://github.com/modelcontextprotocol/servers) |

---

## Browser & Automation

| Server | Description | Installation | Repository |
|--------|-------------|--------------|------------|
| **Playwright** | Browser automation and web scraping | `npx -y @modelcontextprotocol/server-playwright` | [GitHub](https://github.com/executeautomation/playwright-mcp-server) |
| **Browser MCP** | Automate your local browser | TBD | [GitHub](https://github.com/browsermcp/mcp) |
| **Browser Control** | Browser extension for LLM control | TBD | [GitHub](https://github.com/eyalzh/browser-control-mcp) |
| **Puppeteer** | Chrome/Chromium browser automation | `npx -y @modelcontextprotocol/server-puppeteer` | [GitHub](https://github.com/modelcontextprotocol/servers) |

---

## Communication & Messaging

| Server | Description | Installation | Repository |
|--------|-------------|--------------|------------|
| **Slack** | Slack messaging integration | `uvx slack-mcp-server` | [GitHub](https://github.com/korotovsky/slack-mcp-server) |
| **Telegram** | Telegram API integration | Various implementations | [GitHub](https://github.com/chaindead/telegram-mcp) |
| **Discord** | Discord bot and messaging | TBD | Community implementations |
| **Email** | Email sending and management | TBD | Community implementations |
| **Carbon Voice** | Voice message management | TBD | [GitHub](https://github.com/PhononX/cv-mcp-server) |

---

## Data & Analytics

| Server | Description | Installation | Repository |
|--------|-------------|--------------|------------|
| **PostgreSQL** | PostgreSQL database integration | `npx -y @modelcontextprotocol/server-postgres` | [GitHub](https://github.com/modelcontextprotocol/servers) |
| **SQLite** | SQLite database operations | `npx -y @modelcontextprotocol/server-sqlite` | [GitHub](https://github.com/modelcontextprotocol/servers) |
| **BigQuery** | Google BigQuery integration | TBD | [GitHub](https://github.com/LucasHild/mcp-server-bigquery) |
| **MongoDB** | MongoDB database operations | TBD | Community implementations |
| **MySQL** | MySQL database integration | TBD | Community implementations |
| **Tinybird** | Real-time data analytics | TBD | [GitHub](https://github.com/tinybirdco/mcp-tinybird) |
| **Qdrant** | Vector database operations | TBD | [GitHub](https://github.com/qdrant/mcp-server) |

---

## Development Tools

| Server | Description | Installation | Repository |
|--------|-------------|--------------|------------|
| **Git** | Version control operations | `uvx mcp-server-git` | [GitHub](https://github.com/modelcontextprotocol/servers) |
| **GitHub** | GitHub API integration | `npx -y @modelcontextprotocol/server-github` | [GitHub](https://github.com/github/github-mcp-server) |
| **GitLab** | GitLab API integration | TBD | Community implementations |
| **npm** | Node package management | TBD | Community implementations |
| **TypeScript** | TypeScript analysis tools | TBD | Community implementations |
| **Python** | Python code execution | TBD | Community implementations |

---

## DevOps & Infrastructure

| Server | Description | Installation | Repository |
|--------|-------------|--------------|------------|
| **Docker** | Docker container management | `npx -y @modelcontextprotocol/server-docker` | [GitHub](https://github.com/QuantGeekDev/docker-mcp) |
| **Kubernetes** | Kubernetes cluster management | TBD | Community implementations |
| **AWS** | Amazon Web Services integration | TBD | [GitHub](https://github.com/awslabs/mcp) |
| **Azure** | Microsoft Azure integration | TBD | Community implementations |
| **GCP** | Google Cloud Platform | TBD | Community implementations |
| **Terraform** | Infrastructure as Code | TBD | Community implementations |
| **Ansible** | Configuration management | TBD | Community implementations |

---

## Documentation & Content

| Server | Description | Installation | Repository |
|--------|-------------|--------------|------------|
| **Notion** | Notion workspace integration | TBD | [GitHub](https://github.com/NotionAI/mcp-server) |
| **Confluence** | Atlassian Confluence | TBD | [GitHub](https://github.com/atlassian/mcp-confluence) |
| **Markdown** | Markdown processing | TBD | Community implementations |
| **Wiki** | Wiki management | TBD | Community implementations |
| **Reader** | Content reading and parsing | `npx -y @modelcontextprotocol/server-reader` | [GitHub](https://github.com/modelcontextprotocol/servers) |

---

## File & Storage

| Server | Description | Installation | Repository |
|--------|-------------|--------------|------------|
| **Filesystem** | Local file operations | `npx -y @modelcontextprotocol/server-filesystem` | [GitHub](https://github.com/modelcontextprotocol/servers) |
| **S3** | Amazon S3 storage | TBD | Community implementations |
| **Google Drive** | Google Drive integration | TBD | Community implementations |
| **Dropbox** | Dropbox file management | TBD | Community implementations |
| **OneDrive** | Microsoft OneDrive | TBD | Community implementations |

---

## Project Management

| Server | Description | Installation | Repository |
|--------|-------------|--------------|------------|
| **Jira** | Atlassian Jira integration | `npx jira-mcp-server` | [GitHub](https://github.com/tom28881/mcp-jira-server) |
| **Linear** | Linear issue tracking | `npx -y @modelcontextprotocol/server-linear` | [GitHub](https://github.com/modelcontextprotocol/servers) |
| **Trello** | Trello board management | `npx -y @modelcontextprotocol/server-trello` | [GitHub](https://github.com/modelcontextprotocol/servers) |
| **Asana** | Asana task management | TBD | Community implementations |
| **Monday** | Monday.com integration | TBD | Community implementations |

---

## Search & Research

| Server | Description | Installation | Repository |
|--------|-------------|--------------|------------|
| **Brave Search** | Brave search engine | TBD | [GitHub](https://github.com/brave/mcp-server) |
| **Google Search** | Google search integration | TBD | Community implementations |
| **Perplexity** | Perplexity AI search | TBD | Community implementations |
| **Wikipedia** | Wikipedia content access | TBD | Community implementations |
| **Arxiv** | Academic paper search | TBD | Community implementations |

---

## Security & Compliance

| Server | Description | Installation | Repository |
|--------|-------------|--------------|------------|
| **Sentry** | Error tracking and monitoring | `npx -y @getsentry/mcp-server` | [GitHub](https://github.com/getsentry/mcp-server) |
| **Vault** | HashiCorp Vault secrets | TBD | Community implementations |
| **1Password** | Password management | TBD | Community implementations |
| **Security Scanner** | Security vulnerability scanning | TBD | Community implementations |

---

## Testing & Quality

| Server | Description | Installation | Repository |
|--------|-------------|--------------|------------|
| **Playwright** | E2E testing and automation | `npx -y @modelcontextprotocol/server-playwright` | [GitHub](https://github.com/executeautomation/playwright-mcp-server) |
| **Jest** | JavaScript testing | TBD | Community implementations |
| **Pytest** | Python testing | TBD | Community implementations |
| **Cypress** | E2E testing framework | TBD | Community implementations |

---

## Utility Servers

| Server | Description | Installation | Repository |
|--------|-------------|--------------|------------|
| **Time** | Time and timezone utilities | `npx -y @modelcontextprotocol/server-time` | [GitHub](https://github.com/modelcontextprotocol/servers) |
| **Memory** | Persistent memory system | `npx -y @modelcontextprotocol/server-memory` | [GitHub](https://github.com/modelcontextprotocol/servers) |
| **Calculator** | Mathematical calculations | TBD | Community implementations |
| **Weather** | Weather information | TBD | Community implementations |
| **Currency** | Currency conversion | TBD | Community implementations |

---

## Aggregators & Meta-Servers

| Server | Description | Installation | Repository |
|--------|-------------|--------------|------------|

---

## Notes

### Installation Methods

- **NPM/NPX**: For TypeScript/Node.js servers
  - Install globally: `npm install -g @package/name`
  - Run directly: `npx -y @package/name`

- **Python/UVX**: For Python servers
  - Install: `pip install mcp-server-name`
  - Run with uv: `uvx mcp-server-name`

### Environment Variables

Most servers require environment variables for authentication. Always use placeholders in configuration:
```json
{
  "env": {
    "API_KEY": "<placeholder>"
  }
}
```

### Sources

This list is compiled from:
- [wong2/awesome-mcp-servers](https://github.com/wong2/awesome-mcp-servers)
- [punkpeye/awesome-mcp-servers](https://github.com/punkpeye/awesome-mcp-servers)
- [Official MCP Repository](https://github.com/modelcontextprotocol/servers)
- [Model Context Protocol Examples](https://modelcontextprotocol.io/examples)
- Community contributions

### Contributing

When adding new servers to this list:
1. Verify the server is actively maintained
2. Test the installation command
3. Confirm the repository URL is correct
4. Note any special requirements or dependencies

---

*Last updated: 2025-08-25*
*This is a living document - servers may be added, removed, or updated as the MCP ecosystem evolves.*