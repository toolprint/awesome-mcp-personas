# QA Engineer Docs

## Overview
The **QA Engineer Docs** persona automates testing workflows and generates structured test reports. It integrates **Playwright** for browser automation, **filesystem** operations for report generation, and **Fetch** for researching testing documentation and web content.

## Role & Responsibilities
- Automate and run browser-based tests using Playwright
- Generate structured test reports and documentation
- Fetch and research testing documentation and web resources
- Capture screenshots and evidence during test execution
- Create organized test report directories

## Toolsets

### 1. Browser Automation
- **Tools**: `playwright.navigate`, `playwright.screenshot`, `playwright.click`, `playwright.fill`, `playwright.evaluate`, `playwright.wait`
- **Purpose**: Automate browser interactions, navigate pages, capture screenshots, and validate UI behavior
- **Example**: Navigate to login page, fill credentials, click submit, verify successful login

### 2. Test Reporting
- **Tools**: `filesystem.read`, `filesystem.write`, `filesystem.create_directory`, `filesystem.list`
- **Purpose**: Generate and manage test reports, save screenshots, create structured documentation
- **Example**: Create test report directory, write HTML/Markdown reports, save screenshot evidence

### 3. Test Research
- **Tools**: `fetch.fetch`
- **Purpose**: Fetch web content and documentation for research purposes
- **Example**: Fetch testing documentation, download resources, get web content for analysis

## Installation

1. Ensure you have Node.js installed for running MCP servers
2. Place the persona files in the `personas/qa-engineer-docs` directory of your MCP-enabled agent
3. The filesystem server will create test reports in the `./test-reports` directory

## Configuration Files

- **mcp.json**: Contains the MCP server configurations for Playwright, filesystem, and fetch
- **persona.yaml**: Defines the toolsets and capabilities of this persona

## Usage

After installation, the persona can:
- Run automated browser tests with Playwright
- Generate test reports in HTML or Markdown format
- Organize test artifacts and screenshots
- Fetch testing documentation and web resources

## Example Workflow

1. Navigate to application under test
2. Perform user interactions (clicks, form fills)
3. Capture screenshots at key points
4. Generate test report with results
5. Save report and artifacts to filesystem

## Requirements

- Node.js 16+ for MCP servers
- Write access to `./test-reports` directory