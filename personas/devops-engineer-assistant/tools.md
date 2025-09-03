# DevOps Engineer Assistant - Tool Reference

This document provides a comprehensive reference for all tools available in the DevOps Engineer Assistant persona, organized by MCP server and workflow integration.

## Tool Summary

| Server | Tools Count | Primary Use Cases |
|--------|-------------|-------------------|
| **docker** | 8 tools | Container lifecycle, deployment automation |
| **cloudflare** | 8 tools | CDN management, traffic routing, security |
| **tavily** | 4 tools | Research, documentation, best practices |
| **Manual Git** | CLI-based | Version control, configuration tracking |

**Total: 20+ tools across 4 integration points**

---

## Docker MCP Server

**Package**: `docker-mcp`  
**Installation**: `npx -y docker-mcp`  
**Transport**: stdio  
**Requirements**: Docker Desktop/Engine running

### Container Lifecycle Management

- **docker.create_container**: Create new containers with configuration, port mapping, and environment variables
- **docker.start_container**: Start stopped containers with health monitoring
- **docker.stop_container**: Gracefully stop running containers with timeout handling
- **docker.list_containers**: List all containers with status, ports, and metadata filtering
- **docker.remove_container**: Remove stopped containers and associated volumes

### Image Operations

- **docker.build_image**: Build Docker images from Dockerfiles with build context and caching
- **docker.list_images**: List available images with size, tags, and creation metadata
- **docker.run_container**: Create and start containers in single operation with full configuration

### Container Interaction

- **docker.get_container_logs**: Retrieve container logs with filtering, timestamps, and follow options
- **docker.exec_command**: Execute commands inside running containers for diagnostics and maintenance

---

## Cloudflare MCP Server

**Package**: `@cloudflare/mcp-server`  
**Installation**: `npx -y @cloudflare/mcp-server`  
**Transport**: stdio  
**Environment**: Requires `CLOUDFLARE_API_TOKEN`

### Workers & Edge Computing

- **cloudflare.deploy_worker**: Deploy and update Cloudflare Workers with code and configuration
- **cloudflare.list_workers**: List deployed Workers with status, routes, and performance metrics
- **cloudflare.get_worker_logs**: Retrieve Worker execution logs and error information

### DNS & Traffic Management

- **cloudflare.get_dns_records**: Retrieve DNS records by zone with filtering and search capabilities
- **cloudflare.update_dns_record**: Modify DNS records for traffic routing and load balancing
- **cloudflare.get_analytics_dashboard**: Access traffic analytics, performance metrics, and usage data

### Security & Compliance

- **cloudflare.get_audit_logs**: Retrieve security audit logs for compliance and incident investigation
- **cloudflare.list_casb_findings**: List CASB security findings and policy violations

---

## Tavily Search MCP Server

**Package**: `tavily-mcp@latest`  
**Installation**: `npx -y tavily-mcp@latest`  
**Transport**: stdio  
**Environment**: Requires `TAVILY_API_KEY` from tavily.com

### Research & Documentation

- **tavily.search**: Perform intelligent web search with AI-focused content extraction
- **tavily.get_search_context**: Get comprehensive context and summaries from search results
- **tavily.extract**: Extract and summarize content from specific URLs and web resources
- **tavily.qna_search**: Question-and-answer format search for specific technical queries

---

## Manual Git Integration

**Status**: CLI-based integration due to archived mcp-server-git (July 2025)  
**Requirements**: Git CLI installed and configured  
**Authentication**: SSH keys or HTTPS tokens configured

### Core Git Operations
- **Manual git status**: Check repository status and uncommitted changes
- **Manual git add**: Stage files for commit
- **Manual git commit**: Commit changes with descriptive messages
- **Manual git push**: Push changes to remote repositories
- **Manual git pull**: Pull latest changes from remote
- **Manual git branch**: Branch management and switching
- **Manual git log**: View commit history and change tracking

### GitOps Integration Patterns
- **Infrastructure as Code**: Version control for Terraform, Kubernetes manifests
- **Configuration Management**: Track environment configurations and secrets
- **Deployment Tracking**: Maintain deployment history and rollback points
- **Audit Trails**: Document infrastructure changes and compliance

---

# Toolset Workflows

## Environment Provisioning & Drift Checks

**Primary Tools**: docker.*, tavily.search, manual git operations

### Typical Workflow:
1. **Baseline Establishment**: Use manual Git to retrieve infrastructure configurations
2. **Container Deployment**: Use `docker.create_container` and `docker.start_container` for service deployment
3. **Health Monitoring**: Use `docker.list_containers` and `docker.get_container_logs` for status verification
4. **Documentation Research**: Use `tavily.search` and `tavily.get_search_context` for best practices validation
5. **Drift Detection**: Compare running state against Git-tracked configurations

### Integration Pattern:
```
Git Configs → Docker Deployment → Health Checks → Best Practices Research → Drift Remediation
```

## Blue-Green / Canary Deployments

**Primary Tools**: docker.*, cloudflare.*, tavily.search

### Typical Workflow:
1. **Image Preparation**: Use `docker.build_image` for new application versions
2. **Parallel Deployment**: Use `docker.run_container` for blue-green container creation
3. **Traffic Routing**: Use `cloudflare.deploy_worker` and `cloudflare.update_dns_record` for traffic management
4. **Health Validation**: Use `docker.exec_command` and `cloudflare.get_analytics_dashboard` for monitoring
5. **Rollback Capability**: Use `cloudflare.list_workers` and `docker.stop_container` for quick rollback

### Integration Pattern:
```
Docker Build → Parallel Deploy → Cloudflare Routing → Health Checks → Traffic Switch/Rollback
```

## Incident Mitigation Playbooks

**Primary Tools**: docker.*, cloudflare.get_audit_logs, tavily.search

### Typical Workflow:
1. **Issue Detection**: Use `docker.list_containers` and `cloudflare.get_audit_logs` for problem identification
2. **Log Analysis**: Use `docker.get_container_logs` and Cloudflare analytics for root cause analysis
3. **Runbook Research**: Use `tavily.search` and `tavily.qna_search` for incident response procedures
4. **Remediation**: Use `docker.exec_command`, `docker.start_container`, and Cloudflare Worker updates
5. **Verification**: Use monitoring tools to confirm service restoration

### Integration Pattern:
```
Issue Detection → Log Correlation → Runbook Lookup → Automated Remediation → Service Verification
```

## Secrets & Configuration Hygiene

**Primary Tools**: docker.exec_command, cloudflare.get_audit_logs, tavily.extract

### Typical Workflow:
1. **Security Scanning**: Use `docker.exec_command` for container security audits
2. **Access Review**: Use `cloudflare.get_audit_logs` and `cloudflare.list_casb_findings` for access pattern analysis
3. **Compliance Research**: Use `tavily.search` and `tavily.extract` for security best practices
4. **Configuration Hardening**: Use `docker.build_image` with security-focused Dockerfiles
5. **Audit Documentation**: Manual Git operations for compliance trail

### Integration Pattern:
```
Security Scan → Access Audit → Compliance Research → Configuration Update → Audit Trail
```

---

# Server Integration Best Practices

## Docker + Cloudflare Integration
- **Deployment Coordination**: Docker containers → Cloudflare Workers for traffic routing
- **Health Monitoring**: Container logs + Cloudflare analytics for comprehensive monitoring
- **Rollback Strategy**: Coordinate container stops with DNS/Worker rollbacks

## Search + Operations Integration
- **Research-Driven Operations**: Use Tavily search before implementing changes
- **Runbook Automation**: Combine search results with automated remediation
- **Best Practice Validation**: Continuous research integration in operational workflows

## Manual Git + Automation Integration
- **Configuration Management**: Git tracking for all infrastructure configurations
- **Deployment Tracking**: Manual Git operations for deployment history
- **Rollback Coordination**: Git-based configuration rollback with service rollback

---

# Environment Variables & Security

## Required Environment Variables

```bash
# Cloudflare Integration
CLOUDFLARE_API_TOKEN="<your_cloudflare_api_token>"

# Tavily Search Integration  
TAVILY_API_KEY="<your_tavily_api_key>"

# Docker Integration (automatic via Docker Desktop)
# No additional environment variables required

# Git Integration (manual CLI setup)
# Configure via: git config --global user.name / user.email
# SSH keys or personal access tokens for repository access
```

## Security Best Practices

1. **API Key Management**: Store all API keys in secure environment variables
2. **Container Security**: Use `docker.exec_command` for security audits and hardening
3. **Access Auditing**: Regular `cloudflare.get_audit_logs` review
4. **Configuration Tracking**: All changes tracked through manual Git operations
5. **Compliance Monitoring**: Use `cloudflare.list_casb_findings` for policy compliance

---

# Troubleshooting & Support

## Common Issues

### Docker Server Issues
- **Connection Problems**: Ensure Docker Desktop/Engine is running
- **Permission Issues**: Verify Docker daemon permissions and group membership
- **Container Conflicts**: Use `docker.list_containers` to identify port or name conflicts

### Cloudflare Server Issues
- **API Token**: Verify token has appropriate permissions for all required operations
- **Rate Limiting**: Implement appropriate delays between API calls
- **Zone Access**: Ensure token has access to required DNS zones and Workers

### Tavily Search Issues
- **API Quota**: Monitor API usage and upgrade plan if needed
- **Search Quality**: Use specific, technical queries for better results
- **Rate Limiting**: Respect API rate limits for consistent access

### Git Integration Issues
- **Authentication**: Ensure SSH keys or tokens are properly configured
- **Repository Access**: Verify read/write permissions for infrastructure repositories
- **Merge Conflicts**: Manual resolution required for configuration conflicts

## Support Resources

- **Docker MCP**: GitHub repository and Docker community forums
- **Cloudflare**: Official Cloudflare API documentation and support
- **Tavily**: API documentation at tavily.com and support channels
- **Git**: Official Git documentation and version control best practices

---

*This tool reference is maintained as part of the DevOps Engineer Assistant persona. For updates and additional tools, refer to the official MCP server documentation and persona validation notes.*