# PostgreSQL DBA Persona - Tool Reference

This document provides a comprehensive reference for all tools available in the PostgreSQL DBA persona, organized by MCP server.

## PostgreSQL Core Operations (postgres)

### Database Query Operations
- **`postgres.execute_query`** - Execute SQL queries and administrative commands with result formatting
- **`postgres.analyze_query`** - Analyze query performance, execution time, and resource usage
- **`postgres.explain_query`** - Generate detailed query execution plans with cost analysis

### Schema Management  
- **`postgres.list_tables`** - List all tables in the database with metadata
- **`postgres.describe_table`** - Get detailed table schema, columns, constraints, and indexes
- **`postgres.get_schema`** - Retrieve complete database schema with relationships

### User and Security Management
- **`postgres.list_users`** - List database users, roles, and their attributes
- **`postgres.check_permissions`** - Verify user permissions and access rights for objects
- **`postgres.get_stats`** - Retrieve database performance and usage statistics

## PostgreSQL Operations (postgres-ops)

### Connection and Session Management
- **`postgres-ops.monitor_connections`** - Monitor active database connections and session details
- **`postgres-ops.check_connection_limits`** - Check connection pool limits and availability

### Performance Monitoring
- **`postgres-ops.analyze_slow_queries`** - Identify and analyze slow-running queries
- **`postgres-ops.get_index_usage`** - Analyze index usage statistics and effectiveness
- **`postgres-ops.check_lock_waits`** - Monitor database locks, waits, and blocking queries
- **`postgres-ops.get_table_stats`** - Get detailed table statistics and usage metrics

### Maintenance and Optimization
- **`postgres-ops.check_vacuum_stats`** - Check autovacuum statistics, last run times, and effectiveness
- **`postgres-ops.monitor_autovacuum`** - Track autovacuum operations and configuration tuning
- **`postgres-ops.check_bloat`** - Analyze table and index bloat for maintenance planning

### System Resource Monitoring
- **`postgres-ops.check_disk_usage`** - Monitor database disk space usage and growth trends
- **`postgres-ops.monitor_cpu_usage`** - Track database CPU utilization and performance impact

### Backup and Recovery
- **`postgres-ops.monitor_backup_status`** - Verify backup completion status and integrity
- **`postgres-ops.get_error_log`** - Retrieve and analyze PostgreSQL error logs

### Replication Management
- **`postgres-ops.monitor_replication`** - Monitor PostgreSQL replication lag and status

### Security and Compliance
- **`postgres-ops.check_security_audit`** - Perform security audit checks and compliance validation
- **`postgres-ops.validate_configuration`** - Validate PostgreSQL configuration parameters

### Schema Development
- **`postgres-ops.validate_schema`** - Validate database schema integrity and consistency
- **`postgres-ops.generate_migration`** - Generate database migration scripts from schema changes

## Visualization and Charting (chart, vchart)

### Basic Chart Creation
- **`chart.create_line_chart`** - Create line charts for performance trends and time-series data
- **`chart.create_bar_chart`** - Generate bar charts for performance comparisons and metrics
- **`chart.create_time_series`** - Create time-based monitoring charts with data points

### Advanced Dashboards
- **`vchart.create_performance_dashboard`** - Build comprehensive interactive performance dashboards
- **`vchart.create_alert_dashboard`** - Create alert and monitoring dashboards with real-time updates

## File System Operations (filesystem)

### File Management
- **`filesystem.read_text_file`** - Read SQL scripts, configuration files, and documentation
- **`filesystem.write_file`** - Write migration scripts, reports, and configuration files
- **`filesystem.list_directory`** - List database script directories and file structures
- **`filesystem.create_directory`** - Create organized directory structures for scripts and documentation

## Version Control (git)

### Git Operations
- **`git.git_status`** - Check version control status of database schema changes
- **`git.git_add`** - Stage database schema changes and migration scripts for commit
- **`git.git_commit`** - Commit database migrations and configuration changes
- **`git.git_diff`** - Review differences in database schemas and configuration files

## Knowledge Management (memory)

### Documentation and Relationships
- **`memory.create_entities`** - Create and document database schema relationships and processes
- **`memory.search_nodes`** - Search documented database relationships and procedures  
- **`memory.add_observations`** - Add notes and observations about database changes and performance
- **`memory.read_graph`** - Access documented monitoring procedures and relationships

## Time Operations (time)

### Time Management
- **`time.get_current_time`** - Get current timestamp for performance tracking and logging
- **`time.convert_timezone`** - Handle timezone conversions for distributed PostgreSQL systems
- **`time.format_time`** - Format timestamps for reports and documentation
- **`time.calculate_duration`** - Calculate time durations for SLA tracking and performance analysis

## Tool Usage by Toolset

### Production Admin Toolset
**Primary Focus**: Core PostgreSQL administration and monitoring
- PostgreSQL Core: `execute_query`, `list_tables`, `describe_table`, `get_schema`, `list_users`, `check_permissions`
- PostgreSQL Ops: `monitor_connections`, `check_vacuum_stats`, `get_table_stats`, `monitor_replication`, `check_bloat`

### Performance Tuning Toolset  
**Primary Focus**: Query optimization and performance analysis
- PostgreSQL Core: `analyze_query`, `explain_query`, `get_stats`
- PostgreSQL Ops: `analyze_slow_queries`, `get_index_usage`, `check_lock_waits`, `monitor_autovacuum`
- Visualization: `create_line_chart`, `create_bar_chart`, `create_performance_dashboard`
- Time: `get_current_time`, `convert_timezone`

### Development Ops Toolset
**Primary Focus**: Schema management and development workflows
- Filesystem: `read_text_file`, `write_file`, `list_directory`, `create_directory`  
- Git: `git_status`, `git_add`, `git_commit`, `git_diff`
- Memory: `create_entities`, `search_nodes`, `add_observations`
- PostgreSQL Ops: `validate_schema`, `generate_migration`

### Monitoring Alerts Toolset
**Primary Focus**: Real-time monitoring and alerting
- PostgreSQL Ops: `check_disk_usage`, `monitor_cpu_usage`, `check_connection_limits`, `monitor_backup_status`, `get_error_log`, `check_security_audit`, `validate_configuration`
- Visualization: `create_time_series`, `create_alert_dashboard`
- Memory: `read_graph`
- Time: `format_time`, `calculate_duration`

## Best Practices by Tool Category

### Query and Performance Tools
- Always run `explain_query` before `execute_query` for complex operations
- Use `analyze_query` to understand performance implications
- Monitor `slow_queries` regularly and optimize identified issues
- Leverage visualization tools to track performance trends over time

### Administrative Tools  
- Use `list_users` and `check_permissions` for regular security audits
- Monitor `connections` to prevent connection pool exhaustion
- Check `vacuum_stats` and `bloat` as part of routine maintenance
- Validate `configuration` changes before applying to production

### Development and Schema Tools
- Always use version control (`git.*`) for schema changes and migrations
- Validate schemas with `validate_schema` before deployment
- Document relationships with `memory.*` tools for knowledge preservation
- Generate migrations with `generate_migration` for consistency

### Monitoring and Alerting Tools
- Set up regular monitoring with `disk_usage`, `cpu_usage`, and `backup_status`
- Use visualization tools to create dashboards for operations teams  
- Track error logs with `get_error_log` for proactive issue identification
- Calculate durations with time tools for SLA compliance tracking

## Security Considerations

### Read-Only Operations
Most monitoring and analysis tools are read-only and safe for production use:
- All `postgres-ops.monitor_*` and `postgres-ops.check_*` tools
- Chart and visualization tools
- File system read operations
- Memory search and read operations

### Write Operations Requiring Caution
Tools that modify data or system state:
- `postgres.execute_query` - Can modify data, use with appropriate permissions
- `filesystem.write_file` - Creates files, ensure proper directory permissions
- `git.*` operations - Modify version control, use appropriate git permissions
- `memory.create_entities` and `memory.add_observations` - Modify knowledge graph

### Administrative Permissions Required
Tools requiring elevated database privileges:
- User management: `list_users`, `check_permissions`  
- Configuration: `validate_configuration`
- Security audits: `check_security_audit`
- Schema operations: `validate_schema`, `generate_migration`

## Error Handling and Troubleshooting

### Connection-Related Tools
If connection tools fail, verify:
- Database connectivity and credentials
- Network access and firewall rules
- Connection pool limits and availability

### Performance Tools
If performance tools timeout:
- Check for long-running queries blocking monitoring
- Verify system resources (CPU, memory, disk)
- Consider running during off-peak hours

### File System Tools  
If filesystem tools fail:
- Check ALLOWED_DIRS configuration
- Verify file and directory permissions
- Ensure paths exist and are accessible

### Visualization Tools
If chart tools fail:
- Verify data format and completeness
- Check for sufficient data points for visualization
- Ensure chart parameters are within valid ranges

This comprehensive tool reference provides PostgreSQL DBAs with detailed information about each available tool, their purposes, and best practices for effective database administration and monitoring.