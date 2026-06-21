# Этап 1 · Toy Agent Playground

**Срок:** 2 недели  
**Стек:** Python 3.12+, uv, pytest (Typer + Rich по желанию для CLI)

Минимальный coding agent: агентский цикл, роли сообщений, tool calls, mock model для тестов и один real provider (OpenAI-compatible) — пока захардкоженный.

## Зачем этот этап

- Понять агент как **цикл с явными состояниями**, а не как «магию LLM».
- Увидеть разницу между «модель думает» и «агент действует».
- Заложить модель, которую все следующие этапы будут расширять, а не переписывать.

## Что изучаем

| Концепция | Суть |
|-----------|------|
| **Agent Loop** | Решение → действие → обновление контекста → повтор, с лимитом шагов |
| **Message Roles** | user / assistant / tool — история как память run |
| **Tool Call** | Имя + аргументы как данные; runtime исполняет отдельно |
| **Final Answer vs Tool Call** | На каждом шаге модель выбирает одно из двух |
| **Mock Model** | Детерминированные ответы для pytest и edge cases |
| **Real Provider** | OpenAI-compatible API; модель сама выбирает tools |
| **Run Lifecycle** | completed / failed / max_steps — явные финальные статусы |

## Чего здесь НЕ делаем

- Несколько провайдеров и env-конфиг (это этап 2).
- Файловая система, shell, git, web UI, approvals.
- Отдельные пакеты в monorepo — один учебный проект.

## Как проходить этап

1. Прочитай [детальный разбор в роадмапе](../../agent-roadmap.html#stage-1) (вкладка «1 · Toy Agent»).
2. Ознакомься с [edge cases этапа](edge-cases.md).
3. Иди по [промптам](prompts/) **по порядку** + [00-base-rules](prompts/00-base-rules.md) в каждой сессии.
4. После каждого промпта — проверь блок **«Готово когда»**.
5. В конце — пройди [Definition of Done](DOD.md) с ментором.

## Промпты

См. [prompts/README.md](prompts/README.md) — порядок и таблица. Кратко: base rules → типы → mock → tools → live → loop → CLI → tests → review.

## Ожидаемое поведение (кратко)

**Mock-режим** — для автотестов:

- Happy path: несколько tool calls → final answer → `completed`.
- Unknown tool: ошибка в контексте, run не падает.
- Max steps: зацикленный mock → `max_steps`.

**Live-режим** — для демо ментору:

- Тот же Agent Loop, другой источник модели.
- Модель сама выбирает calculator tool на простой задаче.
- Ошибка сети / 401 / 429 → `failed`, не зависание.

## Связь со следующим этапом

На этапе 2 цикл вынесут в `agent_core`, mock и live станут реализациями `ModelClient` Protocol, hardcode ключей уйдёт в env. Не закладывай «на вырост» — держи код простым, но с понятными границами (цикл / модель / tools / CLI).

## Полезные ссылки

- [Roadmap (HTML)](../../agent-roadmap.html#stage-1)
- [Все шаги](../README.md)
- [Edge cases этапа](edge-cases.md)
- [Definition of Done](DOD.md)
- [Промпты](prompts/)
