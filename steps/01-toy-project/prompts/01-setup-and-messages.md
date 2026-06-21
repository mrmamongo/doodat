# 1. Setup и модель диалога

> [00-base-rules.md](00-base-rules.md)

## Цель

Минимальный Python-проект и типы для диалога агента.

## Сделать

- Инициализация проекта (uv или pip), pytest в зависимостях.
- Типы: `Message` (user / assistant / tool), `ToolCall`, `ModelResponse`, `RunResult`.
- Статусы run: `completed`, `failed`, `max_steps`.
- Smoke-тест на создание Message.

## Понять

- Assistant «просит tool» ≠ tool «отдаёт результат».
- История — список сообщений, не один строковый prompt.

## Готово когда

- [ ] `pytest` находит тесты
- [ ] Роли и ToolCall / ModelResponse / RunResult разделены явно

## Не в этом промпте

→ mock model, tools, HTTP, CLI
