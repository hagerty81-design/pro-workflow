---
name: workflow
description: "Print the pro workflow quick-reference card. Use when user types /workflow or asks about commands, shortcuts, or how to use Claude Code effectively."
user-invocable: true
disable-model-invocation: true
---

When the user invokes /workflow, print the following reference card exactly. Do not add commentary or explanation beyond what is listed. Do not include any commands that are not listed here -- these are all verified and real.

# Pro Workflow Quick Reference

## Before You Code
| Action | How | When |
|--------|-----|------|
| Start a new project | `/init` | First time opening any project -- creates CLAUDE.md |
| Enter Plan Mode | `Shift+Tab` until you see the pause icon, or `/plan` | Before any change that touches 3+ files |
| Point to specific files | `@src/components/Header.tsx` | Every prompt -- cheaper and more precise than pasting |
| Open full editor for prompt | `Ctrl+G` | When your prompt is longer than 2-3 lines |
| Set thinking depth | `Option+T` / `Alt+T` | Toggle extended thinking for complex architecture decisions |

## While You Code
| Action | How | When |
|--------|-----|------|
| Run a command and show output | `!npm run build` | Whenever you want Claude to see terminal output |
| Ask a side question | `/btw what does cn() do?` | Quick clarification without polluting main context |
| Compress conversation | `/compact` | When the chat feels slow or you're 40+ messages deep |
| Full reset | `/clear` | When switching to a completely unrelated task |
| Pick a model | `Option+P` / `Alt+P` | Switch between Opus, Sonnet, Haiku mid-session |

## When Things Break
| Action | How | When |
|--------|-----|------|
| Undo everything | `Esc` + `Esc` or `/rewind` | Claude made a mistake -- rolls back code, conversation, or both |
| Review what changed | `Shift+Tab` to Plan Mode | Look at the plan before approving execution |

## The Gold Loop
```
Plan (Shift+Tab) -> Describe with @files -> Review plan -> Execute -> Verify (!npm test) -> Rewind if wrong
```
