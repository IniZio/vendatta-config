---
title: TDD Best Practices
description: Comprehensive Test-Driven Development guidelines
globs: ["**/*_test.go", "**/*.test.ts", "**/*.spec.js"]
alwaysApply: true
source: https://martinfowler.com/bliki/TestDrivenDevelopment.html
references:
  - Kent Beck - TDD By Example: https://www.oreilly.com/library/view/test-driven-development/0321146530/
  - Martin Fowler - BDD: https://martinfowler.com/bliki/GivenWhenThen.html
---

# TDD BEST PRACTICES

## The Red-Green-Refactor Cycle
1. **RED**: Write a failing test BEFORE writing any production code.
2. **GREEN**: Write the SIMPLEST code that makes the test pass.
3. **REFACTOR**: Improve structure and readability without breaking tests.

## Test Isolation
- **Independence**: Each test must be completely independent. No shared state.
- **Deterministic**: Tests must produce the same results given the same inputs. Avoid random IDs or timestamps.

## BDD Patterns (Given-When-Then)
Organize tests around behavior, not implementation.
- **Given**: Preconditions and setup.
- **When**: The action being tested.
- **Then**: Expected outcome and assertions.

## AAA Pattern
**Arrange-Act-Assert** for clarity in test structure.

## Coverage Guidelines
**Aim for 80%+ coverage on new logic.** Focus on business logic, error handling, and edge cases. Avoid testing external libraries or framework internals.
