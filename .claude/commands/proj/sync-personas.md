# /sync-personas

Scans the personas directory and automatically updates the top-level README.md with any new or missing personas, following all established guidelines for categorization, emoji labeling, and table formatting.

## Usage

```
/sync-personas
```

## What it does

1. **Scans personas directory** - Discovers all valid persona configurations
2. **Validates persona structure** - Ensures required files exist (mcp.json, README.md, persona.yaml)
3. **Analyzes MCP configurations** - Determines appropriate emoji labels based on server requirements
4. **Categorizes personas** - Places personas in correct README sections based on their purpose
5. **Updates README table** - Adds missing personas to appropriate category tables
6. **Preserves existing entries** - Does not modify existing persona entries, only adds new ones

## Emoji Label Detection

The command automatically assigns emoji labels based on MCP server analysis:

- 🔐 **Secrets Required** - Detects environment variables with credentials/API keys
- 🌐 **Remote Services** - Identifies cloud services, APIs, and external connections  
- 💻 **Local Only** - No external dependencies or credentials required
- ⚙️ **Configuration** - Requires environment variable setup
- 🚀 **Zero Setup** - Works immediately without configuration
- 📦 **External Dependencies** - Requires additional tools/services
- 🏢 **Enterprise** - Production/enterprise-focused configurations

## Category Assignment

Personas are automatically categorized based on:

- **Filename patterns** (e.g., `*-dba`, `*-sre`, `*-engineer`)
- **MCP server types** (database, cloud, monitoring tools)
- **Description keywords** from persona.yaml and README.md
- **Established patterns** from existing personas

## Requirements

- Persona must have valid `mcp.json`, `README.md`, and `persona.yaml`
- README.md must contain a clear description
- persona.yaml should specify the persona's purpose and target audience

## Example Output

```
Found 3 new personas to add:
✓ rust-developer → Software Engineering (💻🚀)
✓ mongodb-dba → Data Science & Analytics (🔐⚙️🏢) 
✓ kubernetes-sre → DevOps & Infrastructure (🔐🌐⚙️🏢)

Updated README.md with 3 new personas
```