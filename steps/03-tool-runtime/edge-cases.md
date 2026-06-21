# Edge cases — Этап 3

## Tool Execution (основной фокус)

- [ ] Tool **timeout** or hang
- [ ] Tool throws **exception** → structured ToolResult error
- [ ] Output **too large** → truncate with notice
- [ ] **Invalid input** schema → reject before execute
- [ ] **Unknown tool** at registry level
- [ ] Multiple tool calls from one step → **sequential**, predictable order
- [ ] Tool success but **application-level error** in output

→ [Этап 2](../02-agent-core/edge-cases.md) · [Этап 4](../04-workspace-tools/edge-cases.md)
