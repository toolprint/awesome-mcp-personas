<div align="center">

# 🎭 Awesome MCP Personas
[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

### 🚀 Stop juggling individual MCP servers — Get a complete AI toolkit for your role in seconds

[![MCP Compatible](https://img.shields.io/badge/MCP-Compatible-green?style=flat-square)](https://modelcontextprotocol.io)
[![Total Personas](https://img.shields.io/badge/Personas-16-blue?style=flat-square)](#-personas-catalog)
[![MCP Servers](https://img.shields.io/badge/MCP%20Servers-33%2B-orange?style=flat-square)](#-personas-catalog)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=flat-square)](https://opensource.org/licenses/MIT)
[![Hypertool MCP](https://img.shields.io/badge/Powered%20by-Hypertool%20MCP-blue?style=flat-square)](https://github.com/toolprint/hypertool-mcp)
[![Claude Compatible](https://img.shields.io/badge/Claude-Compatible-purple?style=flat-square)](https://claude.ai)
[![Cursor Compatible](https://img.shields.io/badge/Cursor-Compatible-teal?style=flat-square)](https://cursor.sh)

</div>

---

## 🤔 What's an MCP Persona?

If you've been **manually copying `mcp.json` files** and wondering which MCP servers work well together, **personas solve that problem**. 

Instead of this tedious process:
```diff
- ❌ Research 50+ individual MCP servers
- ❌ Test which ones work together
- ❌ Configure each server individually  
- ❌ Debug compatibility issues
- ❌ Repeat for every new project
```

**Get this instant setup:**
```diff
+ ✅ Install one persona = get 5-15 perfectly configured MCP servers
+ ✅ Community-created toolkits using validated MCP servers from established registries
+ ✅ Zero compatibility issues, zero debugging
+ ✅ Works immediately in Claude Code, Cursor, Continue, etc.
```

### 🎯 Real Examples

| Your Role | Old Way (Hours) | Persona Way (Seconds) |
|-----------|-----------------|----------------------|
| **Python Developer** | Research filesystem + git + code-checker + sequential-thinking + memory + fetch servers individually | `"persona": "python-backend-engineer"` ✨ |
| **DevOps Engineer** | Configure AWS CLI + CloudFormation + EKS + Docker + Postgres + DynamoDB separately | `"persona": "aws-cloud-engineer"` ✨ |
| **Database Admin** | Set up Postgres + monitoring + charting + git + memory + time servers | `"persona": "postgresql-dba"` ✨ |

## ⚡ Two Ways to Get Started

### 🏃‍♂️ **Quick Start: Copy & Paste (30 seconds)**

Pick a persona from the [catalog below](#-personas-catalog) or browse the [`personas/`](personas/) directory. Start with [`intern`](personas/intern/) if you're new!

#### 🤖 **Claude Code**
```bash
cp personas/intern/mcp.json ~/.config/claude-code/mcp.json
```

#### ⚡ **Cursor**
```bash
cp personas/intern/mcp.json ~/.cursor/mcp.json
```

#### 🔧 **Other Applications**
```bash
# Copy to your application's mcp.json location
cp personas/intern/mcp.json <your-app-config-path>/mcp.json
```

> ⚠️ **Note**: Replace any `<placeholder>` values with your actual credentials.

### 🚀 **Full Features: Hypertool Setup (2 minutes)**

Get access to **complete persona features** including organized toolsets, workflows, and advanced configurations:

```bash
# Step 1: Clone this repository
git clone https://github.com/toolprint/awesome-mcp-personas.git

# Step 2: Install hypertool globally
npm install -g @toolprint/hypertool-mcp@latest

# Step 3: Add a persona (example: intern)
hypertool-mcp persona add ./awesome-mcp-personas/personas/intern

# Step 4: Update your mcp.json
```

Then add this to your `mcp.json`:
```json
{
  "mcpServers": {
    "hypertool": {
      "command": "npx",
      "args": ["-y", "@toolprint/hypertool-mcp", "--persona", "intern"]
    }
  }
}
```

> ✨ **Hypertool Benefits**: Organized toolsets, compound workflows, persona updates, and community-contributed configurations using MCP servers from established registries.

## 🛠️ Application-Specific Installation

### Claude Code
```bash
cp personas/intern/mcp.json <your_project_path>/.mcp.json
```

### Cursor
```bash
cp personas/intern/mcp.json ~/.cursor/mcp.json
```

### Continue (VS Code)
```bash
cp personas/intern/mcp.json ~/.continue/mcp.json
```

> **📍 Quick Reference**: Replace `intern` with any persona name from the catalog below

## 📋 Table of Contents

- [⚡ Two Ways to Get Started](#-two-ways-to-get-started)
- [🛠️ Application-Specific Installation](#️-application-specific-installation)
- [👥 Personas](#-personas)
  - [💻 Software Engineering](#-software-engineering)  
  - [📊 Data Science & Analytics](#-data-science--analytics)
  - [☁️ DevOps & Infrastructure](#️-devops--infrastructure)
  - [✍️ Content & Documentation](#️-content--documentation)
  - [🛡️ Security & Compliance](#️-security--compliance)
  - [🔬 Research & Analysis](#-research--analysis)
  - [📋 Project Management](#-project-management)
  - [🧪 Quality Assurance](#-quality-assurance)
- [📝 Creating a Persona](#-creating-a-persona)
- [🤝 Contributing](#-contributing)
- [📚 Resources](#-resources)


## 👥 Personas Catalog

### 🏷️ Legend

| Emoji | Meaning | Description |
|-------|---------|-------------|
| 🔐 | **Secrets Required** | Requires API keys, credentials, or sensitive configuration |
| 🌐 | **Remote Services** | Uses external APIs, cloud services, or remote connections |
| 💻 | **Local Only** | Runs entirely locally without external dependencies |
| ⚙️ | **Configuration** | Requires environment variables or configuration setup |
| 🚀 | **Zero Setup** | Works immediately without any configuration |
| 📦 | **External Dependencies** | Requires additional tools or services to be installed |
| 🏢 | **Enterprise** | Designed for production/enterprise environments |

### 💻 Software Engineering

| Persona | Labels | Description | MCP Servers | Best For |
|---------|---------|-------------|------------|----------|
| 🐍 **Python Developer** | 💻🚀 | Optimized for Python development and data engineering | filesystem, git, python-executor, pytest, pip | Python applications, scripts, data processing |
| 🚀 [**Python Backend Engineer**](./personas/python-backend-engineer/) | 💻🚀 | Python-focused backend development with code analysis and testing | filesystem, code-checker, sequential-thinking, git, memory, fetch | Python web applications, API development, backend services |
| 🤖 [**Claude Code Assistant**](./personas/claude-code-assistant/) | 💻🚀 | AI-powered coding assistant for Claude Code users | filesystem, git, sequential-thinking, memory, fetch, time | AI-assisted development, code review, intelligent project guidance |
| 💼 [**Software Development Assistant**](./personas/software-development-assistant/) | 💻🚀 | General-purpose software development toolkit | filesystem, git, sequential-thinking, memory, time | General software development, cross-language projects, development workflow automation |
| 🎓 [**Intern**](./personas/intern/) | 💻🚀 | Learning-focused development environment for beginners | filesystem, git, sequential-thinking, memory, time | Learning programming, educational projects, skill development |
| 🎨 [**Web UI Engineer Assistant**](./personas/web-ui-engineer-assistant/) | 🔐⚙️ | Frontend development automation for prototyping, scaffolding, and UI validation | playwright, shadcn-ui, exa-search | Rapid prototyping, component scaffolding, UI testing, design system integration |

### 📊 Data Science & Analytics  

| Persona | Labels | Description | MCP Servers | Best For |
|---------|---------|-------------|------------|----------|
| 🐘 [**PostgreSQL DBA**](./personas/postgresql-dba/) | 🔐⚙️🏢 | Production PostgreSQL database administration and performance optimization | postgres, postgresql-ops, antv-chart, vchart, filesystem, git, memory, time | Production PostgreSQL administration, database performance tuning, enterprise deployments |
| 🐬 [**MySQL DBA**](./personas/mysql-dba/) | 🔐⚙️🏢 | Production MySQL database administration with web application focus | mysql, antv-chart, vchart, filesystem, git, memory, time | Web application databases, MySQL administration, high-traffic MySQL environments |
| 🪶 [**SQLite Engineer**](./personas/sqlite-engineer/) | ⚙️💻 | Local development and embedded systems database management | sqlite, antv-chart, filesystem, git, memory, time | Mobile applications, desktop software, embedded systems, data analysis prototyping |

### ☁️ DevOps & Infrastructure

| Persona | Labels | Description | MCP Servers | Best For |
|---------|---------|-------------|------------|----------|
| ☁️ [**AWS Cloud Engineer**](./personas/aws-cloud-engineer/) | 🔐🌐⚙️🏢 | Comprehensive AWS ecosystem management and automation | aws-cli, aws-api, aws-documentation, aws-cloudformation, aws-cdk, aws-eks, aws-serverless, aws-pricing, filesystem, git, docker, postgres, dynamodb, sequential, time, pulumi | AWS infrastructure management, cloud architecture, enterprise AWS deployments |
| 🌐 [**Cloud Engineer**](./personas/cloud-engineer/) | ⚙️📦 | Multi-cloud infrastructure management and DevOps automation | terraform, kubernetes, docker, filesystem | Cloud-agnostic infrastructure, DevOps workflows, container management |
| 📊 [**Grafana SRE**](./personas/grafana-sre/) | 🔐⚙️🏢 | Specialized SRE toolkit for Grafana-based monitoring and observability | filesystem, git, prometheus, docker, postgresql, slack | Grafana-centric monitoring, observability automation, SLI/SLO tracking |
| 🚀 [**DevOps Engineer Assistant**](./personas/devops-engineer-assistant/) | 🔐🌐⚙️ | Infrastructure automation specialist for safe deployments and incident mitigation | docker, cloudflare, tavily | Deployment automation, incident response, infrastructure management, operational excellence |

### ✍️ Content & Documentation

| Persona | Labels | Description | MCP Servers | Best For |
|---------|---------|-------------|------------|----------|
| 📝 [**QA Engineer - Documentation**](./personas/qa-engineer-docs/) | 💻🚀 | Quality assurance focused on documentation and content validation | filesystem, git, sequential-thinking, memory, time | Documentation quality control, content validation, technical writing QA |

### 🛡️ Security & Compliance

| Persona | Labels | Description | MCP Servers | Best For |
|---------|---------|-------------|------------|----------|
| *Coming Soon* | | | | |

### 🔬 Research & Analysis

| Persona | Labels | Description | MCP Servers | Best For |
|---------|---------|-------------|------------|----------|
| *Coming Soon* | | | | |

### 📋 Project Management

| Persona | Labels | Description | MCP Servers | Best For |
|---------|---------|-------------|------------|----------|
| 📋 [**Linear Project Manager**](./personas/linear-project-manager/) | 🔐🌐⚙️ | Project management integration with Linear issue tracking | linear, filesystem, git, memory, time | Agile project management, Linear-based workflows, development team coordination |
| 🎯 [**Trello Project Manager**](./personas/trello-project-manager/) | 🔐🌐⚙️ | Kanban-style project management with Trello integration | trello, filesystem, git, memory, time | Visual project management, kanban methodology, team collaboration |

### 🧪 Quality Assurance

| Persona | Labels | Description | MCP Servers | Best For |
|---------|---------|-------------|------------|----------|
| 🔍 [**QA Engineer**](./personas/qa-engineer/) | 💻🚀 | Comprehensive quality assurance and testing workflows | filesystem, git, sequential-thinking, memory, time | Software testing, quality assurance, test case management |

## 📝 Creating a Persona

### Quick Start with Claude Code

If you're using Claude Code, simply run:
```
/new-persona
```
Claude will guide you through creating a properly formatted persona with all required files.

After creating your persona, run:
```
/sync-personas
```
This will automatically add your new persona to the README with proper categorization and emoji labeling.

### Manual Creation

Each persona consists of:

1. **persona.yaml** - The persona definition with toolsets and metadata
2. **mcp.json** - The MCP server configuration file  
3. **README.md** - Documentation describing the persona's purpose and usage

### Persona Structure

```
personas/
├── your-persona-name/
│   ├── persona.yaml      # Persona definition (required)
│   ├── mcp.json          # MCP server configuration (required)
│   ├── README.md         # Persona documentation (recommended)
│   ├── tools.md          # Tool reference guide (optional)
│   └── validation_notes.md # Configuration notes (optional)
```

### Example Configuration

See existing personas for complete examples:
- [`python-backend-engineer`](./personas/python-backend-engineer/) - Python-focused backend development with code analysis
- [`postgresql-dba`](./personas/postgresql-dba/) - Complex persona with specialized toolsets
- [`claude-code-assistant`](./personas/claude-code-assistant/) - AI-assisted development persona

## 🤝 Contributing

We welcome contributions! Here's how you can help:

### Ways to Contribute
- 🆕 **Add a new persona**: Create configurations for your profession or use case
- 🔧 **Improve existing personas**: Enhance configurations with better tool combinations  
- 📚 **Share workflows**: Add example workflows and best practices
- 🐛 **Fix issues**: Help maintain and update existing personas
- 📖 **Improve documentation**: Enhance README files and guides

### Submission Guidelines
- Ensure your persona has a clear, specific use case
- Use only validated MCP servers from established registries (see Resources section)
- Test the configuration before submitting  
- Include comprehensive documentation
- Follow the established directory structure
- Add your persona to the appropriate category in this README
- Community review helps ensure quality and compatibility

Please see our [GitHub Issues](https://github.com/toolprint/awesome-mcp-personas/issues) for bug reports and [GitHub Discussions](https://github.com/toolprint/awesome-mcp-personas/discussions) for questions.

## 📚 Resources

### MCP Server Registries
All personas in this repository are community-created with best effort made to ensure that only validated MCP servers from the following established registries are used:

- [Awesome MCP Servers](https://github.com/punkpeye/awesome-mcp-servers) - Comprehensive community-maintained list of MCP servers
- [Model Context Protocol](https://modelcontextprotocol.io/) - Official MCP documentation and server registry
- [Smithery Registry](https://smithery.ai/servers) - Curated registry of MCP servers
- [NPM Registry](https://www.npmjs.com/search?q=mcp%20server) - Published MCP server packages

### Related Projects
- [Hypertool MCP](https://github.com/toolprint/hypertool-mcp) - Persona installation and management tool

### Community
- [GitHub Issues](https://github.com/toolprint/awesome-mcp-personas/issues) - Report bugs or request features
- [GitHub Discussions](https://github.com/toolprint/awesome-mcp-personas/discussions) - Ask questions and share ideas

## 📊 Statistics

![Total Personas](https://img.shields.io/badge/Total%20Personas-16-blue)
![MCP Servers](https://img.shields.io/badge/MCP%20Servers-33%2B-green)
![Categories](https://img.shields.io/badge/Categories-8-purple)
![Open Source](https://img.shields.io/badge/Open%20Source-100%25-brightgreen)

---

<div align="center">
  <p><em>"Built by developers who got tired of watching AI pick the wrong tools 🎯"</em></p>
  
  <img src="https://raw.githubusercontent.com/toolprint/hypertool-mcp/main/assets/toolprint.png" alt="Toolprint Logo" width="120">
  
  <p><strong>Built with ❤️ by <a href="https://github.com/toolprint">Toolprint</a></strong><br>
  © 2025 OneGrep, Inc.</p>
</div>

## License

[![MIT License](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.