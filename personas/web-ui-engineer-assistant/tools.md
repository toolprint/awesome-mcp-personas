# Web UI Engineer Assistant Tools Reference

Complete tool reference for the Web UI Engineer Assistant persona, covering browser automation, component systems, and advanced search capabilities.

## 🎭 Playwright Tools (@playwright/mcp)

### Core Navigation & Interaction
- **`browser_navigate`**: Navigate to URLs with configurable wait conditions
- **`browser_click`**: Click on page elements with selector support
- **`browser_type`**: Enter text into input fields and text areas
- **`browser_fill_form`**: Fill multiple form fields in a single operation
- **`browser_select_option`**: Select options from dropdown menus
- **`browser_file_upload`**: Upload files to file input elements

### Visual Capture & Testing
- **`browser_take_screenshot`**: Capture full page or element-specific screenshots
- **`browser_snapshot`**: Generate accessibility-focused page snapshots with DOM structure

### Debugging & Monitoring
- **`browser_console_messages`**: Retrieve browser console logs and error messages
- **`browser_network_requests`**: Monitor network requests and response data
- **`browser_handle_dialog`**: Manage browser alerts, confirms, and prompts

### Configuration Options
- **Browser Types**: Chrome, Firefox, WebKit
- **Execution Modes**: Headless (default) or headed for visual debugging
- **Device Emulation**: Mobile and tablet viewport simulation
- **Network Conditions**: Throttling and offline simulation

## 🎨 ShadCN UI Tools (@jpisnice/shadcn-ui-mcp-server)

### Component Discovery
- **Component Browsing**: Access complete shadcn/ui component library
- **Source Code Access**: Retrieve component implementation code
- **Demo Examples**: View working examples and usage patterns
- **Metadata Retrieval**: Get component properties, types, and dependencies

### Multi-Framework Support
- **React Components**: Default shadcn/ui React implementation
- **Vue Components**: Vue.js adaptations of shadcn components
- **Svelte Components**: Svelte versions with reactive patterns

### Advanced Features
- **Block Implementations**: Access complex layouts (dashboards, forms, authentication pages)
- **Component Variants**: Different styling and behavior variants
- **Theme Integration**: Design token and theming system access
- **Caching System**: Smart GitHub API caching for improved performance

### Usage Patterns
- **Component Integration**: Direct code insertion with proper imports
- **Customization Guidance**: Best practices for component modification
- **Accessibility Features**: WCAG-compliant implementations
- **Performance Optimization**: Optimized component patterns

## 🔍 Exa Search Tools (exa-mcp-server)

### Core Search Capabilities
- **`web_search_exa`**: AI-powered web search with intelligent filtering and ranking
- **`company_research`**: Targeted research on companies, products, and technologies
- **`linkedin_search`**: Professional network and talent research

### Advanced Research Workflows
- **`deep_researcher_start`**: Initialize comprehensive multi-stage research projects
- **`deep_researcher_check`**: Monitor and continue ongoing research processes
- **`crawling`**: Systematic website exploration and content extraction

### Search Optimization
- **AI Filtering**: Machine learning-powered result relevance scoring
- **Context Awareness**: Search results tailored to development contexts
- **Source Diversity**: Multiple source types (documentation, tutorials, examples)
- **Quality Ranking**: Prioritization based on authority and recency

## 🔗 Tool Integration Patterns

### Component Development Workflow
1. **Research Phase**: Use `web_search_exa` to find design patterns and best practices
2. **Discovery Phase**: Browse shadcn components for suitable base implementations
3. **Implementation Phase**: Retrieve component source code and customize
4. **Validation Phase**: Use `browser_navigate` and `browser_screenshot` to test
5. **Optimization Phase**: Monitor with `browser_network_requests` and `browser_console_messages`

### Visual Regression Testing
1. **Baseline Capture**: `browser_take_screenshot` for initial component state
2. **Modification Phase**: Apply changes using shadcn component patterns
3. **Comparison Testing**: Capture new screenshots for visual diff analysis
4. **Accessibility Validation**: Use `browser_snapshot` for WCAG compliance

### Performance Analysis Pipeline
1. **Initial Load Testing**: `browser_network_requests` to capture baseline metrics
2. **Component Optimization**: Research performance patterns with `web_search_exa`
3. **Implementation Updates**: Apply optimized shadcn component variants
4. **Validation Testing**: Monitor improvements with browser debugging tools

### Cross-Browser Compatibility
1. **Multi-Browser Testing**: Configure playwright for Chrome, Firefox, WebKit
2. **Component Adaptation**: Use shadcn multi-framework support for consistency
3. **Issue Research**: `deep_researcher_start` for browser-specific solutions
4. **Validation**: Screenshot comparison across browser environments

## ⚙️ Configuration Requirements

### API Keys Required
- **Exa API**: Register at dashboard.exa.ai for search capabilities
- **GitHub Token**: Optional for increased shadcn server request limits

### Environment Setup
- **Node.js**: Required for npm-based MCP servers
- **Browser Installation**: Playwright automatically installs browser binaries
- **Development Environment**: Compatible with modern web development workflows

### Performance Considerations
- **Caching**: Automatic caching for shadcn component data
- **Rate Limiting**: Built-in request throttling for external APIs
- **Resource Management**: Configurable browser resource usage
- **Network Optimization**: Intelligent batching of search requests

## 🎯 Use Case Templates

### Rapid Prototyping Template
```
1. web_search_exa: "modern button component patterns 2024"
2. shadcn component browsing: button variants and implementations
3. browser_navigate: load development environment
4. browser_screenshot: capture implementation results
5. browser_console_messages: validate for errors
```

### Performance Optimization Template
```
1. browser_network_requests: baseline performance measurement
2. web_search_exa: "React component performance best practices"
3. shadcn optimization patterns: efficient component implementations
4. browser_take_screenshot: visual validation post-optimization
5. deep_researcher_check: continuous performance monitoring
```

### Accessibility Compliance Template
```
1. browser_snapshot: accessibility DOM analysis
2. shadcn component variants: WCAG-compliant implementations
3. web_search_exa: "ARIA best practices for [component type]"
4. browser_take_screenshot: visual accessibility validation
5. browser_console_messages: accessibility error monitoring
```

This comprehensive tool reference enables efficient frontend development workflows through intelligent coordination of browser automation, component systems, and advanced research capabilities.