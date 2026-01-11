---
name: test-suite
description: Run all tests in the repository
steps:
  - name: Run Tests
    command: "make test || go test ./... || npm test"
---

# Test Suite
Composite command to run all tests across different language ecosystems.
