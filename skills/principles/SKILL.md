---
name: principles
description: Use before writing, changing, or reviewing code in this repo — features, bug fixes, refactors, reviews. Not for questions or explanations with no code change.
---

At the start of a code-change task:
1. Read the index below. Pick at most 3 principles that apply and read the corresponding files. Picking none is valid for trivial edits.
2. Open the chosen files in their respective locations.
3. In the final reply, for each principle used, state the specific decision it changed. Naming a principle without a changed decision does not count.


**Core**

- [**Laziness Protocol**](../principle-laziness-protocol/SKILL.md). Refactoring, sizing a diff, or tempted to add abstractions, layers, or signal threading. Bias to deletion and the smallest change that solves the problem.
- [**Foundational Thinking**](../principle-foundational-thinking/SKILL.md). Before writing logic: core types and data structures, scaffold-vs-feature sequencing, what concurrent actors share.
- [**Redesign from First Principles**](../principle-redesign-from-first-principles/SKILL.md). Integrating a new requirement into an existing design. Redesign as if it had been foundational from day one.
- [**Subtract Before You Add**](../principle-subtract-before-you-add/SKILL.md). Sequencing an addition, refactor, or rewrite. Remove dead weight first, then build on the simpler base.
- [**Minimize Reader Load**](../principle-minimize-reader-load/SKILL.md). Reviewing or shaping code that's hard to trace. Count layers and hidden state, collapse one-caller wrappers, shrink mutable scope.
- [**Build the Lever**](../principle-build-the-lever/SKILL.md). Any non-trivial work. Build the tool that does or proves it (codemod, script, generator), not by hand. The tool is the artifact a reviewer reruns.

**Architecture**

- [**Model the Domain**](../principle-model-the-domain/SKILL.md). Writing stateful logic, or code that branches a lot or repeats a shape assumption across files. Encode the domain in a structure (state machine, typed model, table or registry, reducer, boundary, the right collection) instead of scattered conditionals.
- [**Boundary Discipline**](../principle-boundary-discipline/SKILL.md). Wiring validation, error handling, or framework adapters. Guards at system boundaries, trust internal types, keep business logic pure.
- [**Type System Discipline**](../principle-type-system-discipline/SKILL.md). Designing types or a signature in any typed language. Make illegal states unrepresentable, brand primitives, parse external data at boundaries.
- [**Make Operations Idempotent**](../principle-make-operations-idempotent/SKILL.md). Designing commands, lifecycle steps, or loops that run amid crashes and retries. Converge to the same end state.
- [**Migrate Callers Then Delete Legacy APIs**](../principle-migrate-callers-then-delete-legacy-apis/SKILL.md). Introducing a new internal API while old callers exist. Migrate and delete in one wave.

**Verification**

- [**Prove It Works**](../principle-prove-it-works/SKILL.md). After a task, before declaring done. Verify against the real artifact, not a proxy or "it compiles".
- [**Fix Root Causes**](../principle-fix-root-causes/SKILL.md). Debugging. Trace each symptom back to the first place the system went wrong and fix it there. A guard is a fix only when the state it handles is legitimate.

**Delegation**

- [**Guard the Context Window**](../principle-guard-the-context-window/SKILL.md). Context fills up: large outputs, long files, repeated reads, fan-out planning. Route bulk to subagents, keep summaries in the main thread.

**Meta**

- [**Encode Lessons in Structure**](../principle-encode-lessons-in-structure/SKILL.md). You catch yourself writing the same instruction a second time. Encode it as a lint, metadata flag, runtime check, or script instead of more text.
