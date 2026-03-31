# SCHAEZEL Skill Collection

A collection of [Claude Code](https://docs.anthropic.com/en/docs/claude-code/overview) skills.

## Available Skills

| Skill | Description |
|-------|-------------|
| [imitate](./imitate/) | Multi-perspective dialogue. Simulate conversations with top experts in any field. |

## Installation

### Claude Code

```bash
# Clone the repository
git clone https://github.com/SCHAEZEL/schaezel-skill.git ~/.claude/skills/schaezel-skill
```

Or manually copy individual skill directories to `~/.claude/skills/`.

### OpenClaw

```bash
npx clawhub@latest install SCHAEZEL/imitate
```

## Structure

```
schaezel-skill/
├── README.md           # This file
└── imitate/
    ├── SKILL.md       # Skill definition
    └── README.md       # Skill documentation
```

## License

MIT
