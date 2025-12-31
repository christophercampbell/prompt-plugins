# Prompt Plugins

A collection of plugins for Claude Code.

## Plugins

### coder

Pragmatic engineering principles: YAGNI, SOLID, KISS, DRY, fail fast, and more.

**Skill:** `coder:development-principles`
- Invoke when designing, implementing, or reviewing code
- Covers: YAGNI, Composability, SOLID, DRY, KISS, Separation of Concerns, Fail Fast, Error Handling, Testing, Performance, Security, Code Review, Refactoring, Problem-Solving, Communication Style, PR Authoring

**Command:** `/coder:review`
- Reviews recent code changes against the principles
- Reports findings with file paths and line numbers

### agent

Utility commands and skills for Claude Code itself.

**Skill:** `agent:confidence-check`
- Pre-implementation confidence assessment (≥90% required)
- Verifies: no duplicates, architecture compliance, official docs, OSS references, root cause

**Command:** `/agent:skills`
- Lists all available skills in a table format

**Command:** `/agent:prune`
- Audits and cleans up plugin installation
- Identifies orphaned caches, old versions, manifest drift

## Installation

Add the marketplace, then install plugins:

```shell
/plugin marketplace add christophercampbell/prompt-plugins
```

```shell
/plugin install coder@prompt-plugins
```

```shell
/plugin install agent@prompt-plugins
```

Or use `/plugin` to browse and install interactively.

## License

MIT
