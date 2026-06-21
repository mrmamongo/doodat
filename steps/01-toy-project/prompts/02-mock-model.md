# 2. Mock Model

> [00-base-rules.md](00-base-rules.md)

## Цель

Детерминированный источник решений модели для тестов.

## Сделать

- `MockModel` со скриптом: список `ModelResponse` по порядку.
- `complete(messages) -> ModelResponse` — та же сигнатура, что у будущего live.
- После конца скрипта — fallback, не exception.
- Тест: tool → tool → final answer строго по скрипту.

## Понять

- Mock изолирует логику цикла от качества LLM и сети.

## Готово когда

- [ ] Повторные вызовы с одним скриптом дают одинаковый результат
- [ ] pytest без network

## Не в этом промпте

→ live provider, Agent Loop
