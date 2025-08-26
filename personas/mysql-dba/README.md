# MySQL DBA Persona

## Overview
Production MySQL Database Administrator focused on MySQL/MariaDB administration, web application database optimization, LAMP/LEMP stack integration, and high-traffic e-commerce database management with MySQL-specific performance tuning and replication tools.

## Target Audience
- Production MySQL Database Administrators
- Senior Database Engineers specializing in MySQL/MariaDB
- Web Application Database Engineers (LAMP/LEMP stack)
- E-commerce Database Specialists (MySQL-heavy environments)
- DevOps Engineers managing MySQL infrastructure
- Backend Developers working with MySQL in production environments

## Prerequisites
- MySQL/MariaDB server access with appropriate privileges
- Basic understanding of MySQL administration concepts
- Familiarity with SQL query optimization
- Knowledge of web application database patterns
- Understanding of LAMP/LEMP stack architecture

## Installation

1. Set up your environment variables:
   ```bash
   export MYSQL_HOST="your-mysql-host"
   export MYSQL_PORT="3306"
   export MYSQL_DATABASE="your-database"
   export MYSQL_USER="your-username"
   export MYSQL_PASSWORD="your-password"
   export ALLOWED_DIRECTORIES="/path/to/sql/scripts,/path/to/configs"
   export DEFAULT_TIMEZONE="UTC"
   ```

2. The MCP servers will be automatically installed when first used.

## MCP Servers

### 1. MySQL MCP Server
Read-only MySQL database access with security features for production environments
- **Source**: https://github.com/mysql/mysql-mcp-server
- **Package**: `uvx mysql-mcp-server`
- **Transport**: stdio
- **Authentication**: MySQL credentials
- **Environment**: `MYSQL_HOST`, `MYSQL_PORT`, `MYSQL_DATABASE`, `MYSQL_USER`, `MYSQL_PASSWORD`

### 2. AntV Chart Generator
Create performance charts and query result visualizations
- **Source**: https://github.com/antvis/mcp-server-chart
- **Package**: `npx -y @antvis/mcp-server-chart`
- **Transport**: stdio
- **Authentication**: None required

### 3. VChart Interactive Charts
Advanced interactive dashboards for MySQL monitoring and analysis
- **Source**: https://github.com/visactor/vchart-mcp-server
- **Package**: `npx -y @visactor/vchart-mcp-server`
- **Transport**: stdio
- **Authentication**: None required

### 4. Filesystem Server
SQL script management and configuration file handling
- **Source**: https://github.com/modelcontextprotocol/servers
- **Package**: `npx -y @modelcontextprotocol/server-filesystem`
- **Transport**: stdio
- **Authentication**: Directory permissions
- **Environment**: `ALLOWED_DIRECTORIES`

### 5. Git MCP Server
Version control for database schemas, migrations, and configurations
- **Source**: https://github.com/modelcontextprotocol/servers
- **Package**: `uvx mcp-server-git`
- **Transport**: stdio
- **Authentication**: Git credentials

### 6. Memory Knowledge Graph
Documentation and relationship management for database schemas
- **Source**: https://github.com/modelcontextprotocol/servers
- **Package**: `npx -y @modelcontextprotocol/server-memory`
- **Transport**: stdio
- **Authentication**: None required

### 7. Time Operations Server
Timezone handling essential for web applications and global deployments
- **Source**: https://github.com/modelcontextprotocol/servers
- **Package**: `npx -y @modelcontextprotocol/server-time`
- **Transport**: stdio
- **Authentication**: None required
- **Environment**: `DEFAULT_TIMEZONE`

## Toolsets

### 1. production-admin (default)
Core MySQL administration and monitoring for production environments

**Tools:**
- `mysql.query` - Execute read-only SQL queries safely
- `mysql.show_tables` - List all tables in the current database
- `mysql.describe` - Show table structure and column information
- `mysql.show_status` - Display server status variables and metrics
- `mysql.show_grants` - Check user privileges and permissions
- `filesystem.read_text_file` - Read SQL scripts and configuration files
- `filesystem.list_directory` - Browse directories containing database assets
- `git.git_status` - Check version control status of database scripts
- `git.git_commit` - Commit database configuration changes
- `memory.create_entities` - Document database objects and relationships
- `memory.search_nodes` - Find documented database information

**Common Workflows:**
- Daily health checks and server status monitoring
- User privilege auditing and security reviews
- Database schema documentation and relationship mapping
- Configuration file management and version control
- Production database maintenance routines

### 2. performance-tuning
MySQL query optimization and InnoDB performance analysis

**Tools:**
- `mysql.query` - Execute performance testing queries
- `mysql.explain` - Analyze query execution plans
- `mysql.show_status` - Monitor performance metrics and counters
- `chart.create_line_chart` - Visualize performance trends over time
- `chart.create_bar_chart` - Compare performance metrics across queries/tables
- `vchart.create_performance_dashboard` - Build comprehensive performance dashboards
- `filesystem.read_text_file` - Analyze slow query logs and configuration files
- `memory.add_observations` - Document performance insights and optimizations
- `time.get_current_time` - Timestamp performance measurements
- `time.convert_timezone` - Handle timezone-specific performance analysis

**Common Workflows:**
- Slow query analysis and optimization
- Index usage analysis and recommendations
- InnoDB buffer pool and cache optimization
- Query execution plan analysis and tuning
- Performance trending and capacity planning
- MySQL configuration optimization for web workloads

### 3. development-ops
Web development workflow and schema migration support

**Tools:**
- `mysql.query` - Execute schema queries and data validation
- `mysql.show_tables` - Verify migration results and schema changes
- `mysql.describe` - Validate table structures after migrations
- `filesystem.read_text_file` - Read migration scripts and SQL files
- `filesystem.write_file` - Create migration scripts and documentation
- `filesystem.create_directory` - Organize migration and script directories
- `git.git_status` - Track changes to database schemas
- `git.git_add` - Stage migration files for version control
- `git.git_commit` - Commit schema changes with proper messages
- `git.git_diff` - Review schema changes before deployment
- `memory.create_entities` - Document migration procedures and dependencies

**Common Workflows:**
- Schema migration planning and execution
- Development environment database setup
- Integration with web application deployment pipelines
- Database change management and rollback procedures
- Developer support for database-related issues
- SQL script organization and version control

### 4. web-stack-integration
LAMP/LEMP stack optimization and e-commerce database management

**Tools:**
- `mysql.query` - Monitor web application database queries
- `mysql.show_status` - Track connection pools and web traffic metrics
- `mysql.show_grants` - Audit web application database permissions
- `time.get_current_time` - Handle session management and timestamps
- `time.convert_timezone` - Manage multi-timezone e-commerce operations
- `time.format_time` - Format timestamps for web application compatibility
- `chart.create_time_series` - Monitor web traffic and database load patterns
- `vchart.create_alert_dashboard` - Build real-time monitoring dashboards
- `filesystem.read_text_file` - Review web application database configurations
- `memory.read_graph` - Access documented integration patterns and optimizations

**Common Workflows:**
- Web application database connection optimization
- E-commerce transaction monitoring and optimization
- Session management and user authentication database support
- Multi-timezone handling for global web applications
- Database scaling for high-traffic web applications
- Integration with Redis/Memcached for web application caching

## Common Use Cases

### 1. Daily Production Health Check
- Check server status and key performance metrics
- Review active connections and resource usage
- Audit recent queries and identify any performance issues
- Validate backup status and replication health
- Document any issues in the knowledge graph

### 2. Query Performance Optimization
- Analyze slow query logs and identify bottlenecks
- Use EXPLAIN to understand query execution plans
- Create performance charts to visualize improvements
- Test index modifications and optimization strategies
- Document optimization results for future reference

### 3. Web Application Database Scaling
- Monitor connection pool utilization and adjust settings
- Analyze query patterns from web application traffic
- Optimize database schema for web application performance
- Plan for traffic spikes and seasonal load increases
- Integrate with application-level caching strategies

### 4. Schema Migration Management
- Plan and test database schema changes
- Create and version migration scripts
- Execute migrations with proper rollback procedures
- Validate schema changes against application requirements
- Document migration procedures and dependencies

### 5. E-commerce Database Optimization
- Optimize product catalog and inventory queries
- Handle timezone-specific operations for global customers
- Monitor transaction processing performance
- Plan for seasonal traffic and sales events
- Ensure data consistency across high-volume operations

## Configuration

### Environment Variables
- `MYSQL_HOST`: MySQL server hostname or IP address (required)
- `MYSQL_PORT`: MySQL server port, typically 3306 (required)
- `MYSQL_DATABASE`: Default database to connect to (required)
- `MYSQL_USER`: MySQL username with appropriate privileges (required)
- `MYSQL_PASSWORD`: MySQL password (required)
- `ALLOWED_DIRECTORIES`: Comma-separated list of allowed directories for filesystem access (required)
- `DEFAULT_TIMEZONE`: Default timezone for time operations, e.g., "UTC", "America/New_York" (optional)

### Customization
To customize the persona:
1. Edit `mcp.json` to modify server configurations or add additional MySQL instances
2. Edit `persona.yaml` to adjust toolsets or add new tools
3. Configure `ALLOWED_DIRECTORIES` to include your SQL script and configuration directories
4. Set up proper MySQL user with read-only privileges for security

## Best Practices

- **Security First**: Always use dedicated MySQL users with minimal required privileges for MCP access
- **Read-Only Operations**: Use read-only database connections to prevent accidental data modifications
- **Version Control**: Keep all database schemas, migrations, and configurations in version control
- **Performance Monitoring**: Regularly monitor MySQL performance metrics and set up alerting
- **Documentation**: Document all database changes, optimizations, and operational procedures
- **Backup Validation**: Regularly test backup and recovery procedures
- **Connection Management**: Monitor and optimize database connection pools for web applications
- **Timezone Awareness**: Always handle timezone operations explicitly for web applications
- **Index Strategy**: Regularly review and optimize indexes for web application query patterns
- **Capacity Planning**: Monitor growth trends and plan for scaling before performance degrades

## Troubleshooting

### Common Issues

1. **MySQL Connection Failures**
   - Verify MySQL server is running and accessible
   - Check network connectivity and firewall rules
   - Validate MySQL credentials and user permissions
   - Ensure database exists and user has access

2. **Permission Denied Errors**
   - Verify MySQL user has required privileges (SELECT, SHOW, etc.)
   - Check that ALLOWED_DIRECTORIES includes necessary paths
   - Ensure filesystem permissions allow access to SQL files
   - Review MySQL security settings and user grants

3. **Chart Generation Failures**
   - Verify Node.js is installed for chart MCP servers
   - Check that query results have appropriate data for visualization
   - Ensure chart server packages are properly installed
   - Review chart configuration parameters

4. **Performance Analysis Issues**
   - Enable MySQL slow query log for analysis
   - Verify EXPLAIN output formatting
   - Check that performance schema is enabled
   - Ensure sufficient privileges for performance monitoring

5. **Time Zone Related Problems**
   - Set DEFAULT_TIMEZONE environment variable
   - Verify MySQL time_zone settings
   - Check system timezone configuration
   - Validate timezone data in MySQL installation

## Support

For issues with:
- This persona configuration: Open an issue in the awesome-mcp-personas repository
- MySQL MCP server: Check the mysql-mcp-server documentation and GitHub repository
- Chart servers: Refer to AntV and VChart documentation
- MySQL database issues: Consult MySQL official documentation and community resources

## Contributing

To improve this persona:
1. Test each toolset with real MySQL environments
2. Validate all tool names against actual mysql-mcp-server implementation
3. Document additional MySQL optimization use cases
4. Submit improvements via pull request with detailed testing results
5. Report any MySQL-specific issues or missing functionality

## License

This persona configuration is part of the Awesome MCP Personas project and follows the same licensing terms.