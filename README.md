[![Claude Code View Marketplace](https://img.shields.io/badge/Claude%20Code-View%20Marketplace-blue?style=for-the-badge&logo=github)](https://github.com/danielrosehill/Claude-Code-Plugins)
[![Claude Code Repos Index](https://img.shields.io/badge/Claude%20Code-Repos%20Index-purple?style=for-the-badge&logo=github)](https://github.com/danielrosehill/Claude-Code-Repos-Index)

## QA Team Plugin

A multi-agent quality assurance system for comprehensive code review and validation. This plugin provides an orchestrated network of specialized AI agents that collaborate to perform thorough QA reviews on codebases.

**To install the marketplace:**

```bash
/plugin marketplace add https://github.com/danielrosehill/Claude-Code-Plugins
```

**Plugin Installation:**

```bash
/plugin install qa-team@danielrosehill
```

---

## Features

### Orchestration Layer (Slash Commands)

| Command | Purpose |
|---------|---------|
| `/qa-team:qa-orchestrator` | Analyzes QA scope and creates execution plans, selecting appropriate agents |
| `/qa-team:qa-team-lead` | Coordinates delegation and consolidates QA work across specialists |
| `/qa-team:documentation-lead` | Maintains QA records, findings, and remediation tracking |

### Specialist Agents

#### General QA
| Agent | Purpose |
|-------|---------|
| `general-qa` | Overall code quality assessment |
| `modular-code` | Code modularity, componentization, and duplicate pattern detection |
| `framework-best-practices` | Framework-specific conventions and patterns |

#### Cleanup
| Agent | Purpose |
|-------|---------|
| `code-remover` | Dead/unused code identification |
| `comments-cleanup` | Comment quality and relevance |
| `diagnostic-file-remover` | Debug/test artifact cleanup |

#### Documentation
| Agent | Purpose |
|-------|---------|
| `docs-qa` | Documentation completeness and accuracy |
| `emojis-and-style` | Style consistency in documentation |

#### Organisation
| Agent | Purpose |
|-------|---------|
| `code-non-code` | File organization and separation |

#### Performance
| Agent | Purpose |
|-------|---------|
| `image-optimization` | Image asset optimization |
| `image-compression-cdn` | Compression and CDN setup |
| `caching-optimization` | API response caching, redundant request reduction |
| `resource-efficiency` | CPU, memory, and I/O optimization |
| `cost-efficiency` | Cloud API cost reduction, local compute alternatives |

#### Backend - API
| Agent | Purpose |
|-------|---------|
| `backend-api-review` | API endpoint quality |
| `frontend-backend-alignment` | API contract consistency |

#### Backend - MCP
| Agent | Purpose |
|-------|---------|
| `mcp-server-validation` | MCP server compliance |

#### Backend - Database
| Agent | Purpose |
|-------|---------|
| `database-reviewer` | Database indexes, query optimization, N+1 detection |

#### UX
| Agent | Purpose |
|-------|---------|
| `edge-case-identifier` | Boundary conditions, blind spots, unhandled scenarios |
| `ux-friction` | Cumbersome interactions, annoying patterns, friction points |
| `user-feedback-messages` | Success/error toasts, loading states, user notifications |
| `navigation-breadcrumbs` | Navigation structure, breadcrumbs, user orientation (recommendations only) |

#### Other
| Agent | Purpose |
|-------|---------|
| `basic-seo` | SEO fundamentals |
| `responsive-style` | Responsive design review |
| `deployment-reviewer` | Deployment configuration |

## Usage Scenarios

**Web Application Review**:
- General QA, Modular Code, Framework Best Practices
- Responsive Style, Basic SEO
- Image Optimization, Caching Optimization
- UX Friction, Navigation & Breadcrumbs
- Deployment Reviewer

**API Project Review**:
- General QA, Modular Code
- Backend API Review, Frontend-Backend Alignment
- Database Reviewer, Caching Optimization
- Code Remover, Comments Cleanup

**Performance Audit**:
- Database Reviewer, Caching Optimization
- Resource Efficiency, Cost Efficiency
- Image Optimization, Image Compression/CDN

**UX Review**:
- Edge Case Identifier, UX Friction
- User Feedback Messages, Navigation & Breadcrumbs
- Responsive Style

**Documentation-focused Review**:
- Docs QA, Emojis and Style
- Code/Non-code organization

**Pre-deployment Cleanup**:
- Diagnostic File Remover, Code Remover
- Comments Cleanup
- Deployment Reviewer

## Directory Structure

```
.claude-plugin/
└── plugin.json         # Plugin manifest

commands/               # Slash commands (user-invoked)
├── qa-orchestrator.md
├── qa-team-lead.md
└── documentation-lead.md

agents/                 # Specialist agents (Claude-invoked)
├── general/
├── cleanup/
├── documentation/
├── organisation/
├── performance/
├── backend/
│   ├── api/
│   ├── mcp/
│   └── db/
├── ux/
└── other/

from_agent/QA/          # Output directory
├── reviews/
├── findings/
├── remediation/
└── logs/
```

## Output Structure

QA findings are organized in `from_agent/QA/`:
- `reviews/` - Completed QA review reports
- `findings/` - Issues discovered, categorized by severity
- `remediation/` - Items flagged for future work
- `logs/` - Process activity logs

## Author

**Daniel Rosehill**
- Website: [danielrosehill.com](https://danielrosehill.com)
- Email: public@danielrosehill.com
- GitHub: [@danielrosehill](https://github.com/danielrosehill)

## License

This plugin is licensed under the MIT License.

---

For more Claude Code projects, visit my [Claude Code Repos Index](https://github.com/danielrosehill/Claude-Code-Repos-Index).
