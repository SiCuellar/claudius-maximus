# Claudius Maximus

A collection of custom commands for [Claude Code](https://github.com/anthropics/claude-code).

## Prerequisites

- [Claude Code](https://github.com/anthropics/claude-code) installed and configured

## Installation

### 1. Create the Claude commands directory

If you haven't used custom commands before, create the required folder:

```bash
mkdir -p ~/.claude/commands
```

### 2. Install the commands

Clone this repo:

```bash
git clone https://github.com/SiCuellar/claudius-maximus.git
```

Then copy the commands to your preferred location:

**Global (available in all projects):**
```bash
cp claudius-maximus/commands/*.md ~/.claude/commands/
```

**Local (project-specific):**
```bash
mkdir -p .claude/commands
cp claudius-maximus/commands/*.md .claude/commands/
```

### 3. Verify installation

Open Claude Code and type `/` to see your available commands. You should see `/create-prompt` and `/run-prompt` in the list.

## Available Commands

### `/create-prompt`

An expert prompt engineer that creates optimized, XML-structured prompts. It will:

- Ask clarifying questions about your task
- Determine complexity and execution strategy
- Generate well-structured prompts saved to `./prompts/`
- Offer to run the prompt immediately

**Usage:**
```
/create-prompt build a user authentication system
```

### `/run-prompt`

Executes prompts from your `./prompts/` folder as delegated sub-tasks. Supports:

- Single prompt execution
- Parallel execution (independent tasks)
- Sequential execution (dependent tasks)

**Usage:**
```
/run-prompt 001                      # Run prompt 001
/run-prompt                          # Run most recent prompt
/run-prompt 005 006 007 --parallel   # Run multiple in parallel
/run-prompt 005 006 007 --sequential # Run multiple sequentially
```

---

![Are you not entertained?](https://media0.giphy.com/media/v1.Y2lkPTc5MGI3NjExcXk4OGV6ZnZ1OG11bmt1NnNhdHQ0bWU2czBnOThydDExYWkwbHI1OCZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/d7mMzaGDYkz4ZBziP6/giphy.gif)

## License

MIT
