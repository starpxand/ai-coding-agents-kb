# 📊 Сравнительная таблица агентных инструментов разработки

> *Все данные актуальны на май 2026 года*

---

## Основная сравнительная таблица

| Инструмент | Тип | Базовые модели | Агентный режим | Локальная работа | Open Source |
|-----------|-----|---------------|---------------|-----------------|-------------|
| **Cursor** | Standalone IDE | Claude 3.7, GPT-4o, Gemini | ✅ Composer Agent | ❌ | ❌ |
| **Windsurf** | Standalone IDE | Claude Sonnet, GPT-4o | ✅ Cascade | ❌ | ❌ |
| **Google Antigravity** | Standalone IDE | Gemini 3 Pro, Claude Sonnet 4.6, GPT-OSS | ✅ Agent Manager | ❌ | ❌ |
| **Qoder** | Standalone IDE / Plugin / CLI | Claude, GPT, Gemini | ✅ Quest Mode | ❌ | ❌ |
| **GitHub Copilot** | IDE Extension | GPT-4o, Claude 3.5 | ✅ Copilot Edits | ❌ | ❌ |
| **Codeium** | IDE Extension | Codeium собственные | ⚠️ Ограниченный | ❌ | ❌ |
| **Tabnine** | IDE Extension | Tabnine / локальные | ❌ | ✅ Enterprise | ❌ |
| **Continue** | IDE Extension | Любые (конфиг) | ⚠️ Зависит | ✅ (Ollama) | ✅ |
| **OpenAI Codex** | CLI / Extension / Cloud | GPT-5.5, GPT-5.4, GPT-4.1 | ✅ Полноценный | ❌ | ✅ (CLI) |
| **Claude Code** | CLI Agent | Claude 3.5/3.7 Sonnet | ✅ Полноценный | ❌ | ❌ |
| **Aider** | CLI Agent | Любые (конфиг) | ✅ Git-агент | ✅ (Ollama) | ✅ |

---

## Условия бесплатного использования

| Инструмент | Бесплатный тариф | Лимиты | Ограничения |
|-----------|-----------------|--------|-------------|
| **Cursor** | ✅ Hobby | 2 000 completion/мес, 50 premium-запросов | Медленные premium-запросы |
| **Windsurf** | ✅ Free | 25 кредитов/день | Premium-модели за кредиты |
| **Google Antigravity** | ✅ Публичное превью | Щедрые лимиты Gemini 3 | Нужен личный Gmail |
| **Qoder** | ✅ 14-дневный Pro-триал | ~2000 запросов в превью | Quest Mode расходует быстрее |
| **GitHub Copilot** | ✅ Free | 2 000 completion/мес, 50 чатов/мес | Ограниченные модели |
| **Codeium** | ✅ Individual | Неограниченно | Только базовые модели Codeium |
| **Tabnine** | ✅ Basic | Неограниченные completion | Нет чата, нет персонализации |
| **Continue** | ✅ Полностью | Нет лимитов расширения | Платишь только за API модели |
| **OpenAI Codex** | ⚠️ Пробные кредиты | Ограниченные при регистрации | Нужен платный ChatGPT для регулярного использования |
| **Claude Code** | ❌ | — | Входит в Claude Pro ($20/мес) |
| **Aider** | ✅ Всегда | Нет лимитов (open-source) | Платишь только за API модели |

---

## Функциональные возможности

| Инструмент | Inline Completion | Chat | Multi-file Edit | Terminal | Browser Agent | Code Review |
|-----------|:----------------:|:----:|:---------------:|:--------:|:-------------:|:-----------:|
| **Cursor** | ✅ | ✅ | ✅ | ✅ | ❌ | ⚠️ |
| **Windsurf** | ✅ | ✅ | ✅ | ✅ | ❌ | ⚠️ |
| **Google Antigravity** | ✅ | ✅ | ✅ | ✅ | ✅✅ | ⚠️ |
| **Qoder** | ✅ | ✅ | ✅ | ✅ | ❌ | ⚠️ |
| **GitHub Copilot** | ✅ | ✅ | ✅ | ✅ | ❌ | ✅ |
| **Codeium** | ✅ | ✅ | ❌ | ❌ | ❌ | ❌ |
| **Tabnine** | ✅ | ✅ (Pro) | ❌ | ❌ | ❌ | ❌ |
| **Continue** | ✅ | ✅ | ⚠️ | ❌ | ❌ | ❌ |
| **OpenAI Codex** | ❌ | ✅ | ✅ | ✅ | ✅ | ✅ |
| **Claude Code** | ❌ | ✅ | ✅ | ✅ | ❌ | ✅ |
| **Aider** | ❌ | ✅ | ✅ | ✅ | ❌ | ❌ |

**Легенда:** ✅ Полная поддержка | ⚠️ Частичная | ❌ Отсутствует

---

## Поддерживаемые редакторы

| Инструмент | VS Code | JetBrains | Vim/NeoVim | Терминал | Браузер |
|-----------|:-------:|:---------:|:----------:|:--------:|:-------:|
| **Cursor** | Встроен | ❌ | ❌ | ❌ | ❌ |
| **Windsurf** | Встроен | ❌ | ❌ | ❌ | ❌ |
| **Google Antigravity** | Встроен | ❌ | ❌ | ❌ | ✅ встроен |
| **Qoder** | Встроен | ✅ плагин | ❌ | ✅ CLI | ❌ |
| **GitHub Copilot** | ✅ | ✅ | ✅ | ❌ | ❌ |
| **Codeium** | ✅ | ✅ | ✅ | ❌ | ❌ |
| **Tabnine** | ✅ | ✅ | ✅ | ❌ | ❌ |
| **Continue** | ✅ | ✅ | ❌ | ❌ | ❌ |
| **OpenAI Codex** | ✅ Extension | ❌ | ❌ | ✅ CLI | ✅ Web |
| **Claude Code** | ❌ | ❌ | ❌ | ✅ | ❌ |
| **Aider** | ❌ | ❌ | ❌ | ✅ | ✅ встроен |

---

## Приватность и безопасность

| Инструмент | Код в облако | Локальные модели | Zero Retention | Корп. опции |
|-----------|:-----------:|:----------------:|:--------------:|:-----------:|
| **Cursor** | ✅ (Privacy Mode) | ❌ | ✅ | ✅ Business |
| **Windsurf** | ✅ | ❌ | ⚠️ | ✅ Enterprise |
| **Google Antigravity** | ✅ | ❌ | ⚠️ | ⚠️ В разработке |
| **Qoder** | ✅ (Alibaba) | ❌ | ⚠️ | ⚠️ В разработке |
| **GitHub Copilot** | ✅ | ❌ | ✅ Enterprise | ✅ Enterprise |
| **Codeium** | ✅ | ❌ | ✅ Enterprise | ✅ Enterprise |
| **Tabnine** | ⚠️ Basic | ✅ Enterprise | ✅ Enterprise | ✅ Enterprise |
| **Continue** | ⚠️ По модели | ✅ (Ollama) | ✅ локальные | ❌ |
| **OpenAI Codex** | ✅ | ❌ | ⚠️ | ✅ Business |
| **Claude Code** | ✅ | ❌ | ⚠️ | ⚠️ |
| **Aider** | ⚠️ По модели | ✅ (Ollama) | ✅ локальные | ❌ |

> ⚠️ **Примечание по Qoder:** Поскольку Qoder разработан Alibaba, ряд разработчиков выражает обоснованные опасения в отношении China's National Intelligence Law и передачи проприетарного кода. Для корпоративного использования рекомендуется изучить политику конфиденциальности перед внедрением.

---

## Матрица выбора

| Ситуация | Рекомендуемый инструмент |
|----------|-------------------------|
| Лучший AI-IDE «из коробки» | **Cursor** |
| Бесплатный неограниченный AI-помощник | **Codeium** |
| Хочу попробовать самый современный agent-first подход | **Google Antigravity** |
| Нужен асинхронный агент для сложных задач | **Qoder (Quest Mode)** |
| Работаю в JetBrains, менять не хочу | **GitHub Copilot** / **Codeium** |
| Важна полная приватность кода | **Tabnine Enterprise** / **Continue + Ollama** |
| Автоматизация через терминал, нужен Git-workflow | **Aider** |
| Нужен агент от OpenAI с параллельными задачами | **OpenAI Codex** |
| Хочу самый мощный CLI-агент | **Claude Code** |
| Open-source, минимальные расходы | **Aider + Ollama** / **Continue + Ollama** |

---

*← [Лонгрид](LONGREAD.md) | [Практический раздел →](PRACTICAL.md)*