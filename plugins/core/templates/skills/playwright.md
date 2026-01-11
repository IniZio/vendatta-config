---
name: playwright
description: Browser automation and web scraping via Playwright
parameters:
  type: object
  properties:
    url: { type: string, description: "URL to visit" }
    action: { type: string, description: "Action to perform (screenshot, trace, test)" }
execute:
  command: "npx"
  args: ["playwright", "test"]
source: https://playwright.dev/
references:
  - Trace Viewer: https://www.browserstack.com/guide/playwright-trace-viewer
  - Visual Testing: https://css-tricks.com/automated-visual-regression-testing-with-playwright/
---

# Playwright Skill
Allows the agent to interact with web pages using Playwright for E2E testing, screenshots, and tracing.

## Patterns
- **Page Object Model**: Organize selectors and actions in reusable objects.
- **Tracing**: Enable tracing for all failed tests to debug in CI.
- **Visual Regressions**: Compare screenshots across builds to catch UI bugs.
