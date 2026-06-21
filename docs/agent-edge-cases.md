# Edge cases — индекс по этапам

Edge cases разложены по папкам `steps/`. На каждом этапе учитывай свой файл + всё накопленное ранее.

| Этап | Файл | Фокус |
|------|------|--------|
| 1 | [01-toy-project](../steps/01-toy-project/edge-cases.md) | Agent loop, unknown tool, max steps, provider errors |
| 2 | [02-agent-core](../steps/02-agent-core/edge-cases.md) | Cancellation, events, RunState, config |
| 3 | [03-tool-runtime](../steps/03-tool-runtime/edge-cases.md) | Tool execution, validation, timeout, output limits |
| 4 | [04-workspace-tools](../steps/04-workspace-tools/edge-cases.md) | Filesystem, shell, sandbox, security basics |
| 5 | [05-coding-cli](../steps/05-coding-cli/edge-cases.md) | CLI, sessions, approvals, Ctrl+C |
| 6 | [06-agent-server](../steps/06-agent-server/edge-cases.md) | HTTP, SSE, persistence, reconnect |
| 7 | [07-web-ui](../steps/07-web-ui/edge-cases.md) | Streaming UI, tabs, diff viewer |
| 8 | [08-git-aware](../steps/08-git-aware/edge-cases.md) | Git status, diff, commit, dirty tree |

## Полный список (справочник)

<details>
<summary>Agent Loop</summary>

- The model returns malformed tool-call JSON.
- The model requests an unknown tool.
- The model repeats the same tool call without making progress.
- The model gives a final answer before the task is actually complete.
- The model mixes final text with tool calls in a single step.
- The loop reaches the maximum step count.
- A recoverable model/provider error occurs mid-run.
- A run is cancelled while the model or a tool is active.
- The latest user message changes or cancels the active task.
- The trace is incomplete, making the run impossible to debug.

</details>

<details>
<summary>Tool Execution</summary>

- A tool times out or hangs.
- A tool throws an exception.
- A tool returns output larger than the context budget.
- A tool returns binary data or invalid text encoding.
- A read-only tool mutates state.
- A tool requires user approval before execution.
- A tool call is unsafe or destructive.
- A tool needs interactive input that the runtime cannot provide.
- Multiple tool calls can run in parallel, but some have hidden dependencies.
- A tool reports success while its output contains an application-level error.

</details>

<details>
<summary>File System · Shell · Context · Security · Git · CLI · Web UI</summary>

См. соответствующие файлы в `steps/04-*` … `steps/08-*`.

</details>
