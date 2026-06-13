# Frontend Mentor — Решение задания «Four card feature section»

Это моё решение задания [«Four card feature section» на Frontend Mentor](https://www.frontendmentor.io/challenges/four-card-feature-section-weK1eFYK). Задания Frontend Mentor помогают прокачать навыки вёрстки через реальные проекты.

## Содержание

- [Обзор](#обзор)
  - [Задача](#задача)
  - [Скриншот](#скриншот)
  - [Ссылки](#ссылки)
- [Мой процесс](#мой-процесс)
  - [Что использовалось](#что-использовалось)
  - [Что я узнал](#что-я-узнал)

## Обзор

### Задача

Пользователи должны:

- Видеть оптимальную раскладку страницы в зависимости от размера экрана устройства

### Скриншот

![](./design/desktop-preview.jpg)

### Ссылки

- URL живого сайта: [Ссылка на живой сайт](https://vimanshin.github.io/four-card-feature-section-master/)

## Мой процесс

### Что использовалось

- Семантическая разметка HTML5 (`header`, `main`, `section`, `article`, `footer`)
- SASS (SCSS) — partials, `@use`, переменные
- CSS custom properties (`:root`)
- Локальные шрифты через `@font-face` (Poppins)
- Flexbox — mobile-раскладка карточек
- CSS Grid — tablet и desktop (перестановка карточек через `grid-row` / `grid-column`)
- Mobile-first подход и медиа-запросы `min-width`
- SCSS-миксин `respond()` для breakpoints
- BEM-подобное именование классов (`intro__title`, `card--cyan`)
- Stylelint — проверка качества CSS

### Что я узнал

- Как строить проект по слоям: `abstracts` → `base` → `layout` → `components` — каждый файл отвечает за свою зону, а `main.scss` только собирает всё вместе.

- Mobile-first на практике: сначала одна колонка (Flexbox), потом tablet (Grid 2 колонки), затем desktop (Grid 3 колонки) — без изменения HTML, только через CSS и `:nth-child()`.

- Как переставлять карточки в сетке, когда порядок в HTML не совпадает с макетом: `grid-row`, `grid-column`, `align-self: center` для боковых карточек на desktop.

- Зачем на больших экранах сбрасывать tablet-стили (`width: 100%`, `justify-self: stretch`) — иначе старые правила «протекают» в новый breakpoint.

- Как подключать шрифты локально через `@font-face` и почему пути в `url()` считаются от скомпилированного `css/style.css`, а не от `.scss`.

- Как выносить дизайн-токены (цвета, отступы, breakpoints) в переменные и дублировать их в CSS custom properties для удобства в DevTools.