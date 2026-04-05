# Pro Workflow Plugin for Claude Code

Expert-level Claude Code setup in one install. Built for beginners and pros alike.

## What You Get

- **Auto-format**: Every file Claude edits gets formatted automatically (Prettier)
- **Security gates**: Dangerous commands (rm -rf, dropping tables) are blocked before they run
- **Secret protection**: Prevents accidentally staging .env, .pem, .key files
- **Plan Mode guidance**: Claude suggests planning before large changes
- **Guided onboarding**: /setup walks you through everything step by step
- **Quick reference**: /workflow shows your command cheat sheet anytime

## Install

1. Open your project folder in terminal
2. Start Claude Code:
   ```
   claude
   ```
3. Install the plugin:
   ```
   /plugin install github.com/chrisotoole/pro-workflow
   ```
4. Run the guided setup:
   ```
   /setup react
   ```
   (Replace `react` with your stack: `python`, `next`, `vue`, `go`, etc. Or just type `/setup` and it will auto-detect.)

5. Start building:
   ```
   Help me build [describe what you want]
   ```

## Commands

| Command | What it does |
|---------|-------------|
| `/setup` | Guided first-time setup (creates CLAUDE.md, tests hooks) |
| `/workflow` | Quick-reference card of all essential commands |
| `/plan` | Enter Plan Mode -- Claude shows its blueprint before coding |
| `/rewind` | Undo Claude's changes (or press Esc twice) |
| `/compact` | Compress conversation to save tokens and speed up |
| `/btw [question]` | Ask a side question without polluting context |

## For Teams

Everyone on your team installs the same plugin and gets identical:
- Auto-format hooks (no more style arguments)
- Security gates (no accidental destructive commands)
- Workflow habits (Plan Mode for big changes)

```
# Share this one command with your team:
/plugin install github.com/chrisotoole/pro-workflow
```

## Developing This Plugin

To test changes locally:
```
claude --plugin-dir /path/to/pro-workflow
```

To reload after making changes (inside a Claude session):
```
/reload-plugins
```

## Structure

```
pro-workflow/
  .claude-plugin/
    plugin.json          # Plugin metadata
  skills/
    workflow-guide/
      SKILL.md           # /workflow command
    plan-first/
      SKILL.md           # Auto-suggests Plan Mode for big tasks
    onboarding/
      SKILL.md           # /setup guided onboarding
  hooks/
    hooks.json           # Auto-format, security gate, secret detection
  CLAUDE.md              # Template (customized by /setup)
  README.md              # This file
```

## License

MIT
