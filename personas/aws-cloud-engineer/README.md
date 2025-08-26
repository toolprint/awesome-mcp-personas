# AWS Cloud Engineer Persona

## Overview
A specialized MCP persona dedicated to Amazon Web Services (AWS) cloud infrastructure management, optimization, and operations. This persona provides comprehensive tools for AWS resource management, documentation access, monitoring, and cloud-native architecture implementation using AWS best practices.

## Target Audience
- **AWS Solutions Architects**: Designing and implementing scalable AWS architectures
- **AWS Cloud Engineers**: Managing day-to-day AWS infrastructure operations
- **AWS DevOps Engineers**: Implementing CI/CD pipelines and automation on AWS
- **AWS Site Reliability Engineers**: Monitoring and maintaining AWS-based applications
- **AWS Migration Specialists**: Moving workloads to AWS and optimizing cloud costs
- **AWS Security Engineers**: Implementing AWS security best practices and compliance

## Core Capabilities

### AWS Infrastructure Management
- **Compute Services**: EC2, ECS, EKS, Lambda, Batch, Fargate
- **Storage Services**: S3, EBS, EFS, FSx, Storage Gateway
- **Database Services**: RDS, DynamoDB, Aurora, ElastiCache, Neptune, DocumentDB
- **Networking**: VPC, Route 53, CloudFront, ALB/NLB, Direct Connect, Transit Gateway
- **Security**: IAM, KMS, Secrets Manager, Security Hub, GuardDuty, Shield

### AWS Infrastructure as Code
- **CloudFormation**: Stack deployment, template validation, parameter management
- **CDK (Cloud Development Kit)**: Infrastructure definition in code
- **Terraform**: Multi-region AWS deployments with state management
- **AWS CLI**: Command-line resource management and automation
- **AWS SDK**: Programmatic access to AWS APIs

### AWS Monitoring & Observability
- **CloudWatch**: Metrics, logs, alarms, dashboards, custom metrics
- **X-Ray**: Distributed tracing and application performance monitoring
- **Config**: Resource compliance and configuration management
- **CloudTrail**: API call logging and security auditing
- **Systems Manager**: Operational insights and patch management

### AWS Security & Compliance
- **IAM**: Role-based access control, policy management, identity federation
- **Security Groups**: Network-level access control and firewall rules
- **KMS**: Encryption key management and data protection
- **Secrets Manager**: Credential rotation and secure storage
- **Inspector**: Security vulnerability assessments

### AWS Cost Management
- **Cost Explorer**: Cost analysis and optimization recommendations
- **Budgets**: Cost monitoring and alerting
- **Resource Optimization**: Right-sizing recommendations and unused resources
- **Reserved Instances**: Capacity planning and cost savings analysis

## Workflow Categories

### Resource Provisioning & Management
Core AWS resource lifecycle management:
- Infrastructure deployment using CloudFormation/CDK/Terraform
- EC2 instance management and auto-scaling configuration
- Database provisioning and backup management
- Load balancer and networking setup
- Storage configuration and lifecycle policies

### Application Deployment & Container Management
AWS-native application deployment workflows:
- ECS/EKS cluster management and service deployments
- Lambda function deployment and event configuration
- ECR container registry management
- API Gateway setup and integration
- CodePipeline CI/CD automation

### Monitoring & Incident Response
AWS monitoring and operational workflows:
- CloudWatch dashboard creation and alarm configuration
- Log analysis and troubleshooting with CloudWatch Logs
- Performance monitoring and optimization
- Security incident response and forensics
- Cost monitoring and optimization

### Security & Compliance Management
AWS security implementation and governance:
- IAM policy creation and permission auditing
- Security group configuration and network ACLs
- Encryption implementation and key rotation
- Compliance monitoring and reporting
- Vulnerability scanning and remediation

## MCP Servers

Comprehensive AWS-focused MCP servers optimized for cloud engineering workflows.

### AWS Infrastructure & API Management

| Server | Description | Installation | Key Capabilities |
|--------|-------------|--------------|------------------|
| **AWS Core** | AWS planning and orchestration hub with guidance support | `uvx awslabs.core-mcp-server@latest` | Infrastructure planning, AWS service integration, solution guidance |
| **AWS API** | Direct AWS API integration with validation and security controls | `uvx awslabs.aws-api-mcp-server@latest` | AWS CLI operations, resource management, API validation |
| **AWS Documentation** | Access and search comprehensive AWS documentation | `uvx awslabs.aws-documentation-mcp-server@latest` | Best practices lookup, service documentation, troubleshooting guides |
| **Filesystem** | Secure file operations for AWS configuration management | `npx -y @modelcontextprotocol/server-filesystem` | Configuration files, CloudFormation templates, infrastructure scripts |

### Infrastructure as Code & Deployment

| Server | Description | Installation | Key Capabilities |
|--------|-------------|--------------|------------------|
| **AWS CloudFormation** | CloudFormation stack management via Cloud Control API | `uvx awslabs.aws-cloudformation-mcp-server@latest` | Stack deployment, template validation, resource management |
| **AWS CDK** | AWS CDK development with security compliance | `uvx awslabs.aws-cdk-mcp-server@latest` | CDK advice, code generation, security best practices |
| **Pulumi** | Multi-cloud Infrastructure as Code with Pulumi Automation API | `uvx pulumi-mcp-server` | Stack operations, deployment automation, state management |
| **Git** | Version control operations for Infrastructure as Code | `uvx mcp-server-git` | Repository management, branch operations, commit tracking |

### Container & Application Management

| Server | Description | Installation | Key Capabilities |
|--------|-------------|--------------|------------------|
| **Docker** | Container management for ECS/EKS development | `npx -y @modelcontextprotocol/server-docker` | Container creation, Compose deployment, log retrieval |
| **AWS EKS** | Kubernetes cluster management and application deployment | `uvx awslabs.aws-eks-mcp-server@latest` | EKS cluster operations, kubectl integration, service deployment |
| **AWS Serverless** | Complete serverless application lifecycle management | `uvx awslabs.aws-serverless-mcp-server@latest` | Lambda deployment, SAM CLI integration, API Gateway setup |

### Database & Data Management

| Server | Description | Installation | Key Capabilities |
|--------|-------------|--------------|------------------|
| **PostgreSQL** | PostgreSQL operations for RDS management | `npx -y @modelcontextprotocol/server-postgres` | Database queries, schema management, performance tuning |
| **DynamoDB Toolbox** | Natural language DynamoDB interactions | `npx dynamodb-toolbox-mcp-server` | NoSQL operations, table management, query optimization |

### Monitoring & Operations

| Server | Description | Installation | Key Capabilities |
|--------|-------------|--------------|------------------|
| **AWS Pricing** | Real-time AWS pricing information and cost analysis | `uvx awslabs.aws-pricing-mcp-server@latest` | EC2 pricing, cost estimation, service comparisons |
| **Sequential Thinking** | Complex AWS troubleshooting and multi-step operations | `npx -y @modelcontextprotocol/server-sequentialthinking` | Root cause analysis, systematic debugging, operational planning |
| **Time** | Time and scheduling operations for AWS workflows | `npx -y @modelcontextprotocol/server-time` | Backup windows, maintenance scheduling, timezone handling |

### AWS Environment Requirements

**Authentication Configuration**:
- AWS credentials via `aws configure` or environment variables
- IAM roles with appropriate permissions for target services
- AWS SSO integration for multi-account environments
- Regional configuration for service-specific operations

**Required AWS Permissions**:
- **Core Operations**: IAM:ListPolicies, STS:GetCallerIdentity, EC2:DescribeRegions
- **Infrastructure**: CloudFormation:*, CDK:*, EC2:*, VPC:*
- **Container Services**: ECS:*, EKS:*, ECR:*
- **Database Services**: RDS:*, DynamoDB:*
- **Monitoring**: CloudWatch:*, Config:*, CloudTrail:*

**Security Considerations**:
- Use IAM roles instead of access keys when possible
- Enable MFA for all administrative operations
- Implement least privilege access principles
- Regular credential rotation and access auditing

## Prerequisites

### Required AWS Access
- **AWS Account**: Active AWS account with appropriate service limits
- **IAM Permissions**: PowerUser or Administrator access for infrastructure management
- **AWS CLI**: Version 2.x configured with credentials
- **AWS SDK**: Python boto3 or other language SDKs as needed

### Authentication Methods
- **AWS CLI Profiles**: Named profiles for different environments/accounts
- **IAM Roles**: AssumeRole for cross-account access
- **Environment Variables**: AWS_ACCESS_KEY_ID, AWS_SECRET_ACCESS_KEY, AWS_REGION
- **EC2 Instance Profiles**: For services running on EC2
- **EKS Service Accounts**: For containerized applications

### Required Tools
- **Infrastructure**: AWS CLI 2.x, Terraform >= 1.0, CloudFormation
- **Containers**: Docker >= 20.10, kubectl >= 1.20 (for EKS)
- **Languages**: Python 3.8+ (boto3), Node.js 16+ (AWS SDK), Go 1.18+
- **Monitoring**: CloudWatch agent, X-Ray daemon (for tracing)

## Example Workflows

### 1. EC2 Infrastructure Deployment
```bash
# Deploy EC2 infrastructure with CloudFormation
aws cloudformation deploy --template-file ec2-stack.yaml \
  --stack-name my-web-app --parameter-overrides \
  InstanceType=t3.medium KeyName=my-key

# Configure auto-scaling and load balancer
aws autoscaling create-auto-scaling-group \
  --auto-scaling-group-name my-asg \
  --launch-template LaunchTemplateName=my-template
```

### 2. Container Application on EKS
```bash
# Create EKS cluster and deploy application
aws eks create-cluster --name my-cluster \
  --version 1.28 --role-arn arn:aws:iam::123456789012:role/eks-service-role

kubectl apply -f k8s-manifests/
aws ecr get-login-password | docker login --username AWS --password-stdin 123456789012.dkr.ecr.us-west-2.amazonaws.com
```

### 3. Database Management
```bash
# Create RDS instance with automated backups
aws rds create-db-instance \
  --db-instance-identifier myapp-prod-db \
  --db-instance-class db.t3.micro \
  --engine mysql --allocated-storage 20 \
  --backup-retention-period 7
```

### 4. Monitoring & Alerting Setup
```bash
# Create CloudWatch alarm for high CPU usage
aws cloudwatch put-metric-alarm \
  --alarm-name cpu-utilization-high \
  --alarm-description "High CPU usage alert" \
  --metric-name CPUUtilization \
  --namespace AWS/EC2 \
  --statistic Average \
  --period 300 --threshold 80
```

### 5. Security & Compliance
```bash
# Audit IAM policies and permissions
aws iam list-policies --scope Local
aws config get-compliance-details-by-config-rule \
  --config-rule-name ec2-security-group-attached-to-eni

# Enable GuardDuty for threat detection
aws guardduty create-detector --enable
```

## Configuration Examples

### Basic AWS Setup
Essential MCP servers for AWS resource management and monitoring.

### Advanced AWS Operations
Extended configuration with advanced monitoring, security, and multi-account management.

### Enterprise AWS Management
Full-featured configuration for large-scale AWS environments with governance and compliance.

## AWS-Specific Best Practices

### Security
- Use IAM roles instead of access keys when possible
- Enable MFA for all privileged accounts
- Implement least privilege access principles
- Enable CloudTrail in all regions
- Use KMS for encryption at rest

### Cost Optimization
- Use Reserved Instances for predictable workloads
- Implement lifecycle policies for S3 storage
- Monitor and optimize data transfer costs
- Use Spot Instances for fault-tolerant workloads
- Regularly review and clean up unused resources

### Reliability
- Design for multiple Availability Zones
- Implement automated backups and disaster recovery
- Use Auto Scaling for application resilience
- Monitor application and infrastructure health
- Test failure scenarios regularly

### Performance
- Use CloudFront for content delivery
- Optimize database performance with appropriate instance types
- Implement caching strategies (ElastiCache, DynamoDB DAX)
- Monitor application performance with X-Ray
- Right-size resources based on actual usage

## Troubleshooting

### Common AWS Issues
- **Authentication**: Verify AWS CLI configuration and IAM permissions
- **Networking**: Check VPC, subnet, and security group configurations
- **Resource Limits**: Monitor service quotas and request increases as needed
- **Cost Overruns**: Set up billing alerts and monitor cost anomalies
- **Security**: Regular security assessments and compliance monitoring

### Support Resources
- AWS Documentation and best practices guides
- AWS Well-Architected Framework
- AWS Support Center and Trusted Advisor
- AWS re:Invent sessions and whitepapers
- AWS community forums and Stack Overflow

## Contributing

Contributions to improve AWS engineering workflows are welcome. Please ensure:
- MCP servers are actively maintained and AWS-focused
- Configurations follow AWS security best practices
- Tools integrate well with AWS services and APIs
- Documentation includes AWS-specific examples and use cases

---

*This persona is designed specifically for AWS cloud engineers and architects. For multi-cloud environments, consider the general cloud-engineer persona. For AWS development, see language-specific developer personas with AWS SDK integration.*