---
title: Git Workflow
description: Comprehensive git workflow guidelines for development teams
globs: ["**/*"]
alwaysApply: true
source: https://www.conventionalcommits.org/
references:
  - GitHub Flow: https://docs.github.com/en/get-started/using-git/github-flow
  - GitLab Flow: https://docs.gitlab.com/ee/workflow/gitlab_flow.html
  - Conventional Commits: https://www.conventionalcommits.org/
---

# GIT WORKFLOW

## Overview
Effective Git workflow is essential for maintaining clean, reproducible codebases and enabling smooth collaboration. This guide combines best practices from Conventional Commits, GitHub Flow, and GitLab Flow.

## Branch Management
### Feature Branch Strategy
**Use feature branches for all development work.** Never commit directly to `main`.
- `feature/<ticket-id>-<description>`
- `bugfix/<ticket-id>-<description>`
- `hotfix/<ticket-id>-<description>`

## Atomic Commits
An atomic commit changes **exactly one thing** and passes all tests.
- Easy to bisect bugs.
- Cleaner history.
- Easier rollback.

## Rebasing Strategy
**Rebase onto the upstream branch** before merging to maintain linear history.
```bash
git fetch origin
git rebase origin/main
```

## Pull Request Quality
Every PR should include a description, type of change, related issues, and testing proof.
- Small PRs (< 300 lines) are preferred for faster reviews.

## Conventional Commits
Format: `<type>[optional scope]: <subject>`
Types: `feat`, `fix`, `docs`, `style`, `refactor`, `perf`, `test`, `ci`, `build`, `chore`.
Breaking Changes: Use `!` after type, e.g., `feat(api)!: remove deprecated endpoint`.
