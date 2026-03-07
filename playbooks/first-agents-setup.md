# Перший запуск агентів: практична конфігурація

Цей документ дає **готовий стартовий стек агентів** для команд, які тільки починають працювати з репозиторієм `agency-agents`.

## 1) Ціль стартового стеку

Запустити першу робочу схему за принципом:

1. Прийняти та декомпозувати запит.
2. Спроєктувати рішення.
3. Реалізувати зміни.
4. Перевірити якість і стабільність.
5. Зафіксувати результат у зрозумілому форматі.

## 2) Перші 5 агентів, які варто налаштувати

| Порядок | Агент | Файл | Роль у потоці |
|---|---|---|---|
| 1 | Project Manager Senior | `project-management/project-manager-senior.md` | Декомпозиція задач, scope, пріоритезація |
| 2 | UX Architect | `design/design-ux-architect.md` | Технічна UX-архітектура, принципи інтерфейсу |
| 3 | Senior Developer | `engineering/engineering-senior-developer.md` | Реалізація складної логіки та коду |
| 4 | API Tester / Evidence Collector | `testing/testing-api-tester.md`, `testing/testing-evidence-collector.md` | Функціональна і доказова валідація |
| 5 | Reality Checker | `testing/testing-reality-checker.md` | Фінальний quality gate перед релізом |

> Якщо у вас переважно UI-задачі, замініть Senior Developer на Frontend Developer (`engineering/engineering-frontend-developer.md`).

## 3) Стандартний workflow (MVP)

### Етап A — Intake
- Вхід: короткий бізнес-запит, обмеження, дедлайн.
- Виконавець: **Project Manager Senior**.
- Результат: backlog, критерії готовності (DoD), ризики.

### Етап B — Design / Architecture
- Вхід: backlog + критерії.
- Виконавець: **UX Architect**.
- Результат: технічна схема реалізації, правила UI/UX, список компонентів або модулів.

### Етап C — Build
- Вхід: architecture package.
- Виконавець: **Senior Developer** (або Frontend/Backend спеціалізований агент).
- Результат: імплементація по задачах, короткий changelog.

### Етап D — QA Loop
- Вхід: реалізовані задачі.
- Виконавці: **API Tester** + **Evidence Collector**.
- Результат: PASS/FAIL, артефакти перевірки, баг-репорти.

### Етап E — Release Gate
- Вхід: QA результати.
- Виконавець: **Reality Checker**.
- Результат: рішення `READY` або `NEEDS WORK` з чітким обґрунтуванням.

## 4) Мінімальні інструкції для старту (copypaste)

### 4.1 Інструкція для PM

```text
Ти Project Manager Senior. Отримай запит, побудуй backlog (epics/tasks), для кожної задачі дай acceptance criteria, залежності, ризики та пріоритет. Ніяких зайвих фіч поза scope.
```

### 4.2 Інструкція для архітектора

```text
Ти UX Architect. На базі backlog спроєктуй технічний UX-план: інформаційна архітектура, ключові потоки, стани UI, edge-cases, та handoff для розробника.
```

### 4.3 Інструкція для розробника

```text
Ти Senior Developer. Реалізуй задачі ітеритивно: 1 задача → локальна перевірка → короткий звіт. Якщо вимога неясна, спочатку сформулюй уточнення/припущення.
```

### 4.4 Інструкція для QA

```text
Ти API Tester + Evidence Collector. Перевір реалізацію відносно acceptance criteria. На кожен критерій дай evidence (лог/скрін/вихід тесту) і вердикт PASS/FAIL.
```

### 4.5 Інструкція для фінального гейту

```text
Ти Reality Checker. Зроби незалежну фінальну валідацію і винеси рішення READY або NEEDS WORK. За замовчуванням обирай NEEDS WORK, якщо доказів недостатньо.
```

## 5) Що додати одразу після першого запуску

1. Таблицю метрик: lead time, pass-rate, retry-rate.
2. Словник артефактів: де зберігаються backlog, архітектура, evidence.
3. Правило handoff: кожен етап завершується структурованим виходом (`input`, `output`, `risks`, `next_step`).
4. Postmortem-шаблон: що спрацювало/не спрацювало в агентному ланцюгу.

## 6) Рекомендація по масштабуванню

Після стабільного MVP-потоку додайте:
- `specialized/agents-orchestrator.md` для напівавтоматичної координації всього пайплайну.
- `testing/testing-workflow-optimizer.md` для оптимізації витрат часу між ролями.
- `support/support-analytics-reporter.md` для регулярних звітів по KPI.
