---
name: lint-all
description: Run all linters in the repository
steps:
  - name: Run Linters
    command: "make lint || golangci-lint run || npm run lint"
---

# Lint All
Composite command to run all linters across different language ecosystems.
