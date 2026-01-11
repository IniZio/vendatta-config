---
name: shell-executor
description: Execute shell commands with safety checks and logging
parameters:
  type: object
  properties:
    command: { type: string, description: "Command to execute" }
execute:
  command: "bash"
  args: ["-c", "{{.command}}"]
references:
  - OWASP Shell Injection: https://cheatsheetseries.owasp.org/cheatsheets/OS_Command_Injection_Defense_Cheat_Sheet.html
---

# Shell Executor
Standard tool for running shell commands within the isolated environment.

## Best Practices
- **Timeouts**: Always implement timeouts for long-running commands.
- **Error Handling**: Properly handle non-zero exit codes.
- **Quoting**: Use proper quoting to prevent shell injection.
