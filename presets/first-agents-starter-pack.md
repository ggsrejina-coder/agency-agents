# First Agents Starter Pack

Готові промпти для запуску першої агентної команди з цього репозиторію.

## Starter Team A (Web MVP)

- `project-management/project-manager-senior.md`
- `specialized/agents-orchestrator.md`
- `engineering/engineering-frontend-developer.md`
- `testing/testing-evidence-collector.md`
- `testing/testing-reality-checker.md`

## Sequence

1. PM: створює task list.
2. Orchestrator: запускає delivery loop по задачах.
3. Dev: реалізує 1 задачу за цикл.
4. Evidence QA: PASS/FAIL на 1 задачу.
5. Reality Checker: фінальний gate після всіх PASS.

## Copy-paste kickoff prompt

```text
Працюємо в режимі агентної команди.
Склад команди:
1) Project Manager (Senior)
2) Agents Orchestrator
3) Frontend Developer
4) EvidenceQA
5) Reality Checker

Правила:
- Спочатку PM готує tasklist із P0/P1/P2 + acceptance criteria.
- Далі orchestrator веде цикл по 1 задачі: Dev -> Evidence QA -> рішення.
- Без PASS поточної задачі перехід далі заборонено.
- Максимум 3 retry на задачу.
- Після завершення всіх P0/P1 — запустити Reality Checker для release verdict.

Почніть зі створення tasklist.
```

## Starter Team B (API/Platform)

Заміна в Team A:
- замість `engineering-frontend-developer` використати `engineering-backend-architect`.

## Starter Team C (Mobile)

Заміна в Team A:
- замість `engineering-frontend-developer` використати `engineering-mobile-app-builder`.

