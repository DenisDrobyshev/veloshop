# VeloShop — витрина магазина велосипедов на Nuxt

[![Nuxt](https://img.shields.io/badge/Nuxt-2-00DC82?logo=nuxtdotjs&logoColor=white)](https://v2.nuxt.com/)
[![Vue](https://img.shields.io/badge/Vue-2-4FC08D?logo=vuedotjs&logoColor=white)](https://v2.vuejs.org/)
[![Sass](https://img.shields.io/badge/Sass-CC6699?logo=sass&logoColor=white)](https://sass-lang.com/)

Фронтенд интернет-магазина велосипедов на **Nuxt 2 / Vue 2**. Проект собран по компонентному принципу с продуманной шапкой сайта и единой SCSS-системой стилей.

## Возможности

- 🧩 **Компонентная шапка**: логотип, меню каталога, строка поиска, иконки аккаунта и входа, панель инструментов.
- 🦶 Переиспользуемый **footer** и общий layout (`layouts/default.vue`).
- 🎨 **Дизайн-система на SCSS**: переменные (`assets/scss/variables.scss`), z-index-шкала, подключение через `@nuxtjs/style-resources`.
- 🏠 Главная страница витрины (`pages/index.vue`).

## Структура

```
veloshop/
├── components/
│   ├── header/     # logo, catalog, search-bar, icon-account, icon-login, tools
│   └── footer/     # footer.vue
├── layouts/default.vue
├── pages/index.vue
├── assets/
│   ├── scss/       # variables.scss, _z-index.scss
│   └── js/const.js
└── nuxt.config.js
```

## Запуск

```bash
git clone https://github.com/DenisDrobyshev/veloshop.git
cd veloshop
npm install

npm run dev       # http://localhost:3000 (hot reload)
npm run build     # production-сборка
npm run generate  # статическая генерация
```

## Стек

`Nuxt 2` · `Vue 2` · `Sass/SCSS` · `@nuxtjs/style-resources`
