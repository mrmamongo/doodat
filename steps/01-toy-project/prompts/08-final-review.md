# 8. Финальный review

> [00-base-rules.md](00-base-rules.md)

## Цель

Сдача этапа 1 ментору по [DOD.md](../DOD.md).

## Попроси у AI

1. Пройти DOD и указать пробелы.
2. Минимальные правки только для закрытия пробелов.
3. Обновить README проекта: цель, установка, mock/live, тесты, ограничения.

## Демо перед сдачей

**Mock:** happy path · unknown tool · max_steps  
**Live:** `--live` + calculator · (опционально) failed при bad key  
**pytest:** все зелёные

## Устно (своими словами)

- Агент vs chatbot
- assistant tool call vs tool result
- Зачем mock и max_steps
- Зачем hardcode ключа и что на этапе 2

## Готово когда

- [ ] DOD закрыт
- [ ] Demo ~5 мин без подсказок
- [ ] 3–5 буллетов «что унесу на этап 2»

## Не на финале

→ agent_core, fs, shell, git, большой рефакторинг

## Шаблон отчёта ментору

```
Этап 1 сдан.
Mock: …
Live: …
pytest: N passed
Вопросы: …
Сложнее всего: …
На этап 2: …
```
