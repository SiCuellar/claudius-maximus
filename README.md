# Claudius Maximus

A collection of custom commands for [Claude Code](https://github.com/anthropics/claude-code).

## Installation

Symlink the commands you want to your Claude commands directory:

```bash
ln -s /path/to/claudius-maximus/commands/my-command ~/.claude/commands/my-command
```

Or copy the entire commands folder:

```bash
cp -r commands/* ~/.claude/commands/
```

## Adding Commands

Each command lives in its own folder under `commands/`:

```
commands/
└── my-command/
    └── skill.md
```

The `skill.md` file defines the command name and prompt.

## License

MIT
