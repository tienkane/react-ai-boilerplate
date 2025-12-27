# Agents

AI agent roles for delegating work in Claude Code.

## Workflow Diagram

```
┌─────────────────────────────────────────────────────────────┐
│                                                             │
│  ❓ Unclear Requirements ──► 📦 product ──► 📋 Clear Task  │
│                                                             │
│  📋 Task ──► 🧑‍💻 frontend-dev ──► 🔍 reviewer              │
│                      ▲                  │                   │
│                      │    ❌ Rejected   │                   │
│                      └──────────────────┘                   │
│                                         │ ✅ Approved       │
│                                         ▼                   │
│                                    🧪 qa ──► ✅ Done        │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

## Available Roles

| Role           | File                             | Purpose                                             |
| -------------- | -------------------------------- | --------------------------------------------------- |
| `frontend-dev` | `.claude/agents/frontend-dev.md` | Implement UI features following conventions         |
| `reviewer`     | `.claude/agents/reviewer.md`     | Strict code review: correctness, DX, perf, security |
| `qa`           | `.claude/agents/qa.md`           | Write tests, find edge cases, create test matrix    |
| `product`      | `.claude/agents/product.md`      | Clarify requirements, define acceptance criteria    |

## Usage

### Invoke an agent

```
@frontend-dev Implement a notification dropdown component.

@reviewer Review my changes to the auth flow.

@qa Create test cases for the payment form.

@product What should happen when a user tries to checkout with an empty cart?
```

### Chain agents for complex features

For any non-trivial feature, run agents in sequence:

1. **@product** (if requirements unclear) → Define acceptance criteria
2. **@frontend-dev** → Implement the feature
3. **@reviewer** → Code review pass
4. **@qa** → Test coverage check
5. **@frontend-dev** → Address feedback (if any)

## Rules

- For non-trivial features: **always** run reviewer + qa passes before finalizing.
- If reviewer finds blockers: address them before qa pass.
- If qa finds gaps: implement tests before marking done.
- If product clarification needed: get it before implementation.

## Agent Response Expectations

### frontend-dev

- Plan with 3-7 steps
- Minimal, focused implementation
- Self-review checklist completed
- Manual test steps included

### reviewer

- Categorized feedback (Blockers / Should Fix / Nice to Have)
- Specific line references
- Suggested fixes where applicable

### qa

- Test matrix (happy path + edge cases)
- Recommended unit/integration tests
- Manual test script (5-10 steps)

### product

- Clear acceptance criteria
- Edge case decisions
- UX expectations for each state
