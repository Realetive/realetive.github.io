# RomanGanin.ru

Персональный сайт Романа Ганина — руководителя проектов, разработчика, эксперта web-технологий.

Построен на [Eleventy](https://www.11ty.dev/) v3. Форк проекта [eleventy-base-blog](https://github.com/11ty/eleventy-base-blog).

## Команды

| Команда | Описание |
|---------|----------|
| `npm start` | Запуск dev-сервера с live reload |
| `npm run build` | Сборка статики в `_site/` |
| `npm run debug` | Сборка с отладочным выводом Eleventy |
| `npm run debugstart` | Dev-сервер с отладочным выводом |

## Структура проекта

- `content/` — контент (Markdown, Nunjucks)
- `_includes/layouts/` — шаблоны (base.njk → post.njk / home.njk)
- `_data/` — глобальные данные и схемы валидации
- `_config/filters.js` — кастомные фильтры Eleventy
- `css/` — стили, собираемые через `{% css %}` shortcode
- `public/` — статические ассеты, копируемые в выходной каталог

## Лицензия

[MIT](LICENSE)
