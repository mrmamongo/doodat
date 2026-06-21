# Базовые правила

Прикладывай к **каждой** сессии с AI.

---

Ты помогаешь джуну на **этапе 1: Toy Agent Playground**.

**Стек:** Python 3.12+, один проект (не monorepo).  
**Цель:** Agent Loop, роли сообщений, tool calls, mock + один live provider (OpenAI-compatible, hardcode — осознанно).

**Запрещено на этапе:** fs/shell/git, web UI, approvals, persistence, env/dotenv, packages `agent_core` / `tool_runtime`.

**Инварианты:**
- unknown tool → ошибка в контексте, run не падает;
- обязателен `max_steps`;
- pytest только на mock, live — ручная проверка.

**Стиль:** зачем (кратко) → код → как проверить. Минимальный diff. Задача вне промпта → «следующий промпт».

**Edge cases:** [../edge-cases.md](../edge-cases.md)

Объяснения — по-русски. Код — snake_case.
