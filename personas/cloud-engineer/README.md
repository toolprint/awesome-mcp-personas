# Cloud Engineer Persona

## Overview
A comprehensive MCP persona for cloud infrastructure management across AWS, Azure, and Google Cloud Platform. This persona provides tools for infrastructure-as-code, container orchestration, monitoring, and cloud resource management.

## Target Audience
- **Cloud Infrastructure Engineers**: Managing multi-cloud deployments and resources
- **DevOps Engineers**: Implementing CI/CD pipelines and infrastructure automation
- **Platform Engineers**: Building and maintaining cloud-native platforms
- **Site Reliability Engineers**: Monitoring and maintaining cloud infrastructure
- **Solutions Architects**: Designing scalable cloud architectures

## Core Capabilities

### Infrastructure Management
- **Infrastructure as Code**: Terraform, CloudFormation, ARM templates
- **Multi-Cloud Support**: AWS, Azure, Google Cloud Platform
- **Resource Provisioning**: Compute, storage, networking, databases
- **Cost Management**: Resource optimization and cost monitoring

### Container & Orchestration
- **Container Management**: Docker build, push, pull operations
- **Kubernetes**: Cluster management, deployment, scaling, monitoring
- **Service Mesh**: Istio, Linkerd configuration and management
- **Container Registries**: ECR, ACR, GCR integration

### Monitoring & Observability
- **Metrics Collection**: Prometheus, CloudWatch, Azure Monitor
- **Log Management**: Centralized logging and analysis
- **Application Performance**: Distributed tracing and monitoring
- **Alerting**: Automated incident detection and notification

### Security & Compliance
- **Identity & Access Management**: Role-based access control
- **Network Security**: VPCs, security groups, network policies
- **Secrets Management**: Key vaults, parameter stores
- **Compliance**: Policy validation and governance

## Workflow Categories

### Infrastructure Deployment
Primary tools for provisioning and managing cloud infrastructure:
- Infrastructure as Code deployment
- Multi-cloud resource management
- Environment provisioning and teardown
- Resource scaling and optimization

### Application Deployment
Tools for deploying and managing applications in the cloud:
- Container image management
- Kubernetes deployments
- CI/CD pipeline execution
- Blue-green and canary deployments

### Monitoring & Maintenance
Tools for ongoing infrastructure monitoring and maintenance:
- Performance monitoring and alerting
- Log analysis and troubleshooting
- Security scanning and compliance checks
- Capacity planning and optimization

### Incident Response
Tools for handling production incidents:
- Real-time monitoring and alerting
- Log aggregation and analysis
- Automated remediation scripts
- Communication and escalation

## MCP Servers

This persona combines 8 essential MCP servers optimized for cloud engineering workflows, providing comprehensive infrastructure management, container orchestration, and monitoring capabilities.

### Infrastructure & Version Control

#### Git MCP Server
**Purpose**: Version control operations for Infrastructure as Code repositories
- **Installation**: `uvx mcp-server-git`
- **Key Tools**: `git_log`, `git_diff`, `git_commit`, `git_push`, `git_status`, `git_branch`
- **Use Cases**: IaC repository management, configuration tracking, deployment history
- **Repository**: [GitHub](https://github.com/modelcontextprotocol/servers/tree/main/src/git)

#### Filesystem MCP Server  
**Purpose**: Secure file operations for configuration files, scripts, and manifests
- **Installation**: `npx -y @modelcontextprotocol/server-filesystem`
- **Key Tools**: `read_file`, `write_file`, `create_directory`, `list_directory`, `move_file`, `search_files`
- **Use Cases**: Managing Terraform files, Kubernetes manifests, configuration scripts
- **Repository**: [GitHub](https://github.com/modelcontextprotocol/servers/tree/main/src/filesystem)

### Container Management

#### Docker MCP Server
**Purpose**: Docker container management and Docker Compose operations
- **Installation**: `uvx docker-mcp` or `npx @smithery/cli install docker-mcp --client claude`
- **Key Tools**: `create_container`, `deploy_compose`, `get_logs`, `list_containers`
- **Use Cases**: Container lifecycle management, multi-service deployments, debugging
- **Repository**: [GitHub](https://github.com/QuantGeekDev/docker-mcp)

#### Kubectl MCP Server  
**Purpose**: Kubernetes cluster management and kubectl operations
- **Installation**: `pip install kubectl-mcp-tool`
- **Key Tools**: `get_pods`, `get_services`, `describe_resource`, `get_logs`, `scale_deployment`, `port_forward`
- **Use Cases**: Cluster monitoring, workload management, troubleshooting, scaling
- **Repository**: [GitHub](https://github.com/rohitg00/kubectl-mcp-server)

### Cloud Provider Integration

#### AWS Cloud Control API MCP Server
**Purpose**: Direct AWS resource management with security compliance
- **Installation**: Available via AWS MCP collection (contact AWS for access)
- **Key Tools**: AWS resource CRUD operations, security scanning, best practices validation
- **Use Cases**: EC2 management, VPC configuration, IAM policy management, resource provisioning
- **Repository**: [GitHub](https://github.com/awslabs/mcp)

#### Sequential Thinking MCP Server
**Purpose**: Complex multi-step cloud architecture analysis and troubleshooting  
- **Installation**: `npx -y @modelcontextprotocol/server-sequentialthinking`
- **Key Tools**: `create_thought`, `continue_thought`, `rewind_thought`
- **Use Cases**: Infrastructure design decisions, incident analysis, capacity planning
- **Repository**: [GitHub](https://github.com/modelcontextprotocol/servers/tree/main/src/sequentialthinking)

### Monitoring & Observability

#### Prometheus MCP Server
**Purpose**: Metrics collection, querying, and analysis
- **Installation**: `curl -LsSf https://astral.sh/uv/install.sh | sh && uv pip install git+https://github.com/pab1it0/prometheus-mcp-server`
- **Key Tools**: `execute_query`, `execute_range_query`, `list_metrics`, `get_targets`, `get_metric_metadata`
- **Use Cases**: Performance monitoring, alerting setup, capacity analysis, SLA tracking
- **Repository**: [GitHub](https://github.com/pab1it0/prometheus-mcp-server)

#### Time MCP Server
**Purpose**: Time and timezone operations for scheduling and monitoring
- **Installation**: `npx -y @modelcontextprotocol/server-time`  
- **Key Tools**: `get_current_time`, `convert_timezone`, `format_time`, `calculate_duration`
- **Use Cases**: Deployment scheduling, maintenance windows, log analysis, incident timelines
- **Repository**: [GitHub](https://github.com/modelcontextprotocol/servers/tree/main/src/time)

### Server Workflow Categories

#### Infrastructure Deployment (Git + Filesystem + AWS Cloud Control + Sequential)
Primary workflow for provisioning and managing cloud infrastructure:
- Plan infrastructure changes using Sequential Thinking
- Manage IaC files with Filesystem operations  
- Track changes with Git version control
- Deploy resources via AWS Cloud Control API

#### Container Operations (Docker + Kubectl + Sequential)
Comprehensive container and orchestration management:
- Build and manage containers with Docker MCP
- Deploy and scale applications with Kubectl MCP  
- Analyze complex deployment scenarios with Sequential Thinking
- Monitor container health and performance

#### Monitoring & Incident Response (Prometheus + Time + Sequential)
End-to-end observability and incident management:
- Query metrics and analyze trends with Prometheus MCP
- Coordinate time-based analysis with Time MCP
- Structure incident response with Sequential Thinking  
- Generate actionable insights for resolution

## Prerequisites

### Required Tools
- **CLI Tools**: AWS CLI, Azure CLI, gcloud CLI
- **Infrastructure**: Terraform >= 1.0, kubectl >= 1.20
- **Containers**: Docker >= 20.10
- **Languages**: Python 3.8+, Go 1.18+ (for custom tooling)

### Authentication
- AWS: IAM roles or access keys with appropriate permissions
- Azure: Service principals or Azure AD authentication
- GCP: Service account keys or Application Default Credentials
- Kubernetes: kubeconfig file with cluster access

### Permissions
- **Infrastructure**: Full access to compute, storage, networking services
- **Security**: IAM/RBAC management permissions
- **Monitoring**: Read/write access to monitoring and logging services
- **Cost Management**: Billing and cost analysis permissions

## Example Workflows

### 1. Multi-Cloud Infrastructure Deployment
```bash
# Deploy infrastructure across multiple clouds
terraform plan -out=plan.tfplan
terraform apply plan.tfplan
kubectl apply -f k8s-manifests/
```

### 2. Container Application Deployment
```bash
# Build and deploy containerized application
docker build -t myapp:v1.0 .
docker push registry/myapp:v1.0
kubectl set image deployment/myapp container=registry/myapp:v1.0
```

### 3. Infrastructure Monitoring
```bash
# Check infrastructure health
kubectl get pods --all-namespaces
terraform state list
aws ec2 describe-instances --filters "Name=instance-state-name,Values=running"
```

### 4. Incident Response
```bash
# Investigate and resolve production issues
kubectl logs -f deployment/myapp
kubectl describe pod failing-pod-name
kubectl scale deployment/myapp --replicas=5
```

## Configuration Examples

### Basic Setup
Essential MCP servers for cloud infrastructure management.

### Advanced Setup  
Extended configuration with monitoring, security, and multi-cloud tools.

### Enterprise Setup
Full-featured configuration for large-scale enterprise cloud operations.

## Troubleshooting

### Common Issues
- **Authentication**: Verify cloud CLI authentication and permissions
- **Network**: Check security groups, VPC configurations, and connectivity
- **Resource Limits**: Monitor quotas and service limits
- **Version Compatibility**: Ensure tool versions are compatible

### Support Resources
- Cloud provider documentation
- Infrastructure as Code best practices
- Kubernetes troubleshooting guides
- Container orchestration patterns

## Contributing

Contributions to improve cloud engineering workflows are welcome. Please ensure:
- MCP servers are actively maintained and well-documented
- Configurations support multiple cloud providers where applicable
- Security best practices are followed
- Tools integrate well together for common workflows

---

*This persona is designed for infrastructure engineers managing modern cloud environments. For application-specific cloud tools, consider the relevant developer personas.*