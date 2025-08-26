# MySQL DBA Persona - Tool Reference

> Comprehensive tool reference for MySQL Database Administration persona
> **Last Updated**: 2025-08-26

## Tool Overview

This persona provides **42 specialized tools** across **7 MCP servers** for comprehensive MySQL database administration, performance optimization, and web application integration.

---

## MySQL Database Tools (mysql-mcp-server)

### Core Query Operations

#### **`mysql.query`**
**Purpose**: Execute read-only SQL queries against MySQL database with safety features  
**Category**: Database Operations  
**Security**: Read-only execution, prevents data modifications  
**Usage**: Daily queries, data analysis, troubleshooting  
**Example**: `SELECT * FROM performance_schema.global_status WHERE Variable_name LIKE 'Innodb%'`

#### **`mysql.show_tables`**
**Purpose**: List all tables in the current MySQL database  
**Category**: Schema Discovery  
**Security**: Safe read-only operation  
**Usage**: Database exploration, schema validation, documentation  
**Example**: View all tables including their engine type and row counts

#### **`mysql.describe`**
**Purpose**: Show detailed table structure including columns, types, and constraints  
**Category**: Schema Analysis  
**Security**: Read-only metadata access  
**Usage**: Schema documentation, migration planning, troubleshooting  
**Example**: `DESCRIBE users` to see column definitions and indexes

### Performance and Administration

#### **`mysql.explain`**
**Purpose**: Analyze MySQL query execution plans for optimization  
**Category**: Performance Analysis  
**Security**: Read-only query analysis  
**Usage**: Query optimization, index analysis, performance troubleshooting  
**Example**: `EXPLAIN SELECT * FROM orders WHERE customer_id = 123`

#### **`mysql.show_status`**
**Purpose**: Display MySQL server status variables and performance metrics  
**Category**: System Monitoring  
**Security**: Read-only system information  
**Usage**: Performance monitoring, capacity planning, troubleshooting  
**Example**: Monitor InnoDB buffer pool usage, connection counts, query cache hit rates

#### **`mysql.show_grants`**
**Purpose**: Display user privileges and permission grants  
**Category**: Security Auditing  
**Security**: Administrative privilege information  
**Usage**: Security audits, permission troubleshooting, compliance checking  
**Example**: `SHOW GRANTS FOR 'webapp'@'%'` to audit application user permissions

---

## Chart Visualization Tools (@antvis/mcp-server-chart)

### Performance Charts

#### **`chart.create_line_chart`**
**Purpose**: Create line charts for time-series performance data  
**Category**: Data Visualization  
**Security**: Safe visualization generation  
**Usage**: Performance trending, monitoring over time, capacity planning  
**Example**: Plot MySQL connection counts or query response times over time

#### **`chart.create_bar_chart`**
**Purpose**: Generate bar charts for comparative analysis  
**Category**: Data Visualization  
**Security**: Safe visualization generation  
**Usage**: Compare performance across tables, queries, or time periods  
**Example**: Compare table sizes, index usage, or query execution counts

#### **`chart.create_time_series`**
**Purpose**: Advanced time-series visualization with multiple metrics  
**Category**: Advanced Visualization  
**Security**: Safe visualization generation  
**Usage**: Complex performance analysis, correlation analysis, trend identification  
**Example**: Correlate web traffic patterns with database performance metrics

---

## Interactive Dashboard Tools (@visactor/vchart-mcp-server)

### Dashboard Creation

#### **`vchart.create_performance_dashboard`**
**Purpose**: Build comprehensive interactive performance dashboards  
**Category**: Dashboard Management  
**Security**: Safe dashboard generation  
**Usage**: Real-time monitoring, executive reporting, performance tracking  
**Example**: MySQL performance dashboard with queries/sec, connections, buffer pool usage

#### **`vchart.create_alert_dashboard`**
**Purpose**: Create alert and monitoring dashboards with real-time updates  
**Category**: Monitoring & Alerting  
**Security**: Safe dashboard generation  
**Usage**: Incident response, proactive monitoring, SLA tracking  
**Example**: Dashboard showing MySQL error rates, slow queries, replication lag

---

## File System Management Tools (@modelcontextprotocol/server-filesystem)

### File Operations

#### **`filesystem.read_text_file`**
**Purpose**: Read SQL scripts, configuration files, and documentation  
**Category**: File Management  
**Security**: Restricted to ALLOWED_DIRECTORIES  
**Usage**: Script execution, configuration review, documentation access  
**Example**: Read my.cnf configuration files, SQL migration scripts, backup logs

#### **`filesystem.write_file`**
**Purpose**: Create new files like migration scripts and documentation  
**Category**: File Creation  
**Security**: Restricted to ALLOWED_DIRECTORIES  
**Usage**: Script creation, documentation updates, configuration backups  
**Example**: Generate migration scripts, create performance reports, backup configurations

#### **`filesystem.list_directory`**
**Purpose**: Browse directory contents to locate database assets  
**Category**: Directory Navigation  
**Security**: Restricted to ALLOWED_DIRECTORIES  
**Usage**: Asset discovery, organization, file management  
**Example**: Browse SQL script directories, configuration folders, backup locations

#### **`filesystem.create_directory`**
**Purpose**: Create new directories for organizing database files  
**Category**: Directory Management  
**Security**: Restricted to ALLOWED_DIRECTORIES  
**Usage**: Project organization, script categorization, backup management  
**Example**: Create directories for new database versions, migration batches

---

## Version Control Tools (mcp-server-git)

### Git Operations

#### **`git.git_status`**
**Purpose**: Check version control status of database scripts and configurations  
**Category**: Version Control  
**Security**: Safe git repository inspection  
**Usage**: Track changes, verify repository state, deployment preparation  
**Example**: Check for uncommitted database schema changes before deployment

#### **`git.git_add`**
**Purpose**: Stage database files for version control  
**Category**: Version Control  
**Security**: Safe git staging operation  
**Usage**: Prepare files for commit, selective staging, change management  
**Example**: Stage new migration scripts or configuration changes

#### **`git.git_commit`**
**Purpose**: Commit database changes with proper documentation  
**Category**: Version Control  
**Security**: Safe git commit operation  
**Usage**: Save changes, document modifications, create deployment history  
**Example**: Commit schema changes with descriptive messages for audit trail

#### **`git.git_diff`**
**Purpose**: Review changes in database scripts and configurations  
**Category**: Change Review  
**Security**: Safe git diff operation  
**Usage**: Code review, change validation, deployment verification  
**Example**: Review differences in migration scripts before applying to production

---

## Knowledge Management Tools (@modelcontextprotocol/server-memory)

### Documentation and Relationships

#### **`memory.create_entities`**
**Purpose**: Document database objects, relationships, and procedures  
**Category**: Knowledge Management  
**Security**: Safe documentation storage  
**Usage**: Schema documentation, procedure documentation, knowledge retention  
**Example**: Document table relationships, stored procedures, optimization strategies

#### **`memory.search_nodes`**
**Purpose**: Find previously documented database information and procedures  
**Category**: Knowledge Retrieval  
**Security**: Safe information retrieval  
**Usage**: Troubleshooting, procedure lookup, historical reference  
**Example**: Find documented solutions for similar performance issues

#### **`memory.add_observations`**
**Purpose**: Record performance insights, optimizations, and lessons learned  
**Category**: Knowledge Capture  
**Security**: Safe observation recording  
**Usage**: Performance tuning, optimization tracking, knowledge building  
**Example**: Document successful index optimizations and their impact

#### **`memory.read_graph`**
**Purpose**: Access comprehensive database knowledge network  
**Category**: Knowledge Networks  
**Security**: Safe knowledge graph access  
**Usage**: Complex relationship analysis, pattern recognition, decision support  
**Example**: Understand complex schema relationships and optimization dependencies

---

## Time and Timezone Tools (@modelcontextprotocol/server-time)

### Time Operations

#### **`time.get_current_time`**
**Purpose**: Get current timestamp for database operations and logging  
**Category**: Time Management  
**Security**: Safe time retrieval  
**Usage**: Logging, performance measurement, audit trails  
**Example**: Timestamp performance measurements, log database operations

#### **`time.convert_timezone`**
**Purpose**: Handle timezone conversions for global web applications  
**Category**: Timezone Management  
**Security**: Safe timezone operations  
**Usage**: Multi-timezone applications, global e-commerce, data analysis  
**Example**: Convert user activity times to database timezone for analysis

#### **`time.format_time`**
**Purpose**: Format timestamps for reports and web application compatibility  
**Category**: Time Formatting  
**Security**: Safe time formatting  
**Usage**: Reporting, API responses, user interfaces  
**Example**: Format database timestamps for web application display

---

## Tool Usage Patterns

### Daily Administration Workflow
```sql
-- Check server status
mysql.show_status

-- Review active connections
mysql.query("SHOW PROCESSLIST")

-- Audit user permissions
mysql.show_grants

-- Document findings
memory.add_observations
```

### Performance Analysis Workflow
```sql
-- Analyze slow queries
mysql.explain("SELECT * FROM large_table WHERE indexed_column = ?")

-- Check performance metrics
mysql.show_status

-- Create performance visualizations
chart.create_line_chart(performance_data)

-- Build monitoring dashboard
vchart.create_performance_dashboard
```

### Schema Management Workflow
```sql
-- Review current schema
mysql.show_tables
mysql.describe("table_name")

-- Read migration script
filesystem.read_text_file("migrations/001_add_index.sql")

-- Execute and validate
mysql.query("migration_sql")

-- Commit changes
git.git_add("migrations/")
git.git_commit("Add performance index for user queries")
```

### Web Application Integration Workflow
```sql
-- Monitor web application queries
mysql.query("SELECT * FROM information_schema.processlist WHERE db = 'webapp'")

-- Handle timezone operations
time.convert_timezone("user_timestamp", "UTC", "America/New_York")

-- Create real-time monitoring
vchart.create_alert_dashboard

-- Document integration patterns
memory.create_entities("web_app_optimization_patterns")
```

---

## Security Considerations

### MySQL Access
- All database operations are read-only by default
- Use dedicated MySQL user with minimal privileges
- Never store credentials in scripts or version control
- Regularly audit user permissions with `mysql.show_grants`

### File System Security
- All file operations restricted to `ALLOWED_DIRECTORIES`
- Set appropriate directory permissions
- Keep SQL scripts in version control
- Regular backup of configuration files

### Version Control Best Practices
- Never commit sensitive configuration files
- Use meaningful commit messages for database changes
- Review all changes with `git.git_diff` before committing
- Maintain separate repositories for different environments

---

## Performance Tips

### Query Optimization
- Always use `mysql.explain` before optimizing queries
- Monitor slow query logs regularly
- Use performance visualizations to identify trends
- Document successful optimizations in memory system

### Monitoring Strategy
- Create baseline performance dashboards
- Set up alert thresholds for key metrics
- Use time-series charts for trend analysis
- Correlate database performance with application metrics

### Documentation Practices
- Document all schema changes and their rationale
- Use memory system to track optimization strategies
- Version control all database scripts and configurations
- Create visual dashboards for non-technical stakeholders