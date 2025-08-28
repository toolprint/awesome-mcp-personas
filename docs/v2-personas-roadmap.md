# V2 Personas Roadmap

*Comprehensive roadmap for the next phase of persona development in the awesome-mcp-personas registry.*

## 📋 Overview

This document tracks the hypothesized personas for V2 development, organized by business function and implementation complexity. Each persona represents a specialized workflow combining multiple MCP servers for specific professional use cases.

**Total Personas Planned:** 16  
**MCP Servers Required:** 15 unique servers  
**Implementation Status:** Planning phase  

---

## 🏗️ Development & Engineering (5 personas)

### software-developer-assistant
- **Description:** Developer workflows for branching, committing, diffs, and quick alerts
- **Based on:** [frontend-developer.md](https://github.com/wshobson/agents/blob/main/frontend-developer.md)
- **MCP Servers:** `git`, `slack`
- **Complexity:** ⭐⭐ (Low-Medium)
- **Priority:** High - Core development workflow

**Toolsets:**
- `plan-build-communicate` → branch, commit, diff, post update in Slack
- `code-archaeology-knowledge-sharing` → browse logs, commits, diffs and share context
- `release-prep-team-nudges` → run sanity checks and nudge reviewers

### qa-engineer-assistant (slack variant)
- **Description:** QA automation using browser tests, containerized suites, Slack reporting
- **Based on:** [test-automator.md](https://github.com/wshobson/agents/blob/main/test-automator.md)
- **MCP Servers:** `playwright`, `docker`, `slack`
- **Complexity:** ⭐⭐⭐ (Medium)
- **Priority:** High - Quality assurance automation

**Toolsets:**
- `browser-regression-testing` → scripted UI flows with screenshots
- `containerized-test-execution` → run tests in containers, fetch logs
- `reporting-and-team-updates` → summarize results, post in Slack

### qa-engineer-docs-assistant (pdf variant)
- **Description:** Same QA flows but outputs structured PDF reports instead of chat
- **Based on:** [test-automator.md](https://github.com/wshobson/agents/blob/main/test-automator.md)
- **MCP Servers:** `playwright`, `docker`, `pdf`
- **Complexity:** ⭐⭐⭐ (Medium)
- **Priority:** Medium - Alternative QA reporting

**Toolsets:**
- `browser-regression-testing` → scripted UI flows with screenshots
- `containerized-test-execution` → run tests in containers, fetch logs
- `documentation-and-reports` → compile results/screenshots into PDF

### web-ui-engineer-assistant
- **Description:** Prototyping, scaffolding, and validating UI flows in browser (no Figma)
- **Based on:** [frontend-developer.md](https://github.com/wshobson/agents/blob/main/frontend-developer.md)
- **MCP Servers:** `playwright`, `shadcn`, `exa` (or `open-websearch`)
- **Complexity:** ⭐⭐⭐⭐ (Medium-High)
- **Priority:** High - Frontend development automation

**Toolsets:**
- `design-to-implementation` → search docs, fetch component, validate in browser
- `component-exploration-and-hardening` → list components, run interactions, validate
- `regression-testing-and-visual-snapshots` → capture before/after evidence
- `performance-and-best-practices-check` → measure timings, resource counts, search docs

### devops-engineer-assistant
- **Description:** Infra automation, safe rollouts, incident mitigation
- **Based on:** [devops-troubleshooter.md](https://github.com/wshobson/agents/blob/main/devops-troubleshooter.md)
- **MCP Servers:** `cloudflare`, `docker`, `git` (optional), `open-websearch`
- **Complexity:** ⭐⭐⭐⭐⭐ (High)
- **Priority:** High - Infrastructure automation

**Toolsets:**
- `env-provisioning-and-drift-checks` → spin up containers, manage configs
- `blue-green-or-canary-deploys` → rollouts, route flipping, health checks
- `incident-mitigation-playbooks` → search runbooks, tail logs, apply/revert fixes
- `secrets-and-config-hygiene` → audit configs and environment variables

---

## 📊 Management & Operations (6 personas)

### project-manager-assistant (linear)
- **Description:** Planning and triage of tasks in Linear
- **Based on:** [deployment-engineer.md](https://github.com/wshobson/agents/blob/main/deployment-engineer.md)
- **MCP Servers:** `linear`
- **Complexity:** ⭐⭐ (Low-Medium)
- **Priority:** High - Project management automation

**Toolsets:**
- `intake-triage-assignment` → create/classify issues, link to projects, assign owners
- `progress-queries-and-reports` → query issues/projects, summarize health
- `roadmap-and-team-operations` → review teams/projects, curate backlogs, comment

### project-manager-assistant (trello)
- **Description:** Backlog and board operations in Trello
- **Based on:** [devops-troubleshooter.md](https://github.com/wshobson/agents/blob/main/devops-troubleshooter.md)
- **MCP Servers:** `trello`
- **Complexity:** ⭐⭐ (Low-Medium)
- **Priority:** Medium - Alternative project management

**Toolsets:**
- `backlog-management` → list/add/update/move cards, assign members
- `board-operations-and-hygiene` → list/add/archive lists, keep board tidy
- `activity-digests` → fetch recent actions for standups or status

### observability-engineer-assistant
- **Description:** Triage errors, manage alerts, correlate releases, draft postmortems
- **Based on:** [performance-engineer.md](https://github.com/wshobson/agents/blob/main/performance-engineer.md)
- **MCP Servers:** `sentry`, `cloudflare`, `open-websearch`
- **Complexity:** ⭐⭐⭐⭐ (Medium-High)
- **Priority:** High - System reliability

**Toolsets:**
- `error-hotspot-triage` → top issues, grouped by release, suspect commits
- `alert-hygiene-and-thresholds` → tune thresholds and filters to reduce noise
- `release-regression-sweep` → correlate spikes to deploys, summarize impact
- `postmortem-starter-kit` → build timelines, metrics, root cause, actions

### sales-operations-assistant
- **Description:** CRM pipeline health, product ops, quotes
- **Based on:** [sales-automator.md](https://github.com/wshobson/agents/blob/main/sales-automator.md)
- **MCP Servers:** `salesforce`, `stripe`
- **Complexity:** ⭐⭐⭐ (Medium)
- **Priority:** Medium - Sales automation

**Toolsets:**
- `crm-hygiene-and-deduping` → find duplicates, normalize fields
- `pipeline-health-and-forecast` → aggregate opps, track risks
- `product-catalog-and-prices` → sync Stripe product/price updates
- `quote-to-cash-starter` → create test payment links, update CRM

### legal-ops-assistant
- **Description:** Manage policy docs, contracts, and audits
- **Based on:** [legal-advisor.md](https://github.com/wshobson/agents/blob/main/legal-advisor.md)
- **MCP Servers:** `atlassian-remote-mcp`, `pdf`, `open-websearch`
- **Complexity:** ⭐⭐⭐ (Medium)
- **Priority:** Medium - Legal operations

**Toolsets:**
- `policy-and-procedure-locator` → search Confluence and web
- `contract-playbook-refresh` → diff contract language, propose edits
- `audit-pack-builder` → collect docs, changelogs, approvals → PDF
- `matter-tracker` → open issues, assign reviewers, set due dates

### it-support-assistant
- **Description:** Handle employee IT issues, device setup, ticket routing
- **Based on:** [customer-support.md](https://github.com/wshobson/agents/blob/main/customer-support.md)
- **MCP Servers:** `cloudflare`, `open-websearch`, `atlassian-remote-mcp` (optional)
- **Complexity:** ⭐⭐ (Low-Medium)
- **Priority:** Medium - IT operations

**Toolsets:**
- `triage-and-routing` → search KB, propose solutions, open ticket
- `device-and-network-diagnostics` → gather device/net context, compare with policy
- `how-to-and-onboarding` → provide how-to guides for apps/devices
- `closure-and-follow-up` → summarize resolution, confirm user satisfaction

---

## 📈 Business & Analytics (3 personas)

### marketer-assistant
- **Description:** Market research, competitor analysis, and campaign briefs
- **Based on:** [content-marketer.md](https://github.com/wshobson/agents/blob/main/content-marketer.md)
- **MCP Servers:** `brave-search` or `open-websearch`, `reader/fetch`, `pdf`
- **Complexity:** ⭐⭐⭐ (Medium)
- **Priority:** High - Marketing automation

**Toolsets:**
- `market-landscape-scan` → search web/news, summarize trends
- `competitor-page-deepdives` → fetch competitor pages, extract claims
- `campaign-brief-writer` → ICP, goals, copy, export PDF
- `content-topic-mining` → cluster SERPs and FAQs into content ideas

### finance-analyst-assistant
- **Description:** FP&A reporting, KPI analysis, cohorts
- **Based on:** [business-analyst.md](https://github.com/wshobson/agents/blob/main/business-analyst.md)
- **MCP Servers:** `postgres`, `tinybird`, `pdf`
- **Complexity:** ⭐⭐⭐⭐ (Medium-High)
- **Priority:** High - Financial analysis

**Toolsets:**
- `kpi-digest-and-trends` → SQL queries, MoM/YoY deltas, export PDF
- `revenue-and-cohort-cuts` → analyze ARPA, LTV, cohorts
- `expense-variance-analysis` → compare actuals vs plan
- `cash-and-burn-runway` → track cash and burn trends

### data-analyst-assistant
- **Description:** Ad-hoc SQL queries, metric explanations, doc grounding
- **Based on:** [data-scientist.md](https://github.com/wshobson/agents/blob/main/data-scientist.md)
- **MCP Servers:** `postgres`, `qdrant`, `open-websearch`
- **Complexity:** ⭐⭐⭐⭐ (Medium-High)
- **Priority:** High - Data analysis automation

**Toolsets:**
- `ad-hoc-sql-explorer` → generate/execute SQL, explain joins
- `metric-explanations` → correlate KPI spikes to events
- `deck-and-spec-grounding` → fetch vectorized doc snippets
- `report-packaging` → assemble findings into briefs

---

## 🎨 Design & Creative (2 personas)

### web-designer-assistant
- **Description:** Support design → dev handoff with assets and moodboards
- **Based on:** [ui-ux-designer.md](https://github.com/wshobson/agents/blob/main/ui-ux-designer.md)
- **MCP Servers:** `figma`, `open-websearch`, `pdf`
- **Complexity:** ⭐⭐⭐ (Medium)
- **Priority:** Medium - Design workflow automation

**Toolsets:**
- `design-asset-curation` → list frames, export assets and tokens
- `pattern-research-and-moodboards` → collect references and a11y notes
- `review-packet-builder` → bundle comps, usage notes, constraints → PDF
- `handoff-checklist` → validate naming, tokens, spacing rules

---

## 🛠️ MCP Server Requirements

### Required Servers (15 total)

**Core Infrastructure:**
- `git` - Version control operations
- `docker` - Container management
- `postgres` - Database operations  
- `pdf` - Document generation

**Communication & Collaboration:**
- `slack` - Team communication
- `figma` - Design assets
- `atlassian-remote-mcp` - Confluence/Jira

**Testing & Monitoring:**
- `playwright` - Browser automation
- `sentry` - Error monitoring
- `cloudflare` - Infrastructure monitoring

**Business & Analytics:**
- `linear` - Project management
- `trello` - Board management
- `salesforce` - CRM operations
- `stripe` - Payment processing
- `tinybird` - Analytics

**Search & Research:**
- `open-websearch` / `brave-search` - Web search
- `reader/fetch` - Content extraction
- `exa` - Advanced search
- `qdrant` - Vector search
- `shadcn` - UI components

### Server Dependency Matrix

| Persona Category | Required Servers | Optional Servers |
|------------------|------------------|------------------|
| Development | git, docker, playwright | slack, open-websearch |
| Management | linear/trello, slack | atlassian-remote-mcp |
| Analytics | postgres, pdf | tinybird, qdrant |
| Design | figma, pdf | open-websearch |
| Operations | cloudflare, sentry | open-websearch |

---

## 🎯 Implementation Roadmap

### Phase 2A: Core Development (Q1)
**Priority: High** | **Complexity: Low-Medium**
1. `software-developer-assistant` 
2. `project-manager-assistant` (linear)
3. `qa-engineer-assistant` (slack variant)

### Phase 2B: Advanced Automation (Q2)  
**Priority: High** | **Complexity: Medium-High**
1. `web-ui-engineer-assistant` ✅ **COMPLETED**
2. `devops-engineer-assistant`
3. `observability-engineer-assistant`

### Phase 2C: Business Operations (Q3)
**Priority: Medium-High** | **Complexity: Medium**
1. `marketer-assistant`
2. `finance-analyst-assistant`  
3. `data-analyst-assistant`

### Phase 2D: Extended Workflows (Q4)
**Priority: Medium** | **Complexity: Low-Medium**
1. `sales-operations-assistant`
2. `legal-ops-assistant`
3. `it-support-assistant`
4. `web-designer-assistant`

### Phase 2E: Alternative Variants (Future)
**Priority: Low** | **Complexity: Medium**
1. `qa-engineer-docs-assistant` (pdf variant)
2. `project-manager-assistant` (trello variant)

---

## 📊 Success Metrics

### Development KPIs
- **Persona Coverage:** 16 specialized business workflows
- **Server Integration:** 15+ MCP servers successfully integrated
- **Complexity Distribution:** 30% Low, 50% Medium, 20% High
- **Business Function Coverage:** 5 major categories

### Quality Standards  
- **Schema Compliance:** 100% validation against persona schemas
- **Security Audit:** All credentials properly parameterized
- **Documentation:** Complete README, tools.md, examples for each persona
- **Cross-Platform:** All personas tested on multiple environments

### User Experience Goals
- **Workflow Efficiency:** 40%+ reduction in manual task time
- **Integration Quality:** Seamless multi-server coordination  
- **Documentation Quality:** Clear setup and usage instructions
- **Community Adoption:** Public registry with contribution guidelines

---

## 🔄 Continuous Evolution

### Feedback Integration
- **User Testing:** Beta testing with target professional roles
- **Community Input:** Public feedback on workflow effectiveness
- **Performance Monitoring:** Server response times and reliability
- **Feature Requests:** Enhancement requests from persona users

### Technical Debt Management
- **Regular Audits:** Quarterly reviews of all persona configurations
- **Security Updates:** Proactive security scanning and updates
- **Dependency Management:** Monitor MCP server updates and compatibility
- **Performance Optimization:** Regular analysis of tool coordination efficiency

This roadmap provides a comprehensive foundation for expanding the awesome-mcp-personas registry with specialized, professional-grade workflow automation personas.