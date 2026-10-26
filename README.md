# Вики по 1С

Личная база знаний по **1С:Предприятие** — язык, конфигурации, администрирование, интеграции и практические рецепты.

**Читать онлайн:** https://andcheb.github.io/1c-articles/

## О проекте

Статьи пишутся в Markdown, сайт собирается генератором [MkDocs Material](https://squidfunk.github.io/mkdocs-material/): полнотекстовый поиск, теги, вкладки разделов, тёмная и светлая темы.

Каждый push в `main` автоматически пересобирает сайт и публикует его на GitHub Pages — workflow [.github/workflows/deploy.yml](.github/workflows/deploy.yml). Правила наполнения — в [CONTRIBUTING.md](CONTRIBUTING.md).

## Разделы

| Раздел | О чём |
|---|---|
| [Основы](https://andcheb.github.io/1c-articles/basics/) | платформа, режимы работы, базовые понятия |
| [Язык 1С](https://andcheb.github.io/1c-articles/language/) | синтаксис, типы, коллекции, запросы |
| [Конфигурации](https://andcheb.github.io/1c-articles/configuration/) | объекты метаданных, типовые конфигурации |
| [Администрирование](https://andcheb.github.io/1c-articles/admin/) | обслуживание баз, пользователи, резервные копии |
| [Интеграции](https://andcheb.github.io/1c-articles/integration/) | HTTP-сервисы, OData, SOAP, планы обмена |
| [Рецепты](https://andcheb.github.io/1c-articles/recipes/) | короткие решения типовых задач |

## Релизы

Версии фиксируются тегами `v*` на значимых изменениях.

| Версия | Дата | Изменения |
|---|---|---|
| v0.2.0 | 2026-10-26 | Правила оформления скриншотов, каталог `docs/assets` |
| v0.1.0 | 2026-10-26 | Первая публикация: каркас сайта, 6 разделов, автодеплой на GitHub Pages |
