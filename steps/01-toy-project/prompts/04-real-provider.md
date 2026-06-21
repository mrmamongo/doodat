# 4. Real Provider (OpenAI-compatible)

> [00-base-rules.md](00-base-rules.md)

## Цель

Один live-провайдер с tool calling — тот же контракт, что у Mock.

## Сделать

- `complete(messages, tools_schema) -> ModelResponse`.
- Hardcode: `BASE_URL`, `API_KEY`, `MODEL_NAME` (ключ не коммитить).
- В API: history + описания tools (echo, add, now).
- Парсинг: tool_calls или final content.
- HTTP timeout; ошибки сети / 401 / 429 → typed error для loop.

## Понять

- Mock и live взаимозаменяемы для Agent Loop.
- Live не идёт в pytest.

## Готово когда

- [ ] Ручной вызов complete работает
- [ ] Задача «17+25, use add» → модель вызывает add (ручная проверка)
- [ ] Timeout и ошибки не вешают процесс
- [ ] pytest по-прежнему без live

## Не в этом промпте

→ Agent Loop, флаг `--live`, env/dotenv
