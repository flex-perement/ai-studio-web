# 🛠️ Quality Tools — Инструкция подключения

## 1. CodeRabbit AI Code Review

**Что делает:** Автоматический AI-ревью кода при каждом PR

**Подключение:**
1. Перейди на https://coderabbit.ai
2. Нажми "Add to GitHub"
3. Выбери репозиторий `flex-perement/ai-studio-web`
4. Настрой правила в `coderabbit.yaml`

**Что видишь:** Комментарии к PR с suggestions по улучшению кода

---

## 2. Lighthouse CI

**Что делает:** Авто-аудит при каждом пуше (performance, accessibility, SEO, best practices)

**Подключение:**
1. Перейди на https://github.com/treosh/lighthouse-ci-action
2. Добавь токен GitHub в Secrets: `LHCI_GITHUB_APP_TOKEN`
3. Workflow уже настроен в `.github/workflows/lighthouse.yml`

**Метрики:**
- Performance > 80
- Accessibility > 90
- Best Practices > 90
- SEO > 80

---

## 3. Mintlify Documentation

**Что делает:** Авто-документация из markdown файлов

**Подключение:**
1. Перейди на https://mintlify.com
2. Нажми "Start Documentation"
3. Подключи репозиторий `flex-perement/ai-studio-web`
4. Документация будет на https://ai-studio.mintlify.com

**Редактирование:** Правь файлы в `docs/`

---

## Как работает сейчас

```
Push → CodeRabbit Review + Lighthouse Audit → Report → Fix → Merge
```

## Статус

| Инструмент | Конфиг | Подключение |
|------------|---------|-------------|
| CodeRabbit | ✅ | 🔴 Требуется ручная активация |
| Lighthouse | ✅ | 🔴 Требуется токен |
| Mintlify | ✅ | 🔴 Требуется подключение |

---

## Запуск Lighthouse локально

```bash
npm install -g @lhci/cli
lhci autorun
```
