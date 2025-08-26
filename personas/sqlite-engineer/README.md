# SQLite Engineer Persona

## Overview
SQLite Engineer specializing in local development, mobile applications, embedded systems, and lightweight database operations with comprehensive development support. This persona provides tools for rapid prototyping, data analysis, application integration, and resource-optimized database operations for edge devices and local storage scenarios.

## Target Audience
- Frontend/Mobile Developers using SQLite for local storage and offline-first applications
- Python/Desktop Application Developers implementing local database solutions
- Data Scientists using SQLite for analysis, prototyping, and data exploration
- Embedded Systems Engineers deploying SQLite in IoT/Edge devices with resource constraints
- Solo Developers and Small Teams requiring lightweight, serverless database solutions

## Prerequisites
- SQLite3 installed on your system
- Node.js (for Chart and official MCP servers)
- Python with uvx (for SQLite and Git MCP servers)
- Git configured for version control (optional but recommended)
- Basic understanding of SQL and database concepts

## Installation

1. Set up your environment variables:
   ```bash
   export SQLITE_DB_PATH="/path/to/your/database.db"
   export ALLOWED_DIRECTORIES="/path/to/your/project,/path/to/backup/location"
   export GIT_AUTHOR_NAME="Your Name"
   export GIT_AUTHOR_EMAIL="your.email@example.com"
   export DEFAULT_TIMEZONE="UTC"
   ```

2. The MCP servers will be automatically installed when first used.

## MCP Servers

### 1. SQLite Server
Comprehensive SQLite database operations for local development and embedded systems.
- **Source**: https://github.com/sqlite/mcp-sqlite
- **Package**: `uvx mcp-sqlite`
- **Transport**: stdio
- **Authentication**: None (local file-based)
- **Environment**: `SQLITE_DB_PATH` (database file location)

### 2. Chart Visualization Server
Create comprehensive visualizations for SQLite data analysis and performance monitoring.
- **Source**: https://github.com/antvis/mcp-server-chart
- **Package**: `npx -y @antvis/mcp-server-chart`
- **Transport**: stdio
- **Authentication**: None
- **Environment**: None required

### 3. Filesystem Server
Secure file operations for database management, backups, and project organization.
- **Source**: https://github.com/modelcontextprotocol/servers/tree/main/src/filesystem
- **Package**: `npx -y @modelcontextprotocol/server-filesystem`
- **Transport**: stdio
- **Authentication**: None
- **Environment**: `ALLOWED_DIRECTORIES` (comma-separated paths)

### 4. Git Version Control Server
Version control operations for database schema, migration scripts, and configuration management.
- **Source**: https://github.com/cyanheads/git-mcp-server
- **Package**: `uvx @cyanheads/git-mcp-server`
- **Transport**: stdio
- **Authentication**: Git credentials
- **Environment**: `GIT_AUTHOR_NAME`, `GIT_AUTHOR_EMAIL`

### 5. Memory Knowledge Server
Knowledge graph for project documentation, schema relationships, and development insights.
- **Source**: https://github.com/modelcontextprotocol/servers/tree/main/src/memory
- **Package**: `npx -y @modelcontextprotocol/server-memory`
- **Transport**: stdio
- **Authentication**: None
- **Environment**: None required

### 6. Time Operations Server
Time and timezone utilities for SQLite applications and temporal data management.
- **Source**: https://github.com/modelcontextprotocol/servers/tree/main/src/time
- **Package**: `npx -y @modelcontextprotocol/server-time`
- **Transport**: stdio
- **Authentication**: None
- **Environment**: `DEFAULT_TIMEZONE` (optional, defaults to system timezone)

## Toolsets

### 1. local-development (default)
SQLite development and rapid prototyping with file management and visualization.

**Tools:**
- `sqlite.execute` - Execute SQL statements and data operations
- `sqlite.list_tables` - Discover database schema and tables
- `sqlite.describe_table` - Analyze table structure and constraints
- `sqlite.analyze` - Performance optimization and statistics
- `filesystem.read_text_file` - Load SQL scripts and configurations
- `filesystem.write_file` - Save query results and backup data
- `filesystem.list_directory` - Explore project structure
- `chart.create_line_chart` - Visualize data trends and performance
- `chart.create_bar_chart` - Display categorical data comparisons

**Common Workflows:**
- Rapid prototyping with immediate schema creation and data loading
- Interactive development with real-time query execution and visualization
- Performance tuning with analysis tools and optimization recommendations
- Project setup with directory structure and initial database creation

### 2. data-analysis
Data analysis and research workflows with SQLite visualization and time operations.

**Tools:**
- `sqlite.execute` - Complex analytical queries and data processing
- `sqlite.analyze` - Database optimization and performance analysis
- `sqlite.pragma` - Advanced database configuration and integrity checks
- `chart.create_line_chart` - Trend analysis and time-series visualization
- `chart.create_time_series` - Temporal data analysis and monitoring
- `time.get_current_time` - Timestamp generation for analysis
- `time.format_time` - Data presentation and export formatting
- `memory.create_entities` - Document analytical insights and patterns
- `memory.search_nodes` - Retrieve previous analysis and findings

**Common Workflows:**
- Statistical analysis with aggregation queries and trend visualization
- Data exploration with schema discovery and pattern recognition
- Research workflows with hypothesis testing and result documentation
- Time-based analysis with temporal queries and timezone handling

### 3. application-integration
Mobile and desktop application database development with comprehensive project management.

**Tools:**
- `sqlite.execute` - Application data operations and business logic
- `sqlite.list_tables` - Schema validation and ORM mapping
- `sqlite.describe_table` - Structure analysis for code generation
- `sqlite.pragma` - Application-specific optimization and security settings
- `git.git_status` - Track schema changes and migration files
- `git.git_add` - Stage database modifications for version control
- `git.git_commit` - Commit schema evolution and feature changes
- `filesystem.create_directory` - Project structure and organization
- `filesystem.write_file` - Configuration files and data export
- `time.convert_timezone` - Multi-timezone application support

**Common Workflows:**
- Mobile app development with offline-first database design
- Desktop application integration with local storage optimization
- Schema migration management with version control and rollback capability
- Multi-platform deployment with configuration management and testing

### 4. embedded-systems
IoT and edge device database operations with resource optimization and backup strategies.

**Tools:**
- `sqlite.execute` - Lightweight data operations for constrained environments
- `sqlite.pragma` - Resource optimization and memory management
- `sqlite.analyze` - Performance tuning for limited hardware
- `filesystem.read_text_file` - Configuration loading and script execution
- `filesystem.list_directory` - System monitoring and file management
- `git.git_diff` - Change tracking and deployment verification
- `memory.add_observations` - Performance monitoring and system insights
- `time.calculate_duration` - Timing analysis and performance measurement

**Common Workflows:**
- IoT device database optimization with minimal resource usage
- Edge computing with local data processing and synchronization
- Embedded system monitoring with performance tracking and alerting
- Backup and recovery strategies for distributed edge deployments

## Common Use Cases

### 1. Mobile Application Development
- Set up SQLite database with `sqlite.execute` for app-specific schema
- Use `sqlite.pragma` to optimize for mobile storage and battery life
- Implement offline-first data synchronization with `time.convert_timezone`
- Track schema evolution with `git.git_commit` for app updates
- Visualize user engagement data with `chart.create_line_chart`

### 2. Data Analysis and Research
- Load research datasets with `filesystem.read_text_file` and `sqlite.execute`
- Perform statistical analysis with complex SQL queries and aggregations
- Create comprehensive visualizations with `chart.create_time_series`
- Document findings and methodology with `memory.create_entities`
- Export results with `filesystem.write_file` for publication

### 3. Rapid Prototyping and Development
- Initialize project structure with `filesystem.create_directory`
- Create proof-of-concept databases with `sqlite.execute`
- Iterate on schema design with `sqlite.describe_table` analysis
- Optimize performance with `sqlite.analyze` recommendations
- Track prototype evolution with `git.git_status` and version control

### 4. IoT and Edge Device Deployment
- Configure resource-optimized databases with `sqlite.pragma` settings
- Implement lightweight data logging with minimal `sqlite.execute` operations
- Monitor system performance with `time.calculate_duration` tracking
- Backup critical data with `filesystem.write_file` strategies
- Document system behavior with `memory.add_observations`

## Configuration

### Environment Variables
- `SQLITE_DB_PATH`: Path to your SQLite database file (required)
- `ALLOWED_DIRECTORIES`: Comma-separated list of accessible directories (required)
- `GIT_AUTHOR_NAME`: Git author name for commits (required for version control)
- `GIT_AUTHOR_EMAIL`: Git author email for commits (required for version control)
- `DEFAULT_TIMEZONE`: Default timezone for time operations (optional, defaults to system)

### Customization
To customize the persona:
1. Edit `mcp.json` to modify server configurations or add database-specific settings
2. Edit `persona.yaml` to adjust toolsets or add specialized tools for your use case
3. Ensure all changes comply with the MCP schema and maintain security best practices

## Best Practices

- **Database Security**: Use `sqlite.pragma` to enable appropriate security settings (foreign keys, secure delete)
- **Performance Optimization**: Regularly run `sqlite.analyze` to maintain query performance statistics
- **Version Control**: Always version control schema changes and migration scripts using git tools
- **Resource Management**: For embedded systems, use `sqlite.pragma` to minimize memory and storage usage
- **Backup Strategy**: Implement regular backups using filesystem tools, especially for production mobile apps
- **Time Handling**: Use time server tools for consistent timezone handling in global applications
- **Documentation**: Maintain project knowledge with memory server for team collaboration
- **Testing**: Use separate databases for development, testing, and production environments

## Troubleshooting

### Common Issues

1. **Database locked errors**
   - Ensure proper transaction handling with `sqlite.execute`
   - Check for long-running connections in mobile applications
   - Use `sqlite.pragma` to configure appropriate timeout settings

2. **Performance issues on mobile devices**
   - Run `sqlite.analyze` to update query planner statistics
   - Use `sqlite.pragma` to optimize for mobile storage (journal mode, synchronous settings)
   - Consider implementing connection pooling for high-traffic apps

3. **File permission errors**
   - Verify `ALLOWED_DIRECTORIES` includes your database location
   - Check filesystem permissions for SQLite database files
   - Ensure backup directories are accessible with proper permissions

4. **Git authentication issues**
   - Verify `GIT_AUTHOR_NAME` and `GIT_AUTHOR_EMAIL` are set correctly
   - Configure Git credentials for repository access
   - Check SSH keys or token authentication for remote repositories

5. **Timezone handling problems**
   - Set `DEFAULT_TIMEZONE` environment variable appropriately
   - Use `time.convert_timezone` for multi-timezone applications
   - Store timestamps in UTC and convert for display

## Support

For issues with:
- This persona configuration: Open an issue in the awesome-mcp-personas repository
- Individual MCP servers: Check respective server documentation
- SQLite operations: Refer to SQLite official documentation
- Mobile/embedded deployment: Consult platform-specific SQLite integration guides

## Contributing

To improve this persona:
1. Verify all tool names against actual MCP server implementations
2. Test each toolset with real-world mobile and embedded scenarios
3. Document any additional tools or optimizations discovered
4. Submit improvements via pull request with detailed testing results

## License

This persona configuration is part of the Awesome MCP Personas project and follows the same licensing terms.