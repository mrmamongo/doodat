# 5. Agent Loop

> [00-base-rules.md](00-base-rules.md)

## Цель

Цикл агента — один для Mock и Live.

## Сделать

- `AgentLoop.run(user_input, model, tools, max_steps) -> RunResult`.
- Шаг: model.complete → tool calls или final answer.
- Tool result в history с role=tool.
- Unknown tool → ошибка в history, цикл продолжается.
- Ошибка model (timeout и т.д.) → status `failed`.
- Исчерпан max_steps → status `max_steps`.
- `model` передаётся снаружи (mock или live).

## Понять

- Агент = цепочка шагов; каждый tool result виден следующему решению модели.

## Готово когда

- [ ] Mock: happy path (2 tools → final → completed)
- [ ] Mock: unknown tool — run не падает
- [ ] Mock: зацикленный скрипт → max_steps
- [ ] Live в том же run() — одна ручная проверка
- [ ] Loop не зависит от CLI

## Не в этом промпте

→ Typer/Rich, полный набор pytest (→ промпт 7)
