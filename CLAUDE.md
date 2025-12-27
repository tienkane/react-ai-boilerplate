# Project: <YOUR_PROJECT_NAME>

## One-liner

A personal React app for <purpose>.

## Tech stack

- React: <Vite | Next.js | Remix | ...>
- Language: TypeScript
- Styling: <Tailwind | CSS Modules | styled-components | ...>
- State: <React Query | Zustand | Redux | ...>
- Forms: <react-hook-form | ...>
- Testing: <Vitest/Jest + Testing Library>, optional: Playwright/Cypress
- Package manager: <pnpm | npm | yarn>
- Lint/format: <eslint + prettier | biome>

## Non-goals (important)

- Do NOT introduce new heavy frameworks unless requested.
- Do NOT rewrite architecture for small tasks.
- Do NOT change styling system (e.g. Tailwind -> something else) unless requested.
- Do NOT add backend unless task explicitly requires it.

## Repo conventions

- Prefer small, focused PRs.
- Prefer composable components; avoid “god components”.
- Prefer pure functions + hooks; keep side effects isolated.
- File naming:
  - Components: PascalCase.tsx
  - Hooks: useXxx.ts
  - Utils: camelCase.ts
- Always keep types close to usage unless shared widely.

## Workflow (must follow)

1. **Explore first**:
   - Identify entry points, routing, state layer, API layer.
   - Confirm existing patterns before adding new ones.
2. **Plan** (short):
   - List steps (3–7 bullets), call out risks.
3. **Implement**:
   - Keep diffs minimal and consistent with existing style.
4. **Self-review checklist**:
   - Types correct, no `any` unless justified
   - Error/empty/loading states handled
   - No secrets in code
   - No dead code / debug logs
5. **Tests**:
   - Add/adjust tests when logic is non-trivial.

## Code quality gates

- No broken build.
- No type errors.
- Lint passes (or explain why not).
- If performance-sensitive UI: memoization only with proof/need.

## How to ask me (the human) questions

If requirements are unclear:

- Propose a default and proceed.
- Clearly mark assumptions in the plan.

## “Definition of Done”

- Works locally
- Clean types
- Reasonable UX states
- Minimal regression risk
