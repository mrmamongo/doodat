# Этап 2 · Agent Core Library

**Срок:** 2 недели · **Статус:** roadmap ✅ · промпты 🔜

Вынести агентский цикл в переиспользуемое ядро: `ModelClient` Protocol, поток событий, отмена run, env-config вместо hardcode.

## Концепции

- Agent Core как библиотека
- ModelClient (Protocol) — mock и live за одним контрактом
- Dependency Injection
- RunState, AgentEvent, Event Stream
- Cancellation, config через env
- Thin client (toy_agent)

## Материалы

- [Детальный разбор в роадмапе](../../agent-roadmap.html#stage-2)
- [Edge cases этапа](edge-cases.md)
- [Все шаги](../README.md)

## Следующий шаг

После сдачи этапа 1 → промпты появятся в `prompts/`.
