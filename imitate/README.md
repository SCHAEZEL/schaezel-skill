# Imitate

Multi-perspective dialogue. Simulate conversations with top experts in any field.

## Features

- **Manual Mode**: Specify two people to simulate a dialogue
- **Search Mode**: Specify a domain and let AI find top experts automatically
- **Three-way Output**: Two expert perspectives + Claude's plain-language summary

## Usage

```
/imitate 马斯克 库克 你认为小米汽车怎么样？
/imitate 投资 A股现在适合入场吗？
```

## Installation

### Claude Code

Copy `SKILL.md` to `~/.claude/skills/imitate/SKILL.md`.

### OpenClaw

```bash
npx clawhub@latest install SCHAEZEL/imitate
```

## How It Works

1. Parse user input to extract person names or domain
2. Search for top experts in that domain (search mode only)
3. Launch two agents in parallel, each playing one expert
4. Aggregate responses with Claude's summary

## License

MIT
