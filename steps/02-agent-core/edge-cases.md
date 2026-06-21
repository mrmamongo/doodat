# Edge cases — Этап 2

## Agent Loop

- [ ] Run **cancelled** while model or tool active → status `cancelled`, graceful stop
- [ ] Provider error mid-run → `failed`, history preserved
- [ ] Incomplete **trace** if events not emitted — каждый шаг должен давать событие

## Context / Config

- [ ] Secrets in env — не в git, `.env.example` без ключей
- [ ] Missing env var → понятная ошибка при старте live

## CLI (thin client)

- [ ] Core **не печатает** в терминал — только события

## Накопленное с этапа 1

Unknown tool, max steps, provider timeout — по-прежнему актуально.

→ [Этап 1](../01-toy-project/edge-cases.md) · [Этап 3](../03-tool-runtime/edge-cases.md)
