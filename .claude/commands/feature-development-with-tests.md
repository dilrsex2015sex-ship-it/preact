---
name: feature-development-with-tests
description: Workflow command scaffold for feature-development-with-tests in preact.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /feature-development-with-tests

Use this workflow when working on **feature-development-with-tests** in `preact`.

## Goal

Develop or refactor a feature and update corresponding browser tests to ensure correctness.

## Common Files

- `src/component.js`
- `src/render.js`
- `test/browser/render.test.js`
- `test/browser/keys.test.js`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Edit implementation files (commonly in src/)
- Update or add test files in test/browser/ (e.g., render.test.js, keys.test.js)

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.