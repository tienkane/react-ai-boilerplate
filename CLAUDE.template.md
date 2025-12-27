# Project: <YOUR_PROJECT_NAME>

> ⚠️ **This is a template file.** Copy this to `CLAUDE.md` and fill in your project details.

## One-liner

<!-- Describe your project in one sentence -->

A personal React app for <purpose>.

## Tech stack

<!-- Fill in your actual choices -->

- **React**: <Vite | Next.js | Remix | Create React App>
- **Language**: TypeScript
- **Styling**: <Tailwind CSS | CSS Modules | styled-components | Emotion | vanilla CSS>
- **State**: <React Query + Zustand | Redux Toolkit | Jotai | Recoil | Context API>
- **Forms**: <react-hook-form | Formik | native>
- **Testing**: <Vitest | Jest> + React Testing Library, E2E: <Playwright | Cypress | none>
- **Package manager**: <pnpm | npm | yarn | bun>
- **Lint/format**: <ESLint + Prettier | Biome | oxlint>

## Project-specific context

<!-- Add any important context about your project -->
<!-- Examples: -->
<!-- - This is a dashboard for managing X -->
<!-- - Users are primarily on mobile devices -->
<!-- - Performance is critical due to large data sets -->
<!-- - Must support offline mode -->

## Key directories

<!-- Map your project structure for AI understanding -->

```
src/
├── components/    # <describe what goes here>
├── features/      # <describe what goes here>
├── hooks/         # <describe what goes here>
├── lib/           # <describe what goes here>
├── types/         # <describe what goes here>
└── pages/         # <describe what goes here>
```

## Non-goals (important)

<!-- These prevent AI from over-engineering -->

- Do NOT introduce new heavy frameworks unless explicitly requested.
- Do NOT rewrite architecture for small tasks.
- Do NOT change styling system (e.g., Tailwind → something else) unless requested.
- Do NOT add backend logic unless task explicitly requires it.
- Do NOT add new dependencies without explicit approval.

## Repo conventions

### Code style

- Prefer small, focused PRs (single responsibility).
- Prefer composable components; avoid "god components" (>300 lines).
- Prefer pure functions + hooks; keep side effects isolated.
- Keep types close to usage unless shared across 3+ files.

### File naming

| Type       | Pattern                    | Example                |
| ---------- | -------------------------- | ---------------------- |
| Components | `PascalCase.tsx`           | `UserProfile.tsx`      |
| Hooks      | `useCamelCase.ts`          | `useAuth.ts`           |
| Utilities  | `camelCase.ts`             | `formatDate.ts`        |
| Types      | `types.ts` or `*.types.ts` | `user.types.ts`        |
| Tests      | `*.test.tsx`               | `UserProfile.test.tsx` |

### Import order

1. React imports
2. External libraries
3. Internal absolute imports (@/...)
4. Relative imports
5. Type imports
6. Style imports

## Workflow (must follow)

### 1. Explore first

- Identify entry points, routing, state layer, API layer.
- Confirm existing patterns before adding new ones.
- Look for similar implementations to follow.

### 2. Plan (short)

- List steps (3–7 bullets).
- Call out risks and assumptions.
- Identify files that will be changed.

### 3. Implement

- Keep diffs minimal and consistent with existing style.
- One logical change per commit.
- Follow existing patterns even if you'd do it differently.

### 4. Self-review checklist

- [ ] Types correct, no `any` unless justified with comment
- [ ] Error/empty/loading states handled
- [ ] No secrets in code
- [ ] No dead code or debug logs (console.log)
- [ ] Accessibility basics (labels, keyboard, focus)
- [ ] Mobile/responsive considered (if applicable)

### 5. Tests

- Add/adjust tests when logic is non-trivial.
- Include manual test checklist in response.

## Code quality gates

- ✅ No broken build
- ✅ No TypeScript errors
- ✅ Lint passes (or explain why exception needed)
- ✅ Tests pass (if any exist)
- ✅ No `any` without justification comment

## How to ask me (the human) questions

If requirements are unclear:

1. **Propose a default** and proceed with it.
2. **Clearly mark assumptions** in the plan section.
3. **Ask specific questions** (not open-ended).

Example:

```
Assumption: I'll use a modal for the delete confirmation.
If you prefer an inline confirmation, let me know.
```

## "Definition of Done"

A task is complete when:

- ✅ Works locally (dev server runs, feature functions)
- ✅ Types are clean (no errors, no untyped code)
- ✅ UX states covered (loading, error, empty, success)
- ✅ Minimal regression risk (existing tests pass)
- ✅ Code is reviewable (clear, follows conventions)
