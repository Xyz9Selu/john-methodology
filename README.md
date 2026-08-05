# john-methodology

John's personal decision-methodology knowledge base for AI agents.

This is a superpowers-style skill that captures **decisions John made with a stated reason** — the choices that reveal his product/UX taste, mental model, and engineering experience — then distills them into reusable principles so future AI sessions can reason the way John does instead of re-deriving from scratch.

## What this is NOT

Not a log of everything John did. Only decisions he **explained** — preferences with a "why" behind them. Bare preferences, factual confirmations, and throwaway implementation details are deliberately excluded.

## Layout

```
john-methodology/
├── SKILL.md          # capture / confirm / distill / consume workflow
├── decisions/        # raw decision entries (YYYY-MM.md)
│   └── 2026-08.md    # seed entries from smart-manu-ops + C-30 discussion
└── principles.md     # distilled principles (P1–P10), each linking to decision numbers
```

## How it works

1. **Capture** — during design/product/tech discussions, AI silently accumulates decisions where John explains his reasoning (UX intuition, mental-model preferences, "this bit us before" experience). John can hard-trigger with "记" / "note".
2. **Confirm** — at a natural break, AI presents a confirmation card (one entry per decision: 场景/决策/理由). Nothing is written until John approves.
3. **Distill** — after ~10 decisions, AI *proposes* a distillation run; John approves → `principles.md` is generated or extended. Raw decisions are always kept as the source of truth.
4. **Consume** — future AI sessions apply John's established preferences when facing similar decisions, citing the supporting principle.

## Recurring signatures (from the seed data)

- Warn-and-surface over block-and-refuse (conditioned on an external final-review system existing)
- Single source of truth; never silently fall back
- Cut complexity that has no visible output, even days after approving it
- Verify a signal discriminates in real data before modeling a state on it
- UI collects, doesn't prescribe; every visible element serves a user decision
- Scoped, thresholded guardrails instead of universal mandates
- Simplest construct first; machinery (engines/abstractions/new entities) only when a concrete need appears

## Install

Clone or copy into your agent runtime's global skills directory:

```bash
git clone git@github.com:Xyz9Selu/john-methodology.git ~/.agents/skills/john-methodology
```

Requires a runtime that auto-discovers skills from `~/.agents/skills/` (e.g. opencode).

## License

GPL-3.0 — see [LICENSE](LICENSE).
