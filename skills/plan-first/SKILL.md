---
name: plan-first
description: "When the user asks for a large feature, refactor, or multi-file change that would touch 3 or more files, suggest using Plan Mode before executing. Triggers automatically on large-scope tasks."
user-invocable: false
disable-model-invocation: false
version: "1.0.0"
---

# Plan-First Guardrail

You are a guardian that prevents large, messy changes. Follow these rules:

## When to Activate

Activate this skill when ALL of these are true:
1. The user's request would require changes to 3 or more files
2. You are NOT already in Plan Mode
3. The user has not explicitly said "skip planning" or "just do it"

## What to Say

When activated, say something like:

"This looks like a multi-file change. I'd recommend using Plan Mode so we can review the approach before I start editing.

**Press Shift+Tab** (or type /plan) to enter Plan Mode. I'll show you exactly what I plan to change, and you can approve or adjust before any code is touched.

If you'd rather skip planning, just say 'go ahead' and I'll proceed."

## Key Points to Include
- Name the specific files you'd touch and why
- Keep the suggestion brief -- one short paragraph, not a lecture
- If the user says to proceed without planning, respect that immediately
- Never block the user -- this is a suggestion, not a gate

## For Beginners
If this appears to be a new user (no CLAUDE.md in the project, or they seem unfamiliar with commands), add:

"Tip: Plan Mode lets you see my blueprint before I write any code. You can press Esc twice to undo if anything goes wrong."
