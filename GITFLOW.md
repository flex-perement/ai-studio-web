# GitFlow — Как работать с кодом

## Ветки

| Ветка | Назначение | Пример |
|-------|------------|--------|
| `main` | production | — |
| `develop` | разработка | — |
| `feature/*` | новая функция | `feature/improve-landing` |
| `hotfix/*` | срочный фикс | `hotfix/fix-typo` |
| `release/*` | подготовка к релизу | `release/v1.0` |

## Процесс

```
1. Создай ветку от develop
   git checkout develop
   git pull
   git checkout -b feature/название

2. Работай над задачей
   git add .
   git commit -m "feat: add new component"

3. Создай Pull Request
   → GitHub → Compare & PR
   → CodeRabbit автоматически проведёт review

4. Исправь замечания CodeRabbit
   → Новые коммиты в ветку
   → CodeRabbit перепроверит

5. После approve → Merge в develop
```

## Сообщения коммитов

```
feat: новая функция
fix: исправление бага  
docs: документация
refactor: рефакторинг
test: тесты
chore: инфраструктура
```

## CodeRabbit Review

- Review запускается автоматически при создании PR
- Исправь критические ошибки
- Опционально: мелкие suggestions
- После approve → Merge

## Пример

```bash
git checkout develop
git checkout -b feature/add-contact-form
# ... работа ...
git add .
git commit -m "feat: add contact form with validation"
git push -u origin feature/add-contact-form
# → Создай PR на GitHub
```
