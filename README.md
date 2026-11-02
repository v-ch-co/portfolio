# Portfolio — Егор Бабушкин

Статический сайт-портфолио: один файл `index.html` (стили, скрипты, изображения и шрифт встроены), без сборки и зависимостей.

Страницы открываются внутри одного документа по хэшу адреса:

- `/` — главная
- `/#/nms` — NMS «ЦИСУСС»
- `/#/handifox` — HandiFox Customer Portal
- `/#/street-style` — Street Style

## Публикация

Достаточно положить `index.html` в корень любого статического хостинга (nginx, Apache, GitHub Pages, Netlify, Cloudflare Pages).

Пример для nginx:

```nginx
server {
    server_name example.com;
    root /var/www/portfolio;
    index index.html;
}
```

## Что поправить перед публикацией

- В проекте Street Style ссылка «открыть сервис» ведёт на артефакт в Claude. После переноса сервиса на свой адрес замените её.
- Заголовок и описание страницы (`<title>`, `<meta>`) проверьте под свой домен.
