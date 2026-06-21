# Edge cases — Этап 3

## Tool Execution (основной фокус)

- [ ] Tool **timeout** or hang
- [ ] Tool throws **exception** → structured ToolResult error
- [ ] Output **too large** → truncate with notice
- [ ] **Invalid input** schema → reject before execute
- [ ] **Unknown tool** at registry level
- [ ] Parallel tool calls with **hidden dependencies** → sequential when needed
- [ ] Tool success but **application-level error** in output

→ [Этап 2](../02-agent-core/edge-cases.md) · [Этап 4](../04-workspace-tools/edge-cases.md)
