# Awesome MCP Personas [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated collection of persona-based MCP (Model Context Protocol) server configurations and toolsets for Claude

## What is this?

Awesome MCP Personas provides pre-configured collections of MCP servers and tools organized by professional personas and use cases. Think of each persona as an installable package that bundles together the most effective MCP servers and tools for specific roles - like having a specialized Claude subagent with the perfect toolkit for your needs.

Whether you're a software engineer, data scientist, DevOps engineer, or content creator, you can find (or contribute) a persona configuration that includes all the MCP servers and tools optimized for your workflow.

## Why Personas?

Instead of manually configuring individual MCP servers and figuring out which tools work well together, personas provide:
- **Pre-configured toolsets** optimized for specific roles and workflows
- **Best practice combinations** of MCP servers that complement each other
- **Quick setup** with tested configurations
- **Community-driven improvements** from professionals in each field

## Table of Contents

- [Installation](#installation)
- [Personas](#personas)
  - [Software Engineering](#software-engineering)
  - [Data Science & Analytics](#data-science--analytics)
  - [DevOps & Infrastructure](#devops--infrastructure)
  - [Content & Documentation](#content--documentation)
  - [Security & Compliance](#security--compliance)
  - [Research & Analysis](#research--analysis)
- [Creating a Persona](#creating-a-persona)
- [Contributing](#contributing)
- [Resources](#resources)

## Installation

### Option 1: Using hypertool-mcp (Recommended)

Install [hypertool-mcp](https://github.com/toolprint/hypertool-mcp) to use personas with full toolset support:
1. Update your project's MCP configuration to use `hypertool-mcp`.
```json
{
  "mcpServers": {
    "hypertool": {
      "command": "npx",
      "args": ["-y", "@toolprint/hypertool-mcp", "--persona", "software-engineer"]
    }
  }
}
```

2. Hypertool will install the persona definition and you can update the servers using `npx -y @toolprint/hypertool --help`.

More information on installing it for various apps such as `Cursor` can be found [**here**](https://github.com/toolprint/hypertool-mcp/tree/feat/persona-content-pack?tab=readme-ov-file#-quick-start).

### Option 2: Manual MCP Configuration

You can copy the `mcp.json` directly to your project:
**Claude Code Example**
```bash
# Copy MCP server configuration
cp personas/simpleton/mcp.json <your_project_path>/.mcp.json
```

**Cursor Example**
```bash
# Copy MCP server configuration
cp personas/simpleton/mcp.json ~/.cursor/mcp.json
```

**Note**: This method only copies the MCP server configurations. You'll need to manually manage toolsets and tool organization defined in `persona.yaml`.

## Personas

### Software Engineering

#### 🛠️ [Full-Stack Developer](./personas/fullstack-developer/)
A comprehensive toolkit for modern web development
- **MCP Servers**: filesystem, git, github, npm, typescript-analyzer
- **Key Features**: Code navigation, version control, package management, type checking
- **Best For**: Web applications, API development, frontend/backend integration

#### 🐍 [Python Developer](./personas/python-developer/)
Optimized for Python development and data engineering
- **MCP Servers**: filesystem, git, python-executor, pytest, pip
- **Key Features**: Python execution, testing, package management, virtual environments
- **Best For**: Python applications, scripts, data processing

#### 🦀 [Rust Developer](./personas/rust-developer/)
Tailored for systems programming with Rust
- **MCP Servers**: filesystem, git, cargo, rust-analyzer
- **Key Features**: Cargo integration, memory safety checks, performance profiling
- **Best For**: Systems programming, performance-critical applications

### Data Science & Analytics

#### 🐘 [PostgreSQL DBA](./personas/postgresql-dba/)
Production PostgreSQL database administration and performance optimization
- **MCP Servers**: postgres, postgresql-ops, antv-chart, vchart, filesystem, git, memory, time
- **Key Features**: Advanced PostgreSQL monitoring, query optimization, performance visualization, enterprise scaling
- **Best For**: Production PostgreSQL administration, database performance tuning, enterprise PostgreSQL deployments

#### 🐬 [MySQL DBA](./personas/mysql-dba/)
Production MySQL database administration with web application focus
- **MCP Servers**: mysql, antv-chart, vchart, filesystem, git, memory, time
- **Key Features**: MySQL optimization, LAMP/LEMP stack integration, e-commerce database management, replication monitoring
- **Best For**: Web application databases, MySQL administration, high-traffic MySQL environments

#### 🪶 [SQLite Engineer](./personas/sqlite-engineer/)
Local development and embedded systems database management
- **MCP Servers**: sqlite, antv-chart, filesystem, git, memory, time
- **Key Features**: Local database development, mobile app integration, embedded systems, rapid prototyping
- **Best For**: Mobile applications, desktop software, embedded systems, data analysis prototyping

#### 📊 [Data Scientist](./personas/data-scientist/)
Complete toolkit for data analysis and machine learning
- **MCP Servers**: jupyter, pandas-helper, matplotlib, scikit-learn
- **Key Features**: Notebook execution, data visualization, ML model training
- **Best For**: Data analysis, machine learning, statistical modeling

#### 📈 [Business Analyst](./personas/business-analyst/)
Tools for business intelligence and reporting
- **MCP Servers**: sql-query, excel-handler, powerbi-connector
- **Key Features**: Database queries, spreadsheet manipulation, BI integration
- **Best For**: Business reporting, data extraction, dashboard creation

### DevOps & Infrastructure

#### ☁️ [Cloud Engineer](./personas/cloud-engineer/)
Multi-cloud infrastructure management
- **MCP Servers**: aws-cli, terraform, kubernetes, docker
- **Key Features**: Cloud resource management, IaC, container orchestration
- **Best For**: Cloud deployments, infrastructure automation

#### 🔧 [Site Reliability Engineer](./personas/sre/)
Monitoring and reliability tools
- **MCP Servers**: prometheus, grafana, pagerduty, logging
- **Key Features**: Metrics collection, alerting, incident managementcc
- **Best For**: System monitoring, incident response, reliability improvements

#### 📊 [Grafana-focused SRE](./personas/grafana-sre/)
Specialized SRE toolkit for Grafana-based monitoring and observability
- **MCP Servers**: filesystem, git, prometheus, docker, postgresql, slack
- **Key Features**: Dashboard management, alert configuration, incident response, monitoring-as-code
- **Best For**: Grafana-centric monitoring, observability automation, SLI/SLO tracking

### Content & Documentation

#### ✍️ [Technical Writer](./personas/technical-writer/)
Documentation and content creation tools
- **MCP Servers**: markdown-editor, grammar-check, diagram-generator
- **Key Features**: Documentation generation, grammar checking, diagram creation
- **Best For**: API documentation, user guides, technical articles

#### 🎨 [Content Creator](./personas/content-creator/)
Multimedia content production
- **MCP Servers**: image-editor, video-tools, social-media
- **Key Features**: Image manipulation, video editing, social media posting
- **Best For**: Blog posts, social media content, multimedia production

### Security & Compliance

#### 🔒 [Security Engineer](./personas/security-engineer/)
Security assessment and hardening tools
- **MCP Servers**: vulnerability-scanner, secrets-detector, compliance-checker
- **Key Features**: Security scanning, secret detection, compliance validation
- **Best For**: Security audits, vulnerability assessment, compliance checks

### Research & Analysis

#### 🔬 [Research Analyst](./personas/research-analyst/)
Information gathering and analysis tools
- **MCP Servers**: web-scraper, citation-manager, data-extractor
- **Key Features**: Web scraping, reference management, data extraction
- **Best For**: Market research, academic research, competitive analysis

## Creating a Persona

### Quick Start with Claude Code

If you're using Claude Code, simply run:
```
/new-persona
```
Claude will guide you through creating a properly formatted persona with all required files.

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
│   └── README.md         # Persona documentation (recommended)
```

### Example Configuration

See the [schema/example/](./schema/example/) directory for complete examples of:
- `persona.yaml` - Persona definition with toolsets
- `mcp.json` - MCP server configurations

For detailed schema documentation, refer to the [schema/README.md](./schema/README.md).

## Contributing

We welcome contributions! Here's how you can help:

1. **Add a new persona**: Create a new persona configuration for your profession or use case
2. **Improve existing personas**: Enhance configurations with better tool combinations
3. **Share workflows**: Add example workflows and best practices
4. **Fix issues**: Help maintain and update existing personas

Please see [CONTRIBUTING.md](./CONTRIBUTING.md) for detailed guidelines.

### Submission Guidelines

- Ensure your persona has a clear, specific use case
- Test the configuration before submitting
- Include comprehensive documentation
- Follow the established directory structure
- Add your persona to the appropriate category in this README

## Resources

### Related Projects
- [Awesome MCP Servers](https://github.com/punkpeye/awesome-mcp-servers) - Comprehensive list of MCP servers
- [Awesome Claude Code Agents](https://github.com/hesreallyhim/awesome-claude-code-agents) - Collection of Claude Code agents
- [MCP Documentation](https://modelcontextprotocol.io/) - Official MCP documentation

### Community
- [Discord Server](#) - Join our community discussions
- [GitHub Discussions](https://github.com/yourusername/awesome-mcp-personas/discussions) - Ask questions and share ideas

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, the contributors have waived all copyright and related or neighboring rights to this work.

---

*Last updated: 2025-08-25*