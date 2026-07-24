```markdown
# preact Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches you how to contribute to the [preact](https://github.com/preactjs/preact) codebase, a fast 3kB alternative to React with the same modern API. You'll learn the project's coding conventions, how to implement and test features, and how to safely update core diffing logic. The guide includes step-by-step workflows, code style examples, and command suggestions to streamline your development process.

## Coding Conventions

**File Naming**
- Use `camelCase` for file names.
  - Example: `component.js`, `render.js`, `sharedUtils.js`

**Import Style**
- Use relative imports for internal modules.
  - Example:
    ```js
    import { diff } from './diff/index.js';
    import { render } from '../render.js';
    ```

**Export Style**
- Prefer named exports.
  - Example:
    ```js
    // In src/render.js
    export function render(vnode, parent) { ... }
    ```

**Commit Messages**
- Freeform style, no strict prefixes.
- Short and descriptive (average ~13 characters).
  - Example: `fix hydration`, `add test for keys`

## Workflows

### diff-module-implementation-update
**Trigger:** When you need to improve, refactor, or fix the diffing algorithm or its related logic.  
**Command:** `/update-diff-logic`

1. Edit one or more files in `src/diff/` (such as `apply.js`, `children.js`, `create.js`, `index.js`, `props.js`, `shared.js`).
    - Example:
      ```js
      // src/diff/children.js
      export function diffChildren(...) { ... }
      ```
2. Optionally update related core files (e.g., `src/component.js`, `src/render.js`) if your changes affect component behavior or rendering.
3. Optionally update or add tests in `test/browser/` to cover your changes.
    - Example:
      ```js
      // test/browser/render.test.js
      import { render } from '../../src/render.js';
      test('should render children correctly', () => { ... });
      ```

### feature-development-with-tests
**Trigger:** When implementing or modifying a feature and ensuring it is covered by tests.  
**Command:** `/feature-with-tests`

1. Edit or create implementation files, commonly in `src/`.
    - Example:
      ```js
      // src/component.js
      export function Component(props) { ... }
      ```
2. Update or add corresponding test files in `test/browser/` (e.g., `render.test.js`, `keys.test.js`).
    - Example:
      ```js
      // test/browser/keys.test.js
      import { h, render } from '../../src/index.js';
      test('should handle keys correctly', () => { ... });
      ```

## Testing Patterns

- Test files are located in `test/browser/` and follow the `*.test.*` naming pattern.
- The exact test framework is unknown, but tests are written in JavaScript and typically import modules from `src/`.
- Example test file:
  ```js
  // test/browser/render.test.js
  import { render } from '../../src/render.js';

  test('renders a simple component', () => {
    // ...test implementation...
  });
  ```

## Commands

| Command              | Purpose                                                        |
|----------------------|----------------------------------------------------------------|
| /update-diff-logic   | Start or review a diff module implementation/refactor workflow |
| /feature-with-tests  | Begin feature development with corresponding tests             |
```
