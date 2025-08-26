# Grafana-focused Site Reliability Engineer

## Overview
A specialized SRE persona focused on monitoring, alerting, and observability using Grafana as the primary platform. This persona extends traditional SRE capabilities with deep Grafana integration for visualization, alerting, and dashboard management.

## Purpose
This persona is designed for Site Reliability Engineers who primarily work with Grafana-based monitoring stacks. It combines traditional SRE monitoring and reliability tools with Grafana-specific capabilities for dashboard creation, alert management, and observability workflows.

## Target Audience
- **Site Reliability Engineers** working with Grafana-based monitoring stacks
- **DevOps Engineers** responsible for observability and monitoring infrastructure
- **Platform Engineers** managing monitoring and alerting systems
- **Operations Engineers** focused on system reliability and incident response

## Core Capabilities

### Monitoring & Observability
- Grafana dashboard creation and management
- Prometheus metrics collection and querying
- Log aggregation and analysis with Loki
- Time-series data visualization and exploration

### Alerting & Incident Response
- Grafana alert rule management and configuration  
- PagerDuty integration for incident escalation
- Notification channel setup and management
- Incident response workflow automation

### Infrastructure Monitoring
- System and application performance monitoring
- Infrastructure health checks and reporting
- Service level indicator (SLI) and objective (SLO) tracking
- Capacity planning and resource optimization

### Data Source Management
- Multiple data source integration (Prometheus, InfluxDB, CloudWatch, etc.)
- Query optimization and performance tuning
- Data retention and storage management
- Cross-platform monitoring integration

## Key Workflows

### Dashboard Development
1. **Create and customize Grafana dashboards** for application and infrastructure monitoring
2. **Build visualization panels** with appropriate chart types and configurations
3. **Template dashboards** for reusable monitoring patterns across services
4. **Export and import dashboards** for version control and sharing

### Alert Management
1. **Configure alert rules** based on metrics thresholds and anomalies
2. **Set up notification channels** for different escalation levels
3. **Manage alert lifecycle** from creation to resolution
4. **Test and validate alert conditions** to reduce false positives

### Incident Response
1. **Monitor system health** through real-time dashboards and alerts
2. **Investigate incidents** using Grafana's data exploration features
3. **Correlate metrics and logs** across different data sources
4. **Document post-incident analysis** with dashboard snapshots and reports

### Platform Operations
1. **Manage Grafana instance** configuration and user access
2. **Optimize query performance** and dashboard load times
3. **Implement backup and disaster recovery** for monitoring infrastructure
4. **Scale monitoring infrastructure** based on usage patterns

## MCP Servers

This persona integrates the following MCP servers to provide comprehensive SRE capabilities:

### Core Infrastructure & Monitoring

**🏗️ Shell Commands Server**
- **Server**: `g0t4/mcp-server-commands`  
- **Installation**: `npx -y @g0t4/mcp-server-commands`
- **Purpose**: Execute system commands for infrastructure management, service monitoring, and automated remediation
- **Key Tools**: `run_command` for system administration, process monitoring, and infrastructure automation
- **SRE Use Cases**: System health checks, service restarts, log file analysis, automated incident response

**📁 Filesystem Server**
- **Server**: `@modelcontextprotocol/server-filesystem`
- **Installation**: `npx -y @modelcontextprotocol/server-filesystem`
- **Purpose**: Manage configuration files, dashboards, and monitoring artifacts
- **Key Tools**: `read_text_file`, `write_file`, `edit_file`, `list_directory`, `search_files`
- **SRE Use Cases**: Dashboard JSON management, configuration file updates, log file analysis, backup operations

**🔀 Git Server**
- **Server**: `@modelcontextprotocol/server-git`
- **Installation**: `uvx mcp-server-git`
- **Purpose**: Version control for monitoring-as-code and infrastructure configurations
- **Key Tools**: `git_status`, `git_commit`, `git_diff`, `git_log`, `git_create_branch`, `git_checkout`
- **SRE Use Cases**: Dashboard version control, configuration management, change tracking, collaborative monitoring development

### Data & Database Integration

**🗄️ Universal Database Server**  
- **Server**: `julien040/anyquery`
- **Installation**: Available through multiple package managers
- **Purpose**: Connect to time-series databases (Prometheus, InfluxDB, TimescaleDB) and other data sources
- **Key Tools**: SQL querying across 40+ data sources including databases, files, and applications
- **SRE Use Cases**: Metrics analysis, historical data queries, multi-source correlation, capacity planning

### Communication & Incident Management

**💬 Slack Integration Server**
- **Server**: `korotovsky/slack-mcp-server`
- **Installation**: Available as MCP server package
- **Purpose**: Automate incident notifications, status updates, and team communication
- **Key Tools**: Message sending, channel management, user notifications, workflow automation
- **SRE Use Cases**: Alert notifications, incident communication, status updates, escalation management

### Advanced Monitoring (When Available)

**📊 Grafana Server** (Community)
- **Server**: Grafana MCP Server (referenced in awesome-mcp-servers)
- **Purpose**: Direct Grafana API integration for dashboard management and data source queries
- **Key Tools**: Dashboard search, incident investigation, datasource queries
- **SRE Use Cases**: Programmatic dashboard management, automated incident investigation, metric exploration

**🚨 Prometheus Alertmanager Server** (Community)
- **Server**: Prometheus Alertmanager MCP Server (referenced in awesome-mcp-servers)  
- **Purpose**: Integration with Prometheus Alertmanager for alert lifecycle management
- **Key Tools**: Alert rule management, notification configuration, alert status monitoring
- **SRE Use Cases**: Alert rule automation, notification channel setup, alert suppression management

### Server Configuration Example

```json
{
  "mcpServers": {
    "filesystem": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-filesystem"],
      "config": {
        "allowedDirectories": ["/opt/grafana/dashboards", "/etc/monitoring", "/var/log"]
      }
    },
    "git": {
      "command": "uvx",
      "args": ["mcp-server-git"]
    },
    "commands": {
      "command": "npx", 
      "args": ["-y", "@g0t4/mcp-server-commands"]
    },
    "database": {
      "command": "anyquery",
      "args": ["mcp", "--stdio"]
    },
    "slack": {
      "command": "npx",
      "args": ["-y", "korotovsky/slack-mcp-server"]
    }
  }
}
```

## Prerequisites
- Basic understanding of Site Reliability Engineering principles
- Experience with monitoring and observability concepts
- Familiarity with Grafana dashboards and alerting
- Knowledge of time-series databases (Prometheus, InfluxDB, etc.)
- Understanding of logging systems and log aggregation

## Use Cases

### Primary Use Cases
- **Monitoring Infrastructure**: Set up comprehensive monitoring for cloud and on-premises infrastructure
- **Application Performance Monitoring**: Create dashboards for application metrics and performance tracking
- **Incident Response**: Use monitoring data to quickly identify and resolve system issues
- **SLI/SLO Management**: Track and report on service reliability metrics
- **Capacity Planning**: Analyze trends and plan for resource scaling

### Advanced Use Cases  
- **Multi-tenant Monitoring**: Manage monitoring for multiple teams and applications
- **Custom Plugin Development**: Extend Grafana functionality with custom datasources and panels
- **Monitoring-as-Code**: Implement infrastructure-as-code principles for monitoring setup
- **Automated Remediation**: Integrate monitoring with automated response systems

## Best Practices
- **Dashboard Organization**: Use consistent naming conventions and folder structures
- **Alert Hygiene**: Regularly review and tune alerts to minimize noise
- **Documentation**: Maintain runbooks and documentation for monitoring procedures  
- **Access Control**: Implement proper RBAC for Grafana users and dashboards
- **Performance Optimization**: Monitor and optimize Grafana instance performance
- **Backup Strategy**: Regular backups of dashboards, datasources, and configuration

## Integration Points
- **CI/CD Pipelines**: Integrate monitoring setup into deployment workflows
- **Infrastructure as Code**: Use Terraform or similar tools for Grafana configuration
- **Chat Platforms**: Connect alerts to Slack, Teams, or other communication tools
- **Ticketing Systems**: Integrate with JIRA, ServiceNow, or other ITSM platforms
- **Security Tools**: Connect security monitoring and compliance reporting

---

*This persona focuses specifically on Grafana-centric SRE workflows while maintaining compatibility with broader monitoring and observability ecosystems.*