# Edge cases — Этап 1

Релевантные кейсы для Toy Agent. На этом этапе закладываем поведение, не полную реализацию всех сценариев.

## Agent Loop (обязательно)

- [ ] Модель запрашивает **unknown tool** → ошибка в контексте, run не падает
- [ ] Цикл достигает **max steps** → status `max_steps`
- [ ] Модель возвращает **malformed tool call** → обработать gracefully (failed или error в контексте)
- [ ] Модель **повторяет тот же tool call** без прогресса → max_steps спасает
- [ ] **Recoverable provider error** (timeout, 429) → status `failed`, не hang
- [ ] Модель смешивает **final text и tool calls** в одном шаге → явное правило приоритета

## Tool Execution (минимум)

- [ ] Unknown tool name
- [ ] Tool бросает exception → ошибка в контексте, не крах run

## Context (осознанность)

- [ ] Пустой user input — решить явно (reject или short-circuit)

## Не на этом этапе

Filesystem, shell, git, web UI, approvals, cancellation — см. следующие шаги.

→ [Полный индекс](../../docs/agent-edge-cases.md) · [Следующий этап](../02-agent-core/edge-cases.md)
