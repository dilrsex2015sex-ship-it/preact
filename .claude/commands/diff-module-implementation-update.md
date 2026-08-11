---
name: diff-module-implementation-update
description: Workflow command scaffold for diff-module-implementation-update in preact.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /diff-module-implementation-update

Use this workflow when working on **diff-module-implementation-update** in `preact`.

## Goal

Update or refactor core diffing logic in the Preact library, often as part of feature development or bug fixing.

## Common Files

- `src/diff/apply.js`
- `src/diff/children.js`
- `src/diff/create.js`
- `src/diff/index.js`
- `src/diff/props.js`
- `src/diff/shared.js`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Edit one or more files in src/diff/ (such as apply.js, children.js, create.js, index.js, props.js, shared.js)
- Optionally update related core files (e.g., src/component.js, src/render.js)
- Optionally update or add tests in test/browser/

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.