# 6. CLI и вывод

> [00-base-rules.md](00-base-rules.md)

## Цель

Тонкий CLI: wiring + отображение шагов. Mock по умолчанию, `--live` для API.

## Сделать

- `python -m toy_agent "prompt"` — mock; `--live`, `--max-steps N`.
- На каждом шаге: номер, tool/final, result/error.
- В конце: status, steps_taken, финальный ответ.
- Exit code: 0 = completed, иначе non-zero.
- Ctrl+C — короткое сообщение, без полного traceback.

## Понять

- CLI не содержит логику цикла — только запуск и render.

## Готово когда

- [ ] Mock timeline читаем
- [ ] `--live` использует тот же AgentLoop
- [ ] README проекта: установка, mock vs live

## Не в этом промпте

→ sessions, approvals, event stream (этап 2)
