# React AI Boilerplate (Cursor + Claude Code)

A **personal React AI boilerplate** to control how AI works in your codebase.

This repo is not about React setup.
It is about **disciplining AI** so it behaves like a senior frontend engineer:

- minimal diffs
- clear scope
- correct TypeScript
- PR-ready output

Designed for:

- Personal React projects
- Cursor
- Claude Code

---

## Why this exists

Without rules, AI tends to:

- refactor unrelated files
- introduce new libraries
- over-engineer simple features
- ignore existing patterns
- output code that “looks right” but is risky

This boilerplate defines **how AI is allowed to work**, not how your app is built.

---

## What this boilerplate controls

✅ AI behavior  
✅ Scope boundaries  
✅ TypeScript discipline  
✅ React architecture expectations  
✅ Output quality (reviewable, explainable)

❌ It does NOT define:

- framework choice (Vite / Next / etc.)
- UI library
- state management
- folder structure
- build tooling

Those belong to the project, not the AI.

---

## Supported tools

### Cursor

Uses:

- `.cursor/rules/*.mdc`

Purpose:

- constrain scope
- prevent drive-by refactors
- keep diffs small
- enforce PR-quality answers

### Claude Code

Uses:

- `CLAUDE.md`
- `.claude/agents/*`

Purpose:

- give Claude repo context
- define working rules
- enable role-based reasoning (dev / reviewer / qa / product)

Cursor and Claude are intentionally aligned so they **do not fight each other**.

---

## Repository structure

```txt
.
├─ README.md
├─ AGENTS.md
├─ CLAUDE.md
├─ .cursorignore
├─ .cursor/
│  └─ rules/
│     ├─ 00-repo-context.mdc
│     ├─ 10-react-ui.mdc
│     ├─ 20-typescript.mdc
│     ├─ 30-testing.mdc
│     └─ 40-security-performance.mdc
└─ .claude/
   └─ agents/
      ├─ frontend-dev.md
      ├─ reviewer.md
      └─ qa.md
```
