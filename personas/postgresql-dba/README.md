# PostgreSQL DBA Persona

## Overview
Production PostgreSQL database administrator persona focused on enterprise PostgreSQL operations, performance monitoring, schema management, and production DBA workflows with advanced PostgreSQL-specific tooling for optimization, maintenance, and compliance.

## Target Audience
- Production PostgreSQL Database Administrators
- Senior Database Engineers specializing in PostgreSQL
- DevOps Engineers managing PostgreSQL infrastructure  
- Database Architects designing PostgreSQL systems
- Site Reliability Engineers maintaining PostgreSQL services

## Prerequisites
- PostgreSQL server access with appropriate permissions
- Database credentials with DBA privileges
- Git repository for schema management
- Basic understanding of PostgreSQL administration concepts
- Knowledge of SQL query optimization and performance tuning

## Installation

1. Set up your environment variables:
   ```bash
   export POSTGRES_HOST="your-postgres-host"
   export POSTGRES_PORT="5432"
   export POSTGRES_DATABASE="your-database-name"
   export POSTGRES_USER="your-dba-username"
   export POSTGRES_PASSWORD="your-dba-password"
   export POSTGRES_SSL="prefer"
   export ALLOWED_DIRS="/usr/local/pgsql,/var/lib/postgresql,/etc/postgresql,/opt/postgresql"
   ```

2. The MCP servers will be automatically installed when first used.

## MCP Servers

### 1. PostgreSQL Operations Server
Core PostgreSQL database operations with multi-tenant support for production environments.
- **Source**: [ahmetkca/mcp-server-postgres](https://github.com/ahmetkca/mcp-server-postgres)
- **Package**: `@ahmetkca/mcp-server-postgres`
- **Transport**: stdio
- **Authentication**: PostgreSQL credentials
- **Environment**: Requires PostgreSQL connection parameters

### 2. PostgreSQL Ops Server  
Comprehensive PostgreSQL monitoring and operations toolkit with 30+ specialized DBA tools.
- **Source**: [call518/MCP-PostgreSQL-Ops](https://github.com/call518/MCP-PostgreSQL-Ops)
- **Package**: `git+https://github.com/call518/MCP-PostgreSQL-Ops`
- **Transport**: stdio
- **Authentication**: PostgreSQL credentials  
- **Environment**: Requires PostgreSQL connection parameters

### 3. Chart Visualization Server
Database performance visualization and query result charting for monitoring dashboards.
- **Source**: [antvis/mcp-server-chart](https://github.com/antvis/mcp-server-chart)
- **Package**: `@antvis/mcp-server-chart`
- **Transport**: stdio
- **Authentication**: None required

### 4. Advanced Chart Server
Interactive visualization server for complex PostgreSQL performance analysis and reporting.
- **Source**: [visactor/vchart-mcp-server](https://github.com/visactor/vchart-mcp-server)
- **Package**: `@visactor/vchart-mcp-server`  
- **Transport**: stdio
- **Authentication**: None required

### 5. Filesystem Management
SQL script and configuration file management for PostgreSQL installations.
- **Source**: [modelcontextprotocol/servers](https://github.com/modelcontextprotocol/servers)
- **Package**: `@modelcontextprotocol/server-filesystem`
- **Transport**: stdio
- **Authentication**: File system permissions
- **Environment**: Restricted to PostgreSQL directories

### 6. Git Integration
Version control for database schemas, migrations, and configuration changes.
- **Source**: [cyanheads/git-mcp-server](https://github.com/cyanheads/git-mcp-server)
- **Package**: `@cyanheads/git-mcp-server`
- **Transport**: stdio
- **Authentication**: Git credentials

### 7. Memory Knowledge Graph
Documentation management and relationship mapping for database schemas and processes.
- **Source**: [modelcontextprotocol/servers](https://github.com/modelcontextprotocol/servers)
- **Package**: `@modelcontextprotocol/server-memory`
- **Transport**: stdio
- **Authentication**: None required

### 8. Time Operations
Timezone handling and time calculations for distributed PostgreSQL systems.
- **Source**: [modelcontextprotocol/servers](https://github.com/modelcontextprotocol/servers)
- **Package**: `@modelcontextprotocol/server-time`
- **Transport**: stdio
- **Authentication**: None required

## Toolsets

### 1. production-admin (default)
Core PostgreSQL administration and monitoring for production environments.

**Tools:**
- `postgres.execute_query` - Execute SQL queries and administrative commands
- `postgres.list_tables` - List all tables in the database
- `postgres.describe_table` - Get detailed table schema information
- `postgres.get_schema` - Retrieve complete database schema
- `postgres.list_users` - List database users and roles
- `postgres.check_permissions` - Verify user permissions and access rights
- `postgres-ops.monitor_connections` - Monitor active database connections
- `postgres-ops.check_vacuum_stats` - Check autovacuum statistics and status
- `postgres-ops.get_table_stats` - Get table statistics and usage metrics
- `postgres-ops.monitor_replication` - Monitor PostgreSQL replication status
- `postgres-ops.check_bloat` - Analyze table and index bloat

**Common Workflows:**
- Daily database health checks and monitoring
- User management and permission auditing
- Connection monitoring and troubleshooting
- Routine maintenance task validation
- Replication status verification

### 2. performance-tuning
PostgreSQL query optimization and database performance analysis.

**Tools:**
- `postgres.analyze_query` - Analyze query performance and execution
- `postgres.explain_query` - Generate query execution plans
- `postgres.get_stats` - Retrieve database performance statistics
- `postgres-ops.analyze_slow_queries` - Identify and analyze slow-running queries
- `postgres-ops.get_index_usage` - Analyze index usage and effectiveness
- `postgres-ops.check_lock_waits` - Monitor database locks and waits
- `postgres-ops.monitor_autovacuum` - Track autovacuum operations and tuning
- `chart.create_line_chart` - Create performance trend visualizations
- `chart.create_bar_chart` - Generate performance comparison charts
- `vchart.create_performance_dashboard` - Build interactive performance dashboards
- `time.get_current_time` - Get current timestamp for performance tracking
- `time.convert_timezone` - Handle timezone conversions for distributed systems

**Common Workflows:**
- Query performance analysis and optimization
- Index usage review and optimization
- Autovacuum tuning and monitoring
- Performance dashboard creation
- Lock contention identification and resolution

### 3. development-ops  
Schema management, migrations, and development workflow support.

**Tools:**
- `filesystem.read_text_file` - Read SQL scripts and configuration files
- `filesystem.write_file` - Write migration scripts and documentation
- `filesystem.list_directory` - List database script directories
- `filesystem.create_directory` - Create directories for organized scripts
- `git.git_status` - Check version control status of schema changes
- `git.git_add` - Stage database schema changes
- `git.git_commit` - Commit database migrations and changes
- `git.git_diff` - Review database schema differences
- `memory.create_entities` - Document database schema relationships
- `memory.search_nodes` - Search documented database relationships
- `memory.add_observations` - Add notes about database changes
- `postgres-ops.validate_schema` - Validate database schema integrity
- `postgres-ops.generate_migration` - Generate database migration scripts

**Common Workflows:**
- Database schema version control and migrations
- Development environment setup and management
- Schema documentation and relationship mapping
- Migration script validation and testing
- Development-to-production deployment workflows

### 4. monitoring-alerts
Real-time monitoring, alerting, and capacity planning.

**Tools:**
- `postgres-ops.check_disk_usage` - Monitor database disk space usage
- `postgres-ops.monitor_cpu_usage` - Track database CPU utilization
- `postgres-ops.check_connection_limits` - Monitor connection pool limits
- `postgres-ops.monitor_backup_status` - Verify backup completion and status
- `postgres-ops.get_error_log` - Retrieve and analyze error logs
- `postgres-ops.check_security_audit` - Perform security audit checks
- `postgres-ops.validate_configuration` - Validate PostgreSQL configuration
- `chart.create_time_series` - Create time-based monitoring charts
- `vchart.create_alert_dashboard` - Build alert and monitoring dashboards
- `memory.read_graph` - Access documented monitoring procedures
- `time.format_time` - Format timestamps for reports
- `time.calculate_duration` - Calculate time durations for SLA tracking

**Common Workflows:**
- Real-time database monitoring and alerting
- Capacity planning and resource utilization analysis
- Backup verification and disaster recovery testing
- Security compliance monitoring and reporting
- SLA tracking and performance reporting

## Common Use Cases

### 1. Daily Database Health Check
- Check database connections and active sessions
- Verify backup completion status
- Monitor disk space and resource usage
- Review error logs for critical issues
- Generate daily health report

### 2. Performance Optimization Workflow  
- Identify slow queries using performance analysis tools
- Generate execution plans for problematic queries
- Analyze index usage and recommend optimizations
- Create performance visualization dashboards
- Document optimization changes and results

### 3. Schema Migration Management
- Review pending schema changes in version control
- Validate migration scripts before deployment
- Execute migrations in controlled environment
- Document schema changes and relationships
- Monitor post-migration performance impact

### 4. Production Incident Response
- Identify connection and lock issues
- Analyze recent performance degradation
- Check system resource utilization
- Review error logs and security alerts
- Generate incident analysis reports

### 5. Capacity Planning Analysis
- Analyze historical growth trends
- Monitor current resource utilization
- Project future capacity requirements
- Create capacity planning visualizations
- Document recommendations for infrastructure scaling

## Configuration

### Environment Variables
- `POSTGRES_HOST`: PostgreSQL server hostname or IP address (required)
- `POSTGRES_PORT`: PostgreSQL server port number (required, default: 5432)
- `POSTGRES_DATABASE`: Target database name (required)
- `POSTGRES_USER`: PostgreSQL username with DBA privileges (required)
- `POSTGRES_PASSWORD`: PostgreSQL user password (required)
- `POSTGRES_SSL`: SSL connection mode (optional, default: prefer)
- `ALLOWED_DIRS`: Comma-separated list of allowed filesystem directories (optional)

### Customization
To customize the persona:
1. Edit `mcp.json` to modify server configurations
2. Edit `persona.yaml` to adjust toolsets or add new tools
3. Ensure all changes comply with the MCP schema

## Best Practices

- Always use read-only queries for monitoring and analysis
- Implement proper connection pooling and limit concurrent connections
- Regularly monitor autovacuum performance and adjust settings as needed
- Maintain comprehensive documentation of schema changes and optimizations
- Use version control for all database scripts and configuration changes
- Monitor disk space and set up appropriate alerts for capacity management
- Regularly review and optimize slow-running queries
- Implement security best practices for database access and authentication
- Create regular backup schedules and test disaster recovery procedures
- Document all administrative procedures and emergency response protocols

## Troubleshooting

### Common Issues

1. **Connection failures to PostgreSQL server**
   - Verify POSTGRES_HOST and POSTGRES_PORT are correct
   - Check that PostgreSQL server is running and accessible
   - Ensure firewall rules allow database connections
   - Verify SSL configuration if using encrypted connections

2. **Permission denied errors for database operations**
   - Confirm POSTGRES_USER has appropriate DBA privileges
   - Check that user can connect to the specified database
   - Verify row-level security policies if applicable
   - Review role membership and inherited permissions

3. **MCP server installation issues**
   - Ensure Node.js is installed for npm packages
   - Check Python/pip installation for uvx packages  
   - Verify network access for package downloads
   - Clear npm/pip cache if installation fails

4. **Performance monitoring tools not responding**
   - Check database connection pool limits
   - Verify system resources (CPU, memory, disk)
   - Review PostgreSQL log files for errors
   - Ensure monitoring queries are not blocking

5. **Filesystem access errors for SQL scripts**
   - Verify ALLOWED_DIRS includes necessary paths
   - Check file permissions for script directories
   - Ensure paths exist and are accessible
   - Review filesystem server configuration

## Support

For issues with:
- This persona configuration: Open an issue in the awesome-mcp-personas repository
- Individual MCP servers: Check respective server documentation
- PostgreSQL operations: Refer to PostgreSQL official documentation
- Database connectivity: Check network and firewall configuration

## Contributing

To improve this persona:
1. Verify all tool names against actual MCP server implementations
2. Test each toolset with real-world PostgreSQL scenarios
3. Document any additional tools discovered
4. Submit improvements via pull request

## License

This persona configuration is part of the Awesome MCP Personas project and follows the same licensing terms.