# Наполнение вики

Практические правила: как добавлять статьи, скриншоты и проверять сборку локально.

## Окружение

Один раз после клонирования (PowerShell, из корня репозитория):

```powershell
py -m venv .venv
.venv\Scripts\python -m pip install -r requirements.txt
```

## Команды

| Действие | Команда |
|---|---|
| Локальный просмотр | `.venv\Scripts\mkdocs serve` → http://127.0.0.1:8000 |
| Разовая сборка | `.venv\Scripts\mkdocs build` |

## Как добавить статью

1. Скопируй `templates/article-template.md` в нужный раздел `docs/<раздел>/` под именем статьи (например, `docs/recipes/http-request.md`).
2. Заполни заголовок и текст; теги из метаданных `tags` автоматически попадают на страницу тегов.
3. Если раздел новый — добавь пункт в `nav` в `mkdocs.yml`.
4. Проверь локально: `.venv\Scripts\mkdocs serve`.
5. Коммит и `git push` — сайт обновится автоматически через 1–2 минуты (GitHub Actions).

## Скриншоты и картинки

1. Клади картинки в `docs/assets/<раздел>/`, имена латиницей без пробелов: `docs/assets/recipes/http-request.png`.
2. Вставляй в статью относительной ссылкой. Из `docs/recipes/article.md` путь к картинке:
   `![Описание скрина](../assets/recipes/http-request.png)`
3. Размер задаётся фигурными скобками: `![Скрин](../assets/recipes/http-request.png){ width="600" }`.
4. Тяжёлые скрины жми перед коммитом: PNG/JPG желательно до 300–500 КБ. Скрины делай через `Win+Shift+S`.

## Релиз

Значимое изменение (новый раздел, крупная порция статей, смена движка) — тег:

```powershell
git tag -a vX.Y.Z -m "Краткое описание"
git push --tags
```

и строка в таблице «Релизы» в `README.md`.

## Структура

```
docs/            — статьи (Markdown), попадают на сайт
  basics/        — Основы
  language/      — Язык 1С
  configuration/ — Конфигурации
  admin/         — Администрирование
  integration/   — Интеграции
  recipes/       — Рецепты
  assets/        — картинки для статей
templates/       — шаблоны (на сайт не попадают)
.github/workflows/deploy.yml — автодеплой на GitHub Pages
```
