# Cleanup Recommendations

Personal coding setup — things to keep vs remove.

## Remove

### Install tooling (already set up, no longer needed)
- `install.sh`, `install.ps1`
- `package.json`, `package-lock.json`
- `manifests/` — only used by the selective install pipeline
- `schemas/` — JSON schemas for the install pipeline

### Docs (contributor-facing, not useful for daily coding)
- `docs/ANTIGRAVITY-GUIDE.md` — unless you use Antigravity IDE

### Misc
- `assets/` — images used only in README
- `plugins/` — plugin marketplace registry
- `.claude-plugin/` — plugin publishing metadata
- `tests/` — test suite for the install scripts
- `README.md` — GitHub-facing, not useful locally

---

## Keep

| Path | Why |
|------|-----|
| `agents/` | Subagents you delegate work to |
| `skills/` | Reusable workflow knowledge loaded by commands |
| `commands/` | Slash commands (`/tdd`, `/plan`, `/code-review`, etc.) |
| `hooks/` | Trigger-based automations (session persistence, etc.) |
| `rules/` | Always-on guidelines loaded into every session |
| `mcp-configs/` | MCP server configurations |
| `scripts/hooks/` | Scripts called at runtime by hooks — required |
| `.claude/` | Project-level Claude Code config for this repo itself |
| `CLAUDE.md` | Auto-loaded by Claude Code — core instructions |
| `AGENTS.md` | Auto-loaded agent guidance |
| `contexts/dev.md`, `contexts/research.md`, `contexts/review.md` | Useful mode-switching prompts |
| `examples/` | CLAUDE.md templates to copy when setting up new projects |
| `docs/COMMAND-AGENT-MAP.md` | Quick reference: which commands use which agents |
| `docs/token-optimization.md` | Practical tips to reduce token usage |
| `docs/SKILL-PLACEMENT-POLICY.md` | Useful if you add custom skills |
| `the-shortform-guide.md` | Worth reading — covers setup philosophy |
| `the-longform-guide.md` | Deep dive: token optimization, memory, evals, parallelization |
| `the-security-guide.md` | Agentic security reference |
