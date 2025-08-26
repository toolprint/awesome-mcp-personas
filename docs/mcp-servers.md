# MCP Servers Registry

> Comprehensive list of Model Context Protocol servers from various registries
> **Last Updated**: 2025-08-26

## Table of Contents

- [Official Servers](#official-servers)
- [Company-Maintained Servers](#company-maintained-servers)
- [Browser & Automation](#browser--automation)
- [Communication & Messaging](#communication--messaging)
- [Data & Analytics](#data--analytics)
- [Development Tools](#development-tools)
- [Python Development](#python-development)
- [Rust Development](#rust-development)
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

### Database Visualization & Analytics

| Server | Description | Installation | Repository |
|--------|-------------|--------------|------------|
| **AntV Chart Generator** | 25+ chart types for data visualization and analysis | `npx -y @antvis/mcp-server-chart` | [GitHub](https://github.com/antvis/mcp-server-chart) |
| **VChart Interactive** | Interactive charts with diverse visualization capabilities | `npx -y @visactor/vchart-mcp-server` | [GitHub](https://github.com/VisActor/vchart-mcp-server) |
| **Data Exploration** | Autonomous insights and visualization for CSV datasets | TBD | Community implementations |

### Database Development & Engineering

| Server | Description | Installation | Repository |
|--------|-------------|--------------|------------|
| **Universal Database** | Multi-database support with unified query interface | TBD | [GitHub](https://github.com/mcanalescl/MCP-Servers-Data-Gold) |
| **Multi-Database** | Cross-database queries and unified data infrastructure view | TBD | [GitHub](https://github.com/mcanalescl/MCP-Servers-Data-Gold) |
| **PostgreSQL Operations** | Professional PostgreSQL monitoring and operations with 30+ tools | `uvx git+https://github.com/call518/MCP-PostgreSQL-Ops` | [GitHub](https://github.com/call518/MCP-PostgreSQL-Ops) |
| **MySQL Advanced** | MySQL-specific optimizations, indexing, and performance monitoring | TBD | [GitHub](https://github.com/mcanalescl/MCP-Servers-Data-Gold) |
| **Neo4j Graph** | Graph database schema and read/write Cypher operations | TBD | Community implementations |
| **ClickHouse Analytics** | Query execution for ClickHouse analytical databases | TBD | Community implementations |
| **MotherDuck/DuckDB** | Analytical database with cloud integration and fast queries | TBD | [GitHub](https://github.com/mcanalescl/MCP-Servers-Data-Gold) |
| **Prisma Postgres** | Database management with Prisma ORM integration | TBD | Community implementations |

### Data Transformation & Analytics

| Server | Description | Installation | Repository |
|--------|-------------|--------------|------------|
| **dbt Integration** | Official dbt MCP server for data transformation workflows | TBD | [GitHub](https://github.com/dbt-labs/dbt-mcp) |
| **dbt CLI** | Command-line interface integration for dbt operations | TBD | [GitHub](https://github.com/MammothGrowth/dbt-cli-mcp) |
| **dbt Analytics Agent** | LLM-based agent for automated dbt data analysis | TBD | [GitHub](https://github.com/pragunbhutani/dbt-llm-agent) |

---

## Development Tools

| Server | Description | Installation | Repository |
|--------|-------------|--------------|------------|
| **Git** | Version control operations | `uvx mcp-server-git` | [GitHub](https://github.com/modelcontextprotocol/servers) |
| **GitHub** | GitHub API integration | `npx -y @modelcontextprotocol/server-github` | [GitHub](https://github.com/github/github-mcp-server) |
| **GitLab** | GitLab API integration | TBD | Community implementations |
| **npm** | Node package management | TBD | Community implementations |
| **TypeScript** | TypeScript analysis tools | TBD | Community implementations |
| **Python Tools** | See dedicated Python Development section below | Various | Multiple repositories |
| **Rust Tools** | See dedicated Rust Development section below | Various | Multiple repositories |

---

## Python Development

Servers specifically designed for Python development workflows, testing, and code quality.

### Code Execution & Runtime

| Server | Description | Installation | Repository | Stars |
|--------|-------------|--------------|------------|-------|
| **PRIMS** | Python Runtime Interpreter with secure sandbox execution | Setup: `git clone` → `python setup.py` → `python -m server.main` | [GitHub](https://github.com/hileamlakB/PRIMS) | 40+ |
| **Pydantic AI Python** | WebAssembly-based Python execution with automatic dependency management | `deno run -N -R=node_modules -W=node_modules --node-modules-dir=auto jsr:@pydantic/mcp-run-python` | [GitHub](https://github.com/pydantic/pydantic-ai) | 2.8k+ |
| **Sandbox MCP** | Production-ready Python sandbox with virtual environment support | `uvx git+https://github.com/scooter-lacroix/sandbox-mcp.git` | [GitHub](https://github.com/scooter-lacroix/sandbox-mcp) | 5+ |

#### Tools Available:
- **PRIMS**: `run_code`, `list_dir`, `preview_file`, `persist_artifact`, `mount_file`
- **Pydantic AI Python**: `run_python` with dynamic dependency resolution
- **Sandbox MCP**: `execute`, `shell_execute`, `list_artifacts` (12+ tools total)

### Code Quality & Testing

| Server | Description | Installation | Repository | Stars |
|--------|-------------|--------------|------------|-------|
| **MCP Code Checker** | Pylint and pytest integration with AI-friendly prompts | `uvx git+https://github.com/MarcusJellinghaus/mcp-code-checker.git` | [GitHub](https://github.com/MarcusJellinghaus/mcp-code-checker) | 15+ |

#### Tools Available:
- `run_pylint_check` - Comprehensive code quality analysis
- `run_pytest_check` - Automated test execution and reporting
- `run_all_checks` - Combined pylint and pytest analysis

### Data Science & Jupyter

| Server | Description | Installation | Repository | Stars |
|--------|-------------|--------------|------------|-------|
| **MCPStack Jupyter** | LLM-powered Jupyter notebook operations | `uv add mcpstack-jupyter` or `pip install mcpstack-jupyter` | [GitHub](https://github.com/MCP-Pipeline/mcpstack-jupyter) | 10+ |
| **Jupyter SageMath MCP** | Multi-kernel Jupyter server with SageMath and Python support | `git clone` → `conda env create -f environment.yml` | [GitHub](https://github.com/jxta/jupyter-sage-mcp) | 5+ |

#### Tools Available:
- **MCPStack Jupyter**: Notebook cell management, code execution, markdown insertion
- **Jupyter SageMath**: Mathematical computation, cryptography research, kernel switching

### Web Development & Security

| Server | Description | Installation | Repository | Stars |
|--------|-------------|--------------|------------|-------|
| **PyRASP** | Runtime Application Self Protection for Flask/Django/FastAPI | Contact for installation | [GitHub](https://github.com/rbidou/PyRASP) | 32+ |

#### Features:
- Real-time security monitoring
- Support for Flask, FastAPI, Django frameworks
- ML-based threat detection
- Zero-Trust Application Access

### Environment Management

Python-focused servers include built-in virtual environment support:
- **PRIMS**: Fresh virtual environment per execution
- **Sandbox MCP**: Configurable virtual environment options
- **Pydantic AI Python**: WebAssembly isolation (no traditional venv needed)

### Usage Recommendations

**For Code Execution**: 
- Use **Pydantic AI Python** for secure, isolated execution
- Use **PRIMS** for local development and testing
- Use **Sandbox MCP** for production workloads

**For Code Quality**:
- Use **MCP Code Checker** for comprehensive Python linting and testing

**For Data Science**:
- Use **MCPStack Jupyter** for LLM-driven notebook automation
- Use **Jupyter SageMath MCP** for mathematical research

**For Web Development**:
- Use **PyRASP** for security-focused Flask/Django/FastAPI applications

---

## Rust Development

Servers and tools specifically designed for Rust development workflows, code analysis, and project management.

### Code Agents & Development Assistants

| Server | Description | Installation | Repository | Stars |
|--------|-------------|--------------|------------|-------|
| **Winx Code Agent** | High-performance Rust-based code agent with multi-provider AI integration | `git clone` → `cargo build --release` | [GitHub](https://github.com/gabrielmaialva33/winx-code-agent) | 15+ |
| **Code Assistant** | Multi-modal AI coding assistant with GUI, terminal, and headless modes | `cargo install --git https://github.com/stippi/code-assistant` | [GitHub](https://github.com/stippi/code-assistant) | 91+ |

#### Key Capabilities:
- **Winx Code Agent**: Shell execution, file management, multi-provider AI (DashScope/Qwen3, NVIDIA NIM, Google Gemini), operational modes (wcgw, architect, code_writer)
- **Code Assistant**: Real-time streaming tool execution, cross-platform GUI using Zed's GPUI, adaptive tool syntax, project-specific session management

### Cross-Language Development Tools

| Server | Description | Installation | Repository | Stars |
|--------|-------------|--------------|------------|-------|
| **MCP-JS Sandbox** | Rust-based JavaScript execution sandbox using V8 with persistent heap snapshots | TBD - Contact maintainer | [GitHub](https://github.com/r33drichards/mcp-js) | 5+ |
| **Developer MCP Server** | Comprehensive developer tools with file editing, shell execution, and screen capture | Built with rmcp crate | [GitHub](https://github.com/VertexStudio/developer) | 20+ |

#### Tools Available:
- **MCP-JS Sandbox**: `run_js` with V8 isolation, heap snapshot persistence, synchronous JavaScript execution
- **Developer MCP Server**: `view_file`, `write_file`, `replace_in_file`, `execute_command`, `screenshot`, `undo_edit` (10+ tools total)

### Development Workflow Tools

While no dedicated Cargo or rustc MCP servers exist yet, Rust developers can benefit from these general development tools:

| Category | Recommended Servers | Use Case |
|----------|-------------------|-----------|
| **Version Control** | Git MCP, GitHub MCP | Repository management, CI/CD integration |
| **Code Execution** | Developer MCP Server | Shell command execution for `cargo build`, `cargo test`, `cargo run` |
| **File Management** | Filesystem MCP, Developer MCP Server | Project structure management, source code editing |
| **Documentation** | Reader MCP, Fetch MCP | Rust docs integration, crate documentation |
| **Testing & Quality** | Playwright MCP (for web projects) | E2E testing for Rust web applications |

### Installation Requirements for Rust MCP Servers

Most Rust-based MCP servers require:
- **Rust 1.70+** (latest stable recommended)
- **Cargo** for building and dependency management
- Platform-specific dependencies (see individual repositories)

#### Installation Commands:
```bash
# Winx Code Agent
git clone https://github.com/gabrielmaialva33/winx-code-agent.git
cd winx
cargo build --release

# Code Assistant
cargo install --git https://github.com/stippi/code-assistant

# Developer MCP Server (pre-built binaries available)
# See repository for platform-specific installation
```

### Rust Ecosystem Gaps & Opportunities

The Rust MCP ecosystem is still emerging. Missing but highly valuable servers would include:

**High Priority:**
- **Cargo MCP Server**: Dependency management, version updates, feature flag management
- **rustc Integration**: Compiler error analysis, suggestion application, edition migration
- **Rust Language Server**: rust-analyzer integration for code analysis and refactoring
- **Crate Discovery**: Crates.io search, dependency analysis, compatibility checking

**Medium Priority:**
- **rustfmt/clippy Integration**: Code formatting and linting automation
- **Benchmark Runner**: Cargo bench integration with performance tracking
- **Cross-compilation Helper**: Target management, build optimization
- **Documentation Generator**: rustdoc integration, example testing

**Future Opportunities:**
- **Rust Security Auditor**: `cargo audit` integration, vulnerability scanning
- **Performance Profiler**: Integration with profiling tools like `perf`, `flamegraph`
- **WebAssembly Tools**: `wasm-pack` integration, WASM optimization
- **Embedded Development**: Cross-compilation, target flashing, debugging tools

### Contributing to Rust MCP Ecosystem

The Rust MCP ecosystem would greatly benefit from community contributions. Consider developing:
1. **Cargo wrapper** with dependency management and build optimization
2. **rust-analyzer integration** for advanced code intelligence
3. **Testing automation** with `cargo test` and benchmark runners
4. **Documentation tools** with rustdoc and crate.io integration

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
| **MCP Code Checker** | Python code quality checks with pylint and pytest | `uvx git+https://github.com/MarcusJellinghaus/mcp-code-checker.git` | [GitHub](https://github.com/MarcusJellinghaus/mcp-code-checker) |
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
  - Git install: `uvx git+https://github.com/user/repo.git`

- **Deno**: For modern JavaScript/TypeScript servers
  - Run directly: `deno run [flags] jsr:@package/name`

- **Rust/Cargo**: For Rust-based servers
  - Install from git: `cargo install --git https://github.com/user/repo`
  - Build from source: `git clone` → `cargo build --release`
  - Install from crates.io: `cargo install mcp-server-name`

### Environment Variables

Most servers require environment variables for authentication. Always use placeholders in configuration:
```json
{
  "env": {
    "API_KEY": "<placeholder>"
  }
}
```

### Python-Specific Requirements

For Python MCP servers:
- **Python 3.8+** required for most servers
- **Virtual environments** recommended for isolation
- **uvx** preferred for one-time execution without global installation
- Some servers require **Deno** for WebAssembly-based execution
- **Conda** environments supported by data science servers

### Rust-Specific Requirements

For Rust MCP servers:
- **Rust 1.70+** required (latest stable recommended)
- **Cargo** for building and dependency management
- **Git** for source-based installations
- Platform-specific **system libraries** may be required
- **Cross-compilation toolchains** for target-specific builds

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

*Last updated: 2025-08-26*
*This is a living document - servers may be added, removed, or updated as the MCP ecosystem evolves.*