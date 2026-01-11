---
title: TypeScript Conventions
description: Senior TypeScript and Node.js development guidelines
globs: ["**/*.ts", "**/*.tsx"]
source: https://google.github.io/styleguide/tsguide.html
references:
  - Airbnb TS Style: https://github.com/airbnb/javascript
  - TS Discriminated Unions: https://betterstack.com/community/guides/scaling-nodejs/discriminated-unions/
---

# TYPESCRIPT SENIOR GUIDELINES

## Type Safety
- **Discriminated Unions**: Use for exhaustive type narrowing in state machines.
- **Strict Mode**: Always enable `strict: true` in `tsconfig.json`.
- **No Explicit any**: Use `unknown` with type guards instead of `any`.

## Async/Await
- **Error Handling**: Wrap async operations in try-catch with custom error classes.
- **Parallelism**: Use `Promise.all` for independent operations to maximize throughput.

## Modularity
- **Dependency Injection**: Use constructor injection or composition for repositories and services.
- **Single Responsibility**: Each module/class should have exactly one reason to change.

## Performance
- **Memoization**: Use `React.memo`, `useMemo`, and `useCallback` to avoid unnecessary re-renders.
- **Lazy Loading**: Use code splitting and dynamic imports for large modules.
