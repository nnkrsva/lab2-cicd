# lab2-cicd

Лабораторна робота №2 з дисципліни «Основи DevOps» — розширений конвеєр CI/CD у GitHub Actions.

| Workflow | Файл | Призначення |
|---|---|---|
| Production Pipeline | `.github/workflows/production-pipeline.yml` | test → build (ghcr.io) → staging → production |
| Matrix Build | `.github/workflows/matrix.yml` | 3 ОС × 3 версії Node.js, без Windows + Node 21 (8 завдань) |
| Reusable Deploy | `.github/workflows/deploy-template.yml` | reusable workflow (`workflow_call`) |
| Call Deploy | `.github/workflows/call-deploy.yml` | ручний виклик reusable workflow |
| Conditional Jobs | `.github/workflows/conditional.yml` | запуск backend/frontend лише за змін у відповідних каталогах |

Локальна перевірка: `npm ci && npm test && npm run lint`.
