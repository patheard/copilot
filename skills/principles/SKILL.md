---
name: principles
description: Use before writing, changing, or reviewing code in this repo — features, bug fixes, refactors, reviews. Not for questions or explanations with no code change.
---

At the start of a code-change task:
1. Read the index below. Pick at most 2 principles that apply. Picking none is valid for trivial edits.
2. Open the chosen files in their respective locations.
3. In the final reply, for each principle used, state the specific decision it changed. Naming a principle without a changed decision does not count.

Precedence when they conflict: fix-root-causes > prove-it-works > laziness-protocol > boundary-discipline.

| Principle | Applies when | File |
|---|---|---|
| fix-root-causes | a bug or unexpected behaviour is being fixed | [fix-root-causes.md](../principle-fix-root-causes/SKILL.md) |
| prove-it-works | any change with observable behaviour | [prove-it-works.md](../principle-prove-it-works/SKILL.md) |
| laziness-protocol | any code is being added | [laziness-protocol.md](../principle-laziness-protocol/SKILL.md) |
| boundary-discipline | code reads input, files, env vars, or API responses | [boundary-disciplined.md](../principle-boundary-discipline/SKILL.md) |
