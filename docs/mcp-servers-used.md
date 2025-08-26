# MCP Servers in Active Use

> Cross-reference of MCP servers currently used in personas
> **Last Updated**: 2025-08-26

## Summary

| Total Servers | Total Personas | Most Used Server |
|---------------|----------------|------------------|
| 33 | 14 | Git (10 personas) |

---

## Active Servers by Usage

### High Usage (3+ personas)
| Server | Package | Personas Count | Environment |
|--------|---------|----------------|-------------|
| **Git** | `uvx mcp-server-git` | 10 | None |
| **Slack** | `uvx slack-mcp-server` | 3 | `SLACK_BOT_TOKEN` |
| **Filesystem** | `npx -y @modelcontextprotocol/server-filesystem` | 10 | None |

### Medium Usage (2 personas)
| Server | Package | Personas Count | Environment |
|--------|---------|----------------|-------------|
| **Sequential Thinking** | `npx -y @modelcontextprotocol/server-sequentialthinking` | 4 | None |
| **Docker** | `npx -y docker-mcp` | 3 | None |

### Low Usage (1 persona)
| Server | Package | Personas Count | Environment |
|--------|---------|----------------|-------------|
| **Linear** | `npx -y @modelcontextprotocol/server-linear` | 1 | `LINEAR_API_KEY` |
| **GitHub** | `npx -y @modelcontextprotocol/server-github` | 1 | `GITHUB_PERSONAL_ACCESS_TOKEN` |
| **Trello** | `npx -y @modelcontextprotocol/server-trello` | 1 | `TRELLO_API_KEY`, `TRELLO_TOKEN` |
| **Fetch** | `npx -y @modelcontextprotocol/server-fetch` | 3 | None |
| **Memory** | `npx -y @modelcontextprotocol/server-memory` | 7 | None |
| **Playwright** | `npx -y @modelcontextprotocol/server-playwright` | 2 | None |
| **Code Checker** | `uvx mcp-code-checker` | 1 | None |
| **Kubectl** | `uvx kubectl-mcp-tool` | 1 | `KUBECONFIG` |
| **AWS Cloud Control** | `uvx aws-cloud-control-mcp` | 1 | `AWS_ACCESS_KEY_ID`, `AWS_SECRET_ACCESS_KEY`, `AWS_DEFAULT_REGION` |
| **Prometheus** | `uvx --from git+https://github.com/pab1it0/prometheus-mcp-server prometheus-mcp-server` | 1 | `PROMETHEUS_URL` |
| **PostgreSQL** | `npx -y @ahmetkca/mcp-server-postgres` | 3 | `POSTGRES_HOST`, `POSTGRES_PORT`, `POSTGRES_DATABASE`, `POSTGRES_USER`, `POSTGRES_PASSWORD` |
| **MySQL** | `uvx mysql-mcp-server` | 2 | `MYSQL_*` |
| **SQLite** | `uvx mcp-sqlite` | 2 | `SQLITE_DB_PATH` |
| **Time** | `npx -y @modelcontextprotocol/server-time` | 6 | `DEFAULT_TIMEZONE` |
| **PostgreSQL Ops** | `uvx git+https://github.com/call518/MCP-PostgreSQL-Ops` | 1 | `POSTGRES_HOST`, `POSTGRES_PORT`, `POSTGRES_DATABASE`, `POSTGRES_USER`, `POSTGRES_PASSWORD` |
| **Chart** | `npx -y @antvis/mcp-server-chart` | 3 | None |
| **VChart** | `npx -y @visactor/vchart-mcp-server` | 2 | None |
| **AWS Core** | `uvx awslabs.core-mcp-server@latest` | 1 | `AWS_ACCESS_KEY_ID`, `AWS_SECRET_ACCESS_KEY`, `AWS_REGION` |
| **AWS API** | `uvx awslabs.aws-api-mcp-server@latest` | 1 | `AWS_ACCESS_KEY_ID`, `AWS_SECRET_ACCESS_KEY`, `AWS_REGION` |
| **AWS Documentation** | `uvx awslabs.aws-documentation-mcp-server@latest` | 1 | `AWS_REGION` |
| **AWS CloudFormation** | `uvx awslabs.aws-cloudformation-mcp-server@latest` | 1 | `AWS_ACCESS_KEY_ID`, `AWS_SECRET_ACCESS_KEY`, `AWS_REGION` |
| **AWS CDK** | `uvx awslabs.aws-cdk-mcp-server@latest` | 1 | `AWS_ACCESS_KEY_ID`, `AWS_SECRET_ACCESS_KEY`, `AWS_REGION`, `CDK_DEFAULT_ACCOUNT` |
| **AWS EKS** | `uvx awslabs.aws-eks-mcp-server@latest` | 1 | `AWS_ACCESS_KEY_ID`, `AWS_SECRET_ACCESS_KEY`, `AWS_REGION`, `KUBECONFIG` |
| **AWS Serverless** | `uvx awslabs.aws-serverless-mcp-server@latest` | 1 | `AWS_ACCESS_KEY_ID`, `AWS_SECRET_ACCESS_KEY`, `AWS_REGION` |
| **AWS Pricing** | `uvx awslabs.aws-pricing-mcp-server@latest` | 1 | `AWS_REGION` |
| **DynamoDB Toolbox** | `npx dynamodb-toolbox-mcp-server` | 1 | `AWS_ACCESS_KEY_ID`, `AWS_SECRET_ACCESS_KEY`, `AWS_REGION`, `DYNAMODB_TABLE_NAME` |
| **Pulumi** | `uvx pulumi-mcp-server` | 1 | `PULUMI_ACCESS_TOKEN`, `AWS_ACCESS_KEY_ID`, `AWS_SECRET_ACCESS_KEY`, `AWS_REGION` |

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
  - [python-developer](../personas/python-developer/) - Python project version control
  - [python-backend-engineer](../personas/python-backend-engineer/) - Backend development version control
  - [postgres-db-engineer](../personas/postgres-db-engineer/) - Database script version control
  - [cloud-engineer](../personas/cloud-engineer/) - Infrastructure as Code version control
  - [aws-cloud-engineer](../personas/aws-cloud-engineer/) - AWS Infrastructure as Code and configuration management
  - [postgresql-dba](../personas/postgresql-dba/) - Database schema and configuration management
  - [mysql-dba](../personas/mysql-dba/) - MySQL schema and web application database management
  - [sqlite-engineer](../personas/sqlite-engineer/) - Mobile and embedded database schema management and version control
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
  - [python-developer](../personas/python-developer/) - Python file management and project structure
  - [postgres-db-engineer](../personas/postgres-db-engineer/) - Database script and configuration management
  - [cloud-engineer](../personas/cloud-engineer/) - Infrastructure as Code file management
  - [aws-cloud-engineer](../personas/aws-cloud-engineer/) - AWS configuration and CloudFormation template management
  - [postgresql-dba](../personas/postgresql-dba/) - PostgreSQL script and configuration management
  - [mysql-dba](../personas/mysql-dba/) - MySQL script and web application configuration management
  - [sqlite-engineer](../personas/sqlite-engineer/) - SQLite database management, backup files, and project organization
- **Common Tools**: `read_text_file`, `write_file`, `list_directory`, `create_directory`

### Fetch MCP Server
- **Source**: https://github.com/modelcontextprotocol/servers/tree/main/src/fetch
- **Package**: `npx -y @modelcontextprotocol/server-fetch`
- **Environment**: None required
- **Used in**:
  - [intern](../personas/intern/) - Web requests
  - [qa-engineer-docs](../personas/qa-engineer-docs/) - Documentation research
  - [python-backend-engineer](../personas/python-backend-engineer/) - Python documentation and resource research
  - [postgres-db-engineer](../personas/postgres-db-engineer/) - SQL script and configuration management
- **Common Tools**: `fetch`

### Memory MCP Server
- **Source**: https://github.com/modelcontextprotocol/servers/tree/main/src/memory
- **Package**: `npx -y @modelcontextprotocol/server-memory`
- **Environment**: None required
- **Used in**:
  - [intern](../personas/intern/) - Knowledge graph for learning and context building
  - [python-developer](../personas/python-developer/) - Project knowledge and pattern storage
  - [python-backend-engineer](../personas/python-backend-engineer/) - Project insights and architectural knowledge management
  - [postgres-db-engineer](../personas/postgres-db-engineer/) - Database documentation and schema relationships
  - [postgresql-dba](../personas/postgresql-dba/) - PostgreSQL schema relationships and operational documentation
  - [mysql-dba](../personas/mysql-dba/) - MySQL schema documentation and web application database knowledge
  - [sqlite-engineer](../personas/sqlite-engineer/) - SQLite project documentation, schema relationships, and development insights
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
  - [cloud-engineer](../personas/cloud-engineer/) - Container management and orchestration
- **Common Tools**: `list_containers`, `create_container`, `start_container`, `stop_container`, `get_container_logs`, `deploy_compose`


### Code Checker MCP Server
- **Source**: https://github.com/MarcusJellinghaus/mcp-code-checker
- **Package**: `uvx mcp-code-checker`
- **Environment**: None required
- **Used in**:
  - [python-backend-engineer](../personas/python-backend-engineer/) - Python code quality analysis and testing
- **Common Tools**: `run_pylint_check`, `run_pytest_check`, `run_all_checks`

### Sequential Thinking MCP Server
- **Source**: https://github.com/modelcontextprotocol/servers/tree/main/src/sequentialthinking
- **Package**: `npx -y @modelcontextprotocol/server-sequentialthinking`
- **Environment**: None required
- **Used in**:
  - [python-backend-engineer](../personas/python-backend-engineer/) - Complex problem decomposition and systematic analysis
  - [intern](../personas/intern/) - Structured learning and problem-solving
  - [cloud-engineer](../personas/cloud-engineer/) - Infrastructure planning and incident analysis
- **Common Tools**: `create_reasoning_session`, `analyze_step_by_step`, `synthesize_solution`

### PostgreSQL MCP Server
- **Source**: https://github.com/ahmetkca/mcp-server-postgres
- **Package**: `npm exec -- @ahmetkca/mcp-server-postgres`
- **Environment**: `DATABASE_URL`, `POSTGRES_HOST`, `POSTGRES_PORT`, `POSTGRES_DB`, `POSTGRES_USER`, `POSTGRES_PASSWORD`, `POSTGRES_SSL`
- **Used in**:
  - [postgres-db-engineer](../personas/postgres-db-engineer/) - PostgreSQL database administration and operations
  - [postgresql-dba](../personas/postgresql-dba/) - Production PostgreSQL administration with multi-tenant support
- **Common Tools**: `execute_query`, `list_tables`, `describe_table`, `get_schema`, `analyze_query`, `explain_query`, `get_stats`, `list_users`, `check_permissions`

### MySQL MCP Server
- **Source**: https://github.com/mysql/mysql-mcp-server
- **Package**: `uvx mysql-mcp-server`
- **Environment**: `MYSQL_HOST`, `MYSQL_PORT`, `MYSQL_DATABASE`, `MYSQL_USER`, `MYSQL_PASSWORD`, `MYSQL_SSL`
- **Used in**:
  - [postgres-db-engineer](../personas/postgres-db-engineer/) - MySQL database analysis and read-only operations
  - [mysql-dba](../personas/mysql-dba/) - Production MySQL administration with web application focus
- **Common Tools**: `query`, `show_tables`, `describe`, `explain`, `show_status`, `show_grants`

### SQLite MCP Server
- **Source**: https://github.com/sqlite/mcp-sqlite
- **Package**: `uvx mcp-sqlite`
- **Environment**: `SQLITE_DB_PATH`
- **Used in**:
  - [postgres-db-engineer](../personas/postgres-db-engineer/) - Local SQLite database operations and testing
  - [sqlite-engineer](../personas/sqlite-engineer/) - Mobile, desktop, and embedded SQLite development and deployment
- **Common Tools**: `execute`, `list_tables`, `describe_table`, `analyze`, `pragma`

### Time MCP Server
- **Source**: https://github.com/modelcontextprotocol/servers/tree/main/src/time
- **Package**: `npx -y @modelcontextprotocol/server-time`
- **Environment**: `DEFAULT_TIMEZONE`
- **Used in**:
  - [postgres-db-engineer](../personas/postgres-db-engineer/) - Time zone handling for distributed databases
  - [cloud-engineer](../personas/cloud-engineer/) - Deployment scheduling and incident coordination
  - [postgresql-dba](../personas/postgresql-dba/) - PostgreSQL timezone operations and performance tracking
  - [mysql-dba](../personas/mysql-dba/) - MySQL timezone handling for web applications and global e-commerce
  - [sqlite-engineer](../personas/sqlite-engineer/) - SQLite timezone operations for mobile and embedded applications
- **Common Tools**: `get_current_time`, `convert_timezone`, `format_time`, `calculate_duration`

### Kubectl MCP Server
- **Source**: https://github.com/rohitg00/kubectl-mcp-server
- **Package**: `uvx kubectl-mcp-tool`
- **Environment**: `KUBECONFIG`
- **Used in**:
  - [cloud-engineer](../personas/cloud-engineer/) - Kubernetes cluster management and operations
- **Common Tools**: `get_pods`, `get_services`, `describe_resource`, `get_logs`, `scale_deployment`, `port_forward`

### AWS Cloud Control MCP Server
- **Source**: https://github.com/awslabs/mcp
- **Package**: `uvx aws-cloud-control-mcp`
- **Environment**: `AWS_ACCESS_KEY_ID`, `AWS_SECRET_ACCESS_KEY`, `AWS_DEFAULT_REGION`
- **Used in**:
  - [cloud-engineer](../personas/cloud-engineer/) - AWS resource management and provisioning
- **Common Tools**: `create_resource`, `get_resource`, `update_resource`

### Prometheus MCP Server
- **Source**: https://github.com/pab1it0/prometheus-mcp-server
- **Package**: `uvx --from git+https://github.com/pab1it0/prometheus-mcp-server prometheus-mcp-server`
- **Environment**: `PROMETHEUS_URL`
- **Used in**:
  - [cloud-engineer](../personas/cloud-engineer/) - Metrics collection and monitoring analysis
- **Common Tools**: `execute_query`, `execute_range_query`, `list_metrics`, `get_targets`, `get_metric_metadata`

### PostgreSQL Operations MCP Server
- **Source**: https://github.com/call518/MCP-PostgreSQL-Ops
- **Package**: `uvx git+https://github.com/call518/MCP-PostgreSQL-Ops`
- **Environment**: `POSTGRES_HOST`, `POSTGRES_PORT`, `POSTGRES_DATABASE`, `POSTGRES_USER`, `POSTGRES_PASSWORD`
- **Used in**:
  - [postgresql-dba](../personas/postgresql-dba/) - Comprehensive PostgreSQL monitoring and operations with 30+ specialized DBA tools
- **Common Tools**: `monitor_connections`, `check_vacuum_stats`, `get_table_stats`, `monitor_replication`, `check_bloat`, `analyze_slow_queries`, `get_index_usage`, `check_lock_waits`, `monitor_autovacuum`, `check_disk_usage`, `monitor_cpu_usage`, `check_connection_limits`, `monitor_backup_status`, `get_error_log`, `check_security_audit`, `validate_configuration`, `validate_schema`, `generate_migration`

### Chart MCP Server
- **Source**: https://github.com/antvis/mcp-server-chart
- **Package**: `npx -y @antvis/mcp-server-chart`
- **Environment**: None required
- **Used in**:
  - [postgresql-dba](../personas/postgresql-dba/) - Database performance visualization and monitoring charts
  - [mysql-dba](../personas/mysql-dba/) - MySQL performance metrics visualization and web application monitoring
  - [sqlite-engineer](../personas/sqlite-engineer/) - SQLite data analysis visualization and performance monitoring for mobile/embedded systems
- **Common Tools**: `create_line_chart`, `create_bar_chart`, `create_time_series`

### VChart MCP Server
- **Source**: https://github.com/visactor/vchart-mcp-server
- **Package**: `npx -y @visactor/vchart-mcp-server`
- **Environment**: None required
- **Used in**:
  - [postgresql-dba](../personas/postgresql-dba/) - Interactive visualization for complex PostgreSQL performance analysis and dashboards
  - [mysql-dba](../personas/mysql-dba/) - Interactive MySQL dashboards for web application performance and e-commerce monitoring
- **Common Tools**: `create_performance_dashboard`, `create_alert_dashboard`

---

## Cross-Reference Matrix

| Persona | Git | Slack | Linear | GitHub | Trello | Filesystem | Fetch | Memory | Playwright | Docker | Code-Checker | Sequential | PostgreSQL | MySQL | SQLite | Time | Kubectl | AWS | Prometheus | PG-Ops | Chart | VChart |
|---------|-----|-------|--------|--------|--------|------------|-------|---------|------------|--------|-------------|------------|------------|-------|---------|------|---------|-----|------------|--------|-------|-------|
| software-development-assistant | ✅ | ✅ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ |
| intern | ✅ | ❌ | ❌ | ❌ | ❌ | ✅ | ✅ | ✅ | ❌ | ❌ | ❌ | ✅ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ |
| linear-project-manager | ❌ | ✅ | ✅ | ✅ | ❌ | ✅ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ |
| trello-project-manager | ❌ | ❌ | ❌ | ❌ | ✅ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ |
| qa-engineer | ❌ | ✅ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ✅ | ✅ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ |
| qa-engineer-docs | ❌ | ❌ | ❌ | ❌ | ❌ | ✅ | ✅ | ❌ | ✅ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ |
| python-developer | ✅ | ❌ | ❌ | ❌ | ❌ | ✅ | ❌ | ✅ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ |
| python-backend-engineer | ✅ | ❌ | ❌ | ❌ | ❌ | ✅ | ✅ | ✅ | ❌ | ❌ | ✅ | ✅ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ |
| postgres-db-engineer | ✅ | ❌ | ❌ | ❌ | ❌ | ✅ | ❌ | ✅ | ❌ | ❌ | ❌ | ❌ | ✅ | ✅ | ✅ | ✅ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ |
| postgresql-dba | ✅ | ❌ | ❌ | ❌ | ❌ | ✅ | ❌ | ✅ | ❌ | ❌ | ❌ | ❌ | ✅ | ❌ | ❌ | ✅ | ❌ | ❌ | ❌ | ✅ | ✅ | ✅ |
| mysql-dba | ✅ | ❌ | ❌ | ❌ | ❌ | ✅ | ❌ | ✅ | ❌ | ❌ | ❌ | ❌ | ❌ | ✅ | ❌ | ✅ | ❌ | ❌ | ❌ | ✅ | ✅ | ❌ |
| cloud-engineer | ✅ | ❌ | ❌ | ❌ | ❌ | ✅ | ❌ | ❌ | ❌ | ✅ | ❌ | ✅ | ❌ | ❌ | ❌ | ✅ | ✅ | ✅ | ✅ | ❌ | ❌ | ❌ |
| aws-cloud-engineer | ✅ | ❌ | ❌ | ❌ | ❌ | ✅ | ❌ | ❌ | ❌ | ✅ | ❌ | ✅ | ✅ | ❌ | ❌ | ✅ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ |
| sqlite-engineer | ✅ | ❌ | ❌ | ❌ | ❌ | ✅ | ❌ | ✅ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ✅ | ✅ | ❌ | ❌ | ❌ | ❌ | ✅ | ❌ |

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