---
name: john-methodology
description: Use when the user is making a design, product, or technical decision with a stated rationale (explained "why"), or says "记"/"note" / "记录一下". Also use when asked to apply the user's past decision methodology ("load john-methodology", "按我的方法论"). Do not capture un-explained preferences or factual confirmations.
---

# John's Decision Methodology

Captures John's design/product/UX/engineering taste as decisions-with-reasons, then distills them into reusable principles so future AI sessions can reason the way John does instead of re-deriving from scratch.

## Core principle

**Not everything is worth keeping — only decisions John explained.** A decision with a stated reason reveals his taste, mental model, and experience. A bare preference does not.

## When to use

- During any design discussion, brainstorm, spec review, or code review where John states a preference WITH a reason ("I prefer X because...", "don't do Y — it makes Z confusing").
- When John explicitly asks to record ("记", "note", "记下来", "这条记一下").
- When asked to recall or apply John's prior methodology ("用我的思路处理", "我以前怎么定的").
- **Not** for: factual confirmations, implementation details, un-explained preferences, throwaway decisions.

## Capture flow

1. **Silently accumulate** during conversation. Do NOT interrupt to ask "should I record this?".
2. Value signals — capture when the reason shows:
   - **Product/UX taste**: interaction model choices, what feels intuitive, reducing user confusion.
   - **Mental model**: preferring one consistent model over special cases, flat over nested, simple over feature-complete.
   - **Experience**: "this bit us before", cost-benefit of already-built vs new, YAGNI instincts.
3. At a natural break (end of topic, end of session), present a **confirmation card** listing candidates: each as `场景 / 决策 / 理由`. John edits (add/delete/modify) before anything is written.

## Record format

One entry per decision, appended to `decisions/YYYY-MM.md`:

```markdown
## #N (YYYY-MM-DD)
- 场景: <context — what was being discussed>
- 决策: <the choice, including options rejected>
- 理由: <John's rationale, in his words or faithful restatement>
- 标签: <product-ux | mental-model | experience | engineering>
```

Numbering is sequential within the file. Tags help later distillation.

## Distillation (principles)

- After ~10 recorded decisions, PROPOSE a distillation session (do not auto-run). John agrees → draft `principles.md` entries: each principle = a generalized rule + links to supporting decision numbers.
- Keep the raw decision text; principles are summaries that reference back, never replacements.
- Re-run distillation as the backlog grows; merge duplicate principles.

## Consumption

When making a design/product/technical decision that resembles a recorded one, check `principles.md` (and `decisions/` for the originals) and apply John's established preference. State when you're applying a past principle ("following your methodology from #12...").

## File layout

```
john-methodology/
├── SKILL.md
├── decisions/YYYY-MM.md   # raw decision entries
└── principles.md          # distilled principles with case links
```
