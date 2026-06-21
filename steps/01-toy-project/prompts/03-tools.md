# 3. Mock Tools

> [00-base-rules.md](00-base-rules.md)

## Цель

Минимальный набор инструментов и вызов по имени.

## Сделать

- Tools: `echo`, `add`, `now`.
- Реестр name → handler (dict достаточно).
- `execute_tool(name, args)` — unknown tool возвращает **строку ошибки**, не exception.
- Тест на каждый tool + unknown tool.

## Понять

- Решение модели (tool call) и исполнение (runtime) — разные шаги.

## Готово когда

- [ ] echo, add, now работают
- [ ] unknown tool — ошибка без падения процесса

## Не в этом промпте

→ OpenAI tool schemas, Agent Loop
