# Beagle - Claude Code Plugin

Code review skills and verification workflows for Python, Go, React, and AI frameworks. Designed to complement [superpowers](https://github.com/obra/superpowers) with pre-push reviews and GitHub bot feedback handling.

## Installation

Add the marketplace to `~/.claude/settings.json`:

```json
{
  "marketplaces": ["https://github.com/anderskev/beagle"]
}
```

Then restart Claude Code and run:

```
/plugin install beagle
```

For more on Claude Code plugins, see [Plugin documentation](https://docs.claude.com/en/docs/claude-code/plugins).

## Skills

Claude loads skills automatically when relevant. See [Agent Skills](https://docs.claude.com/en/docs/agents-and-tools/agent-skills/overview) for how skills work.

### Frontend

| Skill | Triggers |
|-------|----------|
| `react-flow` | Graph visualization, workflow nodes, custom edges |
| `react-router-v7` | Routing, loaders, actions, navigation |
| `tailwind-v4` | Styling, theming, dark mode |
| `shadcn-ui` | Component library, CVA variants |
| `zustand-state` | State management, middleware |
| `dagre-react-flow` | Auto-layout for graphs |

### Backend (Python)

| Skill | Triggers |
|-------|----------|
| `python-code-review` | Type hints, async patterns, error handling |
| `fastapi-code-review` | Endpoints, dependencies, validation |
| `sqlalchemy-code-review` | ORM patterns, relationships, queries |
| `postgres-code-review` | Postgres-specific patterns, JSONB, GIN |
| `pytest-code-review` | Test patterns, fixtures, mocking |

### Backend (Go)

| Skill | Triggers |
|-------|----------|
| `go-code-review` | Error handling, concurrency, interfaces |
| `bubbletea-code-review` | TUI patterns, Model/Update/View, Lipgloss |
| `wish-ssh-code-review` | SSH server, middleware, sessions |
| `prometheus-go-code-review` | Metrics, labels, instrumentation |
| `go-testing-code-review` | Table-driven tests, mocking, parallel tests |

### AI Frameworks

| Skill | Triggers |
|-------|----------|
| `pydantic-ai-*` | Agent creation, tools, dependency injection, testing |
| `langgraph-*` | Graph architecture, implementation patterns |
| `vercel-ai-sdk` | Streaming, use-chat, tools |

### Utilities

| Skill | Triggers |
|-------|----------|
| `vitest-testing` | Test configuration, mocking patterns |
| `docling` | Document parsing, chunking |
| `sqlite-vec` | Vector search, embeddings |
| `github-projects` | Project management via GraphQL |
| `ai-elements` | AI visualization components |
| `receive-feedback` | Processing code review feedback |
| `agent-architecture-analysis` | Analyzing agent system architecture |
| `12-factor-apps` | 12-Factor App compliance patterns |

## Commands

Run commands with `/beagle:<command>`. See [Slash commands](https://docs.claude.com/en/docs/claude-code/slash-commands) for how commands work.

### Code review

| Command | Description |
|---------|-------------|
| `/beagle:review-python` | Python/FastAPI code review with tech detection |
| `/beagle:review-frontend` | React/TypeScript code review with tech detection |
| `/beagle:review-go` | Go code review with BubbleTea/Wish/Prometheus detection |
| `/beagle:review-tui` | BubbleTea TUI code review with Elm architecture focus |
| `/beagle:review-plan <path>` | Review implementation plans before execution |

### Git workflows

| Command | Description |
|---------|-------------|
| `/beagle:commit-push` | Commit staged changes and push |
| `/beagle:create-pr` | Create PR with standardized template |
| `/beagle:gen-release-notes <tag>` | Generate release notes since tag |

### Other

| Command | Description |
|---------|-------------|
| `/beagle:skill-builder` | Create skills following best practices |
| `/beagle:12-factor-apps-analysis` | Analyze codebase for 12-Factor compliance |
| `/beagle:receive-feedback <path>` | Process code review feedback |
| `/beagle:fetch-pr-feedback` | Fetch bot review comments from PR |
| `/beagle:respond-pr-feedback` | Reply to bot review comments |

## Cursor IDE

Commands are also available for Cursor. Copy the `.cursor/commands/` folder to your project:

```bash
curl -L https://github.com/anderskev/beagle/archive/refs/heads/main.tar.gz | tar -xz --strip-components=1 beagle-main/.cursor
```

See [Cursor documentation](https://docs.cursor.com/) for command usage.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines on adding skills and commands.

## License

[MIT](LICENSE)
