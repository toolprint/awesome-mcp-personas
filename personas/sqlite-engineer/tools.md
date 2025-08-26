# SQLite Engineer Tools Reference

> Comprehensive tool reference for SQLite engineering, local development, and lightweight database operations.

## 💾 Core SQLite Database Tools

### SQLite Server (`sqlite`)
Comprehensive SQLite database operations for local development, mobile applications, and embedded systems.

#### **`sqlite.execute`**
Execute SQL statements on SQLite databases.
- **Usage**: Database operations, data manipulation, schema changes
- **Parameters**: SQL statement, database file path
- **Returns**: Query results, execution metadata
- **Applications**: Mobile app development, local storage, data analysis

#### **`sqlite.list_tables`**
List all tables in the SQLite database.
- **Usage**: Schema discovery, database exploration
- **Parameters**: Database file path
- **Returns**: Table names and basic information
- **Applications**: Development debugging, schema documentation

#### **`sqlite.describe_table`**
Get detailed table structure information from SQLite.
- **Usage**: Schema analysis, application development
- **Parameters**: Table name, database file path
- **Returns**: Column definitions, data types, constraints, indexes
- **Applications**: ORM mapping, migration planning

#### **`sqlite.analyze`**
Analyze SQLite database for optimization opportunities.
- **Usage**: Performance optimization, maintenance
- **Parameters**: Database file path, analysis options
- **Returns**: Performance statistics, optimization recommendations
- **Applications**: Mobile performance tuning, embedded optimization

#### **`sqlite.pragma`**
Execute SQLite PRAGMA commands for database configuration and analysis.
- **Usage**: Database tuning, security settings, integrity checks
- **Parameters**: PRAGMA command, database file path
- **Returns**: Configuration values, integrity results
- **Applications**: Security hardening, performance tuning, debugging

## 📊 Data Visualization Tools

### Chart Server (`chart`)
Create comprehensive visualizations for SQLite data analysis and performance monitoring.

#### **`chart.create_line_chart`**
Generate line charts for time-series data and trends.
- **Usage**: Performance monitoring, data trend visualization
- **Parameters**: Data points, labels, styling options
- **Returns**: Interactive line chart
- **Applications**: App usage trends, performance metrics

#### **`chart.create_bar_chart`**
Create bar charts for categorical data comparison.
- **Usage**: Data distribution analysis, comparison visualization
- **Parameters**: Categories, values, styling options
- **Returns**: Interactive bar chart
- **Applications**: Feature usage analysis, error categorization

#### **`chart.create_time_series`**
Build time-series charts for temporal data analysis.
- **Usage**: Time-based analysis, monitoring dashboards
- **Parameters**: Time data, metrics, time ranges
- **Returns**: Time-series visualization
- **Applications**: Real-time monitoring, historical analysis

## 📁 File Management Tools

### Filesystem Server (`filesystem`)
Secure file operations for SQLite database management and project organization.

#### **`filesystem.read_text_file`**
Read SQLite schema files, SQL scripts, and configuration files.
- **Usage**: Script loading, configuration reading
- **Parameters**: File path
- **Returns**: File contents
- **Applications**: Migration scripts, backup files

#### **`filesystem.write_file`**
Write SQLite backup files, export data, and save configurations.
- **Usage**: Data export, backup creation, configuration management
- **Parameters**: File path, content
- **Returns**: Write confirmation
- **Applications**: Automated backups, data export

#### **`filesystem.list_directory`**
List database files, backup directories, and project structure.
- **Usage**: Database discovery, backup management
- **Parameters**: Directory path
- **Returns**: File/directory listing
- **Applications**: Multi-database projects, backup verification

#### **`filesystem.create_directory`**
Create directories for database organization and project structure.
- **Usage**: Project setup, backup organization
- **Parameters**: Directory path
- **Returns**: Creation confirmation
- **Applications**: Project initialization, backup structure

## 🔄 Version Control Tools

### Git Server (`git`)
Version control operations for SQLite databases, schema changes, and migration scripts.

#### **`git.git_status`**
Check status of database files and migration scripts.
- **Usage**: Change tracking, deployment preparation
- **Parameters**: Repository path
- **Returns**: File status, staged changes, untracked files
- **Applications**: Schema versioning, migration tracking

#### **`git.git_add`**
Stage database files and schema changes for version control.
- **Usage**: Change preparation, selective staging
- **Parameters**: File paths
- **Returns**: Staging confirmation
- **Applications**: Incremental migrations, feature development

#### **`git.git_commit`**
Commit database schema changes and migration scripts.
- **Usage**: Version control, change documentation
- **Parameters**: Commit message, files
- **Returns**: Commit hash, status
- **Applications**: Release management, schema evolution

#### **`git.git_diff`**
Show differences in database schema and migration files.
- **Usage**: Change review, migration validation
- **Parameters**: File paths, commit references
- **Returns**: File differences, change details
- **Applications**: Code review, migration verification

## 🧠 Knowledge Management Tools

### Memory Server (`memory`)
Knowledge graph for project documentation, schema relationships, and development insights.

#### **`memory.create_entities`**
Create entities for database schemas, tables, and relationships.
- **Usage**: Schema documentation, relationship mapping
- **Parameters**: Entity data, relationships
- **Returns**: Entity creation confirmation
- **Applications**: Database documentation, architectural knowledge

#### **`memory.add_observations`**
Add observations about performance, usage patterns, and optimization insights.
- **Usage**: Knowledge capture, best practices documentation
- **Parameters**: Observation data, context
- **Returns**: Observation ID
- **Applications**: Performance notes, development insights

#### **`memory.search_nodes`**
Search for database-related knowledge and patterns.
- **Usage**: Knowledge retrieval, pattern discovery
- **Parameters**: Search criteria, filters
- **Returns**: Matching nodes and relationships
- **Applications**: Problem solving, pattern reuse

## ⏰ Time and Timezone Tools

### Time Server (`time`)
Time and timezone utilities for SQLite applications and data management.

#### **`time.get_current_time`**
Get current timestamp for logging and data operations.
- **Usage**: Timestamp generation, logging
- **Parameters**: Timezone, format options
- **Returns**: Formatted timestamp
- **Applications**: Audit trails, data synchronization

#### **`time.convert_timezone`**
Convert timestamps between timezones for global applications.
- **Usage**: Multi-timezone applications, data normalization
- **Parameters**: Source time, source zone, target zone
- **Returns**: Converted timestamp
- **Applications**: Global apps, distributed systems

#### **`time.format_time`**
Format timestamps for display and export.
- **Usage**: Data presentation, report generation
- **Parameters**: Timestamp, format specification
- **Returns**: Formatted time string
- **Applications**: User interfaces, data export

#### **`time.calculate_duration`**
Calculate time differences and durations.
- **Usage**: Performance measurement, scheduling
- **Parameters**: Start time, end time
- **Returns**: Duration calculation
- **Applications**: Performance monitoring, SLA tracking

---

## 🎯 Toolset Usage Patterns

### **local-development** Toolset
Core SQLite development and rapid prototyping with visualization.
- **Primary Tools**: `execute`, `list_tables`, `describe_table`, `analyze`
- **Support Tools**: File management, visualization
- **Workflows**: Schema development, data exploration, performance tuning

### **data-analysis** Toolset  
Data analysis and research workflows with comprehensive visualization.
- **Primary Tools**: `execute`, `analyze`, `pragma`
- **Support Tools**: Charts, time operations, knowledge capture
- **Workflows**: Data exploration, statistical analysis, insight generation

### **application-integration** Toolset
Mobile and desktop application database development.
- **Primary Tools**: `execute`, `list_tables`, `describe_table`, `pragma`
- **Support Tools**: Version control, project management, timezone handling
- **Workflows**: App development, schema migrations, multi-platform deployment

### **embedded-systems** Toolset
IoT and edge device database operations with resource optimization.
- **Primary Tools**: `execute`, `pragma`, `analyze`
- **Support Tools**: File operations, version control, knowledge management
- **Workflows**: Resource optimization, backup strategies, edge synchronization

---

## 📝 Common Usage Examples

### Database Development Workflow
```sql
-- Use sqlite.list_tables to explore database structure
-- Use sqlite.describe_table to understand schema
-- Use sqlite.execute to run development queries
-- Use filesystem.write_file to save results
-- Use git.git_add and git.git_commit to version changes
```

### Data Analysis Workflow  
```sql
-- Use sqlite.execute to query data
-- Use sqlite.analyze to optimize performance
-- Use chart.create_line_chart to visualize trends
-- Use memory.create_entities to document insights
-- Use time.format_time for temporal analysis
```

### Mobile Application Development
```sql
-- Use sqlite.pragma to configure for mobile optimization
-- Use sqlite.execute for app data operations
-- Use time.convert_timezone for global apps
-- Use filesystem.create_directory for app structure
-- Use git.git_status to track schema changes
```

### Embedded Systems Optimization
```sql
-- Use sqlite.pragma to minimize resource usage
-- Use sqlite.analyze for performance optimization
-- Use filesystem.read_text_file for configuration loading
-- Use memory.add_observations to track performance
-- Use time.calculate_duration for timing analysis
```