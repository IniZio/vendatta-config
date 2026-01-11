---
title: Go Conventions
description: Senior Go development guidelines and best practices
globs: ["**/*.go"]
source: https://go.dev/wiki/CodeReviewComments
references:
  - Effective Go: https://go.dev/doc/effective_go
  - Uber Go Style Guide: https://github.com/uber-go/guide
  - Go ADK: https://developers.googleblog.com/announcing-the-agent-development-kit-for-go-build-powerful-ai-agents-with-your-favorite-languages/
---

# GO SENIOR GUIDELINES

## Error Handling
- **Wrapping**: Always wrap errors with context using `fmt.Errorf("...: %w", err)`.
- **Unwrapping**: Use `errors.Is` and `errors.As` for type-specific handling.
- **Testify**: Use `github.com/stretchr/testify/assert` and `require` for all tests.

## Concurrency
- **Limit Goroutines**: Use worker pools or semaphores. Never spawn unbounded goroutines.
- **Context**: Always pass and respect `context.Context` for cancellation and timeouts.

## Package Structure
- **Internal**: Use `internal/` for private implementation details.
- **Pkg**: Use `pkg/` for public libraries.
- **Naming**: Short, lowercase, single-word package names.

## Interface Design
- **Accept Interfaces, Return Structs**: Define interfaces as parameters, concrete types as returns.
- **Small Interfaces**: Prefer composition of small, focused interfaces (e.g., `io.Reader`).

## Testing
- **Table-Driven Tests**: Use for testing multiple scenarios efficiently.
- **Test Helpers**: Use `t.Helper()` for better error reporting in utilities.
