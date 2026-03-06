---
name: git-workflow
description: Использовать при любых операциях с git: коммит, ветка, пуш, история. Алгоритм работы с репозиторием Империи по стандарту Conventional Commits.
---

# GIT-WORKFLOW: Алгоритм работы с репозиторием

Грязный коммит — грязная история.

---

## Стандарт сообщений: Conventional Commits

```
<type>(<scope>): <description>

[тело коммита (опционально)]
[футер (опционально, для breaking changes или ссылок)]
```

### Типы (`type`)

| Тип        | Когда использовать                             |
| ---------- | ---------------------------------------------- |
| `feat`     | Новая функциональность                         |
| `fix`      | Исправление бага                               |
| `docs`     | Только документация                            |
| `chore`    | Служебное: конфиг, зависимости, правила агента |
| `refactor` | Рефакторинг без изменения поведения            |
| `test`     | Тесты                                          |
| `style`    | Форматирование, пробелы (без логики)           |
| `perf`     | Оптимизация производительности                 |
| `ci`       | CI/CD конфигурация                             |
| `revert`   | Откат коммита                                  |

### Скоупы (`scope`) проекта

| Скоуп     | Что покрывает                             |
| --------- | ----------------------------------------- |
| `scraper` | `src/scraper/`                            |
| `api`     | `src/api/`                                |
| `mcp`     | MCP сервер                                |
| `agents`  | `.agents/` (rules, skills, workflows)     |
| `archive` | `src/garden/goddess_archive/`             |
| `garden`  | `src/garden/` в целом                     |
| `docs`    | `docs/`                                   |
| `config`  | `pyproject.toml`, `.gitignore`, `uv.lock` |

### Примеры корректных коммитов

```
feat(api): add /search endpoint for full-text doc search

fix(scraper): handle 404 responses without crashing

chore(agents): update person-core.md with new skill reference

docs(archive): add 2026-03-05 goddess wisdom entry

refactor(scraper): extract fetcher logic into separate module
```

---

## Алгоритм атомарного коммита

**Принцип:** Один коммит = одно логическое изменение.

### Шаг 1 — Проверка статуса

```bash
git status
git diff
```

Понять: что изменилось и почему.

### Шаг 2 — Выбор файлов для стейджинга

```bash
# Конкретные файлы — предпочтительно
git add path/to/file.py path/to/other.py

# Частичный стейджинг (интерактивный)
git add -p

# ВСЁ — только если все изменения принадлежат ОДНОМУ коммиту
git add .
```

### Шаг 3 — Написание сообщения коммита

1. Тип — из таблицы выше
2. Скоуп — из таблицы выше (если применимо)
3. Описание — в настоящем времени, по-английски, кратко
4. Тело (если нужно) — ЧТО и ПОЧЕМУ, через пустую строку

### Шаг 4 — Коммит

```bash
git commit -m "type(scope): short description"

# Или с телом
git commit -m "type(scope): short description

- Детальное объяснение что сделано
- Почему это сделано
- Что изменилось в поведении"
```

### Шаг 5 — Верификация

```bash
git log --oneline -5   # проверить историю
git show HEAD          # проверить последний коммит
```

---

## Стратегия веток

```
main          ← стабильная продакшн ветка (GitHub)
  └─ feature/<name>   ← новая функциональность
  └─ fix/<name>       ← исправление бага
  └─ chore/<name>     ← служебные изменения
```

**Правила:**
- `main` всегда в рабочем состоянии
- Работа ведётся в ветках, в `main` — только через merge/PR
- Имена веток: строчные буквы, дефисы (`feature/goddess-archive`)

### Создание ветки

```bash
git checkout -b feature/<name>
# работа, коммиты...
git push -u origin feature/<name>
```

---

## Синхронизация с GitHub

```bash
# Первый пуш ветки
git push -u origin <branch-name>

# Обычный пуш
git push

# Получить изменения
git pull --rebase origin main
```

---

## Чеклист перед каждым пушем

- [ ] `git status` — нет случайных файлов
- [ ] `git log --oneline -5` — история читаемая и атомарная
- [ ] Нет `*.pyc`, `archive.db`, `.venv` в коммитах (проверить `.gitignore`)
- [ ] Каждый коммит описывает ОДНО изменение
- [ ] Сообщения по Conventional Commits

---

## Полезные команды

```bash
# История с деревом веток
git log --oneline --graph --all

# Что в последнем коммите
git show HEAD

# Отменить последний коммит (сохранив изменения)
git reset --soft HEAD~1

# Исправить сообщение последнего коммита
git commit --amend -m "новое сообщение"

# Размер репозитория
git count-objects -vH
```
