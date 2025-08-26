# {{PERSONA_NAME}} Persona

## Overview
{{DESCRIPTION}}

## Target Audience
{{TARGET_AUDIENCE_LIST}}

## Prerequisites
{{PREREQUISITES_LIST}}

## MCP Servers

{{#each MCP_SERVERS}}
### {{@index}}. {{name}}
{{description}}
- **Source**: {{source}}
- **Package**: {{package}}  
- **Transport**: {{transport}}
- **Authentication**: {{authentication}}
{{#if environment}}
- **Environment**: {{environment}}
{{/if}}

{{/each}}

## Toolsets

{{#each TOOLSETS}}
### {{@index}}. {{name}}{{#if isDefault}} (default){{/if}}
{{description}}

**Tools:**
{{#each tools}}
- `{{id}}` - {{description}}
{{/each}}

**Common Workflows:**
{{#each workflows}}
- {{this}}
{{/each}}

{{/each}}

## Common Use Cases

{{#each USE_CASES}}
### {{@index}}. {{name}}
{{#each steps}}
- {{this}}
{{/each}}

{{/each}}

## Configuration

### Environment Variables
{{#each ENV_VARIABLES}}
- `{{name}}`: {{description}} {{#if required}}(required){{else}}(optional){{/if}}
{{/each}}

### Customization
To customize the persona:
1. Edit `mcp.json` to modify server configurations
2. Edit `persona.yaml` to adjust toolsets or add new tools
3. Ensure all changes comply with the MCP schema

## Best Practices

{{BEST_PRACTICES_LIST}}

## Troubleshooting

### Common Issues

{{#each TROUBLESHOOTING}}
1. **{{issue}}**
{{#each solutions}}
   - {{this}}
{{/each}}

{{/each}}

## Support

For issues with:
- This persona configuration: Open an issue in the awesome-mcp-personas repository
- Individual MCP servers: Check respective server documentation
- API services: Refer to service provider documentation

## Contributing

To improve this persona:
1. Verify all tool names against actual MCP server implementations
2. Test each toolset with real-world scenarios
3. Document any additional tools discovered
4. Submit improvements via pull request

## License

This persona configuration is part of the Awesome MCP Personas project and follows the same licensing terms.