# agent

Utility commands and skills for Claude Code.

## Installation

```shell
/plugin marketplace add christophercampbell/prompt-plugins
```

```shell
/plugin install agent@prompt-plugins
```

## Skills

**`agent:confidence-check`** - Pre-implementation confidence assessment (≥90% required).

Use before starting any implementation to verify:
- No duplicate implementations exist
- Architecture compliance verified
- Official documentation reviewed
- Working OSS implementations found
- Root cause properly identified

## Commands

**`/agent:skills`** - Lists all available skills in a table format.

**`/agent:prune`** - Audits and cleans up plugin installation.

Checks:
- Orphaned cache (in cache but not enabled)
- Old versions (multiple versions, only latest needed)
- Manifest drift (entries pointing to deleted paths)
- Empty plugins (cache exists but contains 0 files)

Locations audited:
| File | Purpose |
|------|---------|
| `~/.claude/settings.json` | Active plugins |
| `~/.claude/plugins/installed_plugins_v2.json` | Install metadata |
| `~/.claude/plugins/cache/` | Plugin files |
