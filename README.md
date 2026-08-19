# Портфолио — Максим Герасимов, Junior DevOps / Infrastructure Engineer

Исходный код персонального сайта-портфолио.
Опубликовано: **[maximgerasimov1.github.io/portfolio](https://maximgerasimov1.github.io/portfolio/)**

Сайт показывает инженерную траекторию — от администрирования Linux и сетевого
стенда к контейнеризации, Kubernetes, CI/CD и наблюдаемости. У каждого проекта
отдельная страница по схеме «задача → что сделано → результат».

## Технически

Статический сайт без сборки и зависимостей: HTML и CSS, без JavaScript
и без внешних запросов — шрифты системные, схемы нарисованы инлайновым SVG.
Открывается из файловой системы так же, как с сервера.

```text
.
├── index.html                позиционирование, траектория, стек, контакты
├── projects/
│   ├── index.html            каталог проектов по инженерным слоям
│   └── <slug>.html           страница проекта; slug совпадает с именем
│                             каталога в репозитории с кодом
├── skills.html               стек со ссылками на проекты
├── about_me.html             биография, образование, сертификат
├── contacts.html             контакты и профили
├── resume/                   резюме в PDF и в виде веб-страницы
├── css/
│   ├── reset.css             сброс браузерных стилей
│   └── main.css              единственный файл стилей, импортирует reset
├── img/
├── favicon.svg
├── sitemap.xml
└── robots.txt
```

Точка входа — `index.html`. Стили подключаются одной строкой
`<link rel="stylesheet" href="./css/main.css">`; `main.css` первой строкой
импортирует `reset.css`. Других зависимостей нет.

## Локальный просмотр

```bash
git clone https://github.com/MaximGerasimov1/portfolio.git
cd portfolio
python -m http.server 8000   # либо просто открыть index.html в браузере
```

## Публикация

GitHub Pages, ветка `main`, корень репозитория. При добавлении или
переименовании страниц обновляйте `sitemap.xml` и канонические ссылки
`<link rel="canonical">` — они должны совпадать с фактическими путями.

## Связанные репозитории

| Репозиторий | Что там |
|---|---|
| [DevOps-Python-SQL](https://github.com/MaximGerasimov1/DevOps-Python-SQL) | инфраструктурные проекты, Python и SQL |
| [docker-nginx-proxy](https://github.com/MaximGerasimov1/docker-nginx-proxy) | приложение за обратным прокси в двух контейнерах |
| [c-cpp-projects](https://github.com/MaximGerasimov1/c-cpp-projects) | проекты на C и C++, курсовая на Qt |
| [php-web-projects](https://github.com/MaximGerasimov1/php-web-projects) | веб-приложения на PHP |

## Автор

Максим Герасимов · [GitHub](https://github.com/MaximGerasimov1) ·
[Telegram](https://t.me/gisellet3) · m.s.gerasimov@mail.ru
