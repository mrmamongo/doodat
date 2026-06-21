# 7. Тесты

> [00-base-rules.md](00-base-rules.md)

## Цель

pytest на mock-сценариях; сверка с [edge-cases.md](../edge-cases.md).

## Сделать

- `test_loop_happy_path` — 2 tools → final, completed
- `test_unknown_tool` — ошибка в messages, run жив
- `test_max_steps` — зацикленный mock
- Опционально: simulated model error → failed
- README: «тесты = mock only»

## Покрытие edge cases

| Case | pytest | live вручную |
|------|--------|--------------|
| Unknown tool | ✓ | — |
| Max steps | ✓ | — |
| Provider timeout | simulate | ✓ |
| Empty input | опционально | — |

## Готово когда

- [ ] `pytest` зелёный, без API keys и network
- [ ] Тесты читаются как спецификация поведения

## Не в этом промпте

→ live в CI, pytest-asyncio (если sync loop)
