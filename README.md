# Copilot CLI Custom Agents

A collection of custom agents for [GitHub Copilot CLI](https://docs.github.com/copilot/concepts/agents/about-copilot-cli).

## Agents

| Agent | Purpose |
|-------|---------|
| `api-architect` | Design REST/GraphQL APIs and OpenAPI specifications |
| `bug-investigator` | Debug errors, analyze stack traces, find root causes |
| `clean-code-enforcer` | Validate SOLID/DRY/KISS principles and coding standards |
| `cloud-deployment-automator` | Deploy apps to AWS/Azure/GCP, set up CI/CD pipelines |
| `code-documenter` | Generate README files, API docs, and inline comments |
| `db-system-architect` | Design database schemas and system architecture |
| `engineering-code-reviewer` | Expert code review focused on correctness and maintainability |
| `engineering-mobile-app-builder` | Build native iOS/Android and cross-platform mobile apps |
| `observability-architect` | Set up logging, metrics, and distributed tracing |
| `performance-optimizer` | Profile code, find bottlenecks, reduce memory usage |
| `qa-test-engineer` | Write unit, integration, and E2E test suites |
| `security-auditor` | Audit for OWASP vulnerabilities and security issues |
| `senior-web-dev` | Build and refactor full-stack web applications |
| `spring-boot-developer` | Build and debug Spring Boot backend applications |
| `ui-accessibility-improver` | Review UI/UX, WCAG compliance, and responsive design |

## Installation

Copy the agent files to your Copilot CLI agents directory:

### macOS / Linux
```bash
cp *.agent.md *.md ~/.copilot/agents/
```

### Windows (PowerShell)
```powershell
Copy-Item *.agent.md, *.md $HOME\.copilot\agents\
```

> **Note:** Create the directory first if it doesn't exist:
> ```powershell
> New-Item -ItemType Directory -Force $HOME\.copilot\agents
> ```

## Usage

Once the agent files are in place, Copilot CLI will automatically pick them up. You can:

- Use the `/agent` slash command inside the CLI to browse and select an agent
- Mention an agent by name in your prompt and Copilot will route to it automatically

## File Format

Each agent is defined as a Markdown file with a YAML frontmatter block:

```markdown
---
name: my-agent
description: "When to use this agent and trigger phrases..."
---

Agent system prompt / instructions go here.
```

Files must use the `.agent.md` extension (or `.md` for legacy format) and be placed in `~/.copilot/agents/`.
