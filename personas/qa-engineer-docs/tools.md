# QA Engineer Docs - Tools Reference

## Overview
The qa-engineer-docs persona provides tools for browser automation testing, test report generation, and documentation research.

## Tools by Server

### Playwright Server
Browser automation and testing capabilities.

| Tool | Description | Example Usage |
|------|-------------|---------------|
| `playwright.navigate` | Navigate to a specified URL | Navigate to login page |
| `playwright.screenshot` | Capture screenshots of pages | Take screenshot for evidence |
| `playwright.click` | Click on elements using selectors | Click login button |
| `playwright.fill` | Fill form fields with specified values | Enter username and password |
| `playwright.evaluate` | Execute JavaScript in browser context | Check page state or extract data |
| `playwright.wait` | Wait for elements or conditions | Wait for page to load |

### Filesystem Server
File operations for test report management.

| Tool | Description | Example Usage |
|------|-------------|---------------|
| `filesystem.read` | Read file contents | Load test configuration |
| `filesystem.write` | Write content to files | Save test results to report |
| `filesystem.create_directory` | Create new directories | Create test report directory |
| `filesystem.list` | List directory contents | Browse test artifacts |

### Fetch Server  
Web content retrieval for documentation research.

| Tool | Description | Example Usage |
|------|-------------|---------------|
| `fetch.fetch` | Fetch web content from URLs | Download testing documentation |

## Toolset Workflows

### Browser Automation
Typical testing workflow using Playwright tools:

1. `playwright.navigate` → Open application URL
2. `playwright.fill` → Enter test data into forms  
3. `playwright.click` → Trigger actions (submit, navigate)
4. `playwright.screenshot` → Capture results for comparison
5. `playwright.evaluate` → Verify expected page state

### Test Reporting
Generate structured test reports:

1. `filesystem.create_directory` → Create report directory
2. `playwright.screenshot` → Capture test evidence
3. `filesystem.write` → Generate HTML/Markdown reports
4. `filesystem.list` → Organize test artifacts

### Test Research
Research testing documentation and resources:

1. `fetch.fetch` → Download testing guides
2. `filesystem.write` → Save documentation locally
3. `filesystem.read` → Review cached resources

## Common Tool Combinations

**E2E Test Execution**:
→ `playwright.navigate` + `playwright.fill` + `playwright.click`

**Evidence Capture**: 
→ `playwright.screenshot` + `filesystem.write`

**Report Generation**:
`playwright.navigate` → `playwright.screenshot` → `playwright.evaluate`

## Best Practices

- Use `playwright.wait` to ensure elements are ready before interaction
- Capture screenshots at key test points for debugging
- Organize test artifacts in structured directories
- Use descriptive filenames for test reports and screenshots