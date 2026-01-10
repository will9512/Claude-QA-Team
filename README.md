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

### Orchestration Layer
- **QA Orchestrator**: Analyzes QA scope and creates execution plans, selecting appropriate sub-agents based on project type
- **QA Team Lead**: Coordinates delegation and consolidates QA work across specialists
- **Documentation Lead**: Maintains QA records, findings, and remediation tracking

### Specialist Sub-agents

| Category | Agents | Purpose |
|----------|--------|---------|
| **General QA** | general-qa, modular-code, framework-best-practices | Code quality, structure, and framework conventions |
| **Cleanup** | code-remover, comments-cleanup, diagnostic-file-remover | Dead code, comment quality, debug artifact removal |
| **Documentation** | docs-qa, emojis-and-style | Documentation completeness and style consistency |
| **Organisation** | code-non-code | File organization and separation |
| **Performance** | image-optimization, image-compression-cdn | Asset optimization and CDN configuration |
| **API** | backend-api-review, frontend-backend-alignment, mcp-server-validation | API quality and contract consistency |
| **Other** | basic-seo, responsive-style, deployment-reviewer | SEO, responsive design, deployment configuration |

## Usage Scenarios

**Web Application Review**:
- General QA, Modular Code, Framework Best Practices
- Responsive Style, Basic SEO
- Image Optimization
- Deployment Reviewer

**API Project Review**:
- General QA, Modular Code
- Backend API Review, Frontend-Backend Alignment
- Code Remover, Comments Cleanup

**Documentation-focused Review**:
- Docs QA, Emojis and Style
- Code/Non-code organization

**Pre-deployment Cleanup**:
- Diagnostic File Remover, Code Remover
- Comments Cleanup
- Deployment Reviewer

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
