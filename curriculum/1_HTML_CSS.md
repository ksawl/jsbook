# HTML & CSS

## **Уровень A1 - Начальный**

### **1. Введение в HTML**

- Структура HTML-документа: `<!DOCTYPE html>`, `<html>`, `<head>`, `<body>`.
- Атрибуты тегов: `id`, `class`, `href`, `src`, `alt`, `title`.
- Основные теги: `<h1>`-`<h6>`, `<p>`, `<a>`, `<img>`, `<ul>`, `<ol>`, `<li>`, `<div>`, `<span>`.
- Работа с таблицами: `<table>`, `<tr>`, `<td>`, `<th>`, `<caption>`.
- Семантическая верстка: использование тегов по назначению.

### **2. Введение в CSS**

- Подключение CSS к HTML (встроенные стили, `<style>`, внешний файл `.css`)
- Базовые селекторы (`*`, `tag`, `.class`, `#id`)
- Работа со шрифтами (`@font-face`, `Google Fonts`, `font-family`)
- Основные свойства для текста
  - `color`, `font-size`, `text-align`, `text-decoration`, `line-height`, `font-family`, `font-weight`, `letter-spacing`
- Базовая работа с фоновыми изображениями
  - `background-color`, `background-image`, `background-size`, `background-repeat`
- Основы блочной модели
  - `width`, `height`, `margin`, `padding`, `border`
- Основы позиционирования
  - `display` (inline, block), `position` (static, relative)
  - `position`, `top`, `right`, `bottom`, `left`.
- Основные стили (цвета, шрифты, размеры)
- Каскадность и наследование

### **3. Базовая верстка:**

- Блочная модель (Box Model).
  - `display`, `float`, `clear`, `overflow`.
- Позиционирование: `static`, `relative`, `absolute`, `fixed`.
- Простые макеты с использованием `float` и `clear`.

---

## **Уровень A2 - Базовый**

### **1. Продвинутые HTML-теги**

- Мета-теги: `<meta>`, `<link rel="icon">`.
- Семантические теги
  - `<header>`, `<footer>`, `<nav>`, `<section>`, `<article>`, `<figure>`, `<figcaption>`
- Семантические теги для SEO
  - `<main>`, `<aside>`, `<time>`, `<mark>`
- Основы работы с медиа
  - `<audio>`, `<video>`, `controls`, `autoplay`, `<iframe>`, `<embed>`, `<object>`
- Атрибуты `data-*` и их использование
- Основы работы с SVG
- HTML-сущности `&lt;`, `&gt;`...

### **2. Сложные селекторы CSS**

- Сложные селекторы
  - cелекторы атрибутов `[attr]`
  - комбинаторы `,`, ` `, `+`. `>`, `~`
- Расширенные селекторы
  - `nth-child`, `nth-of-type`, `first-child`, `last-child`
- Псевдоклассы и псевдоэлементы
  - `hover`, `focus`, `before`, `after`
- Адаптивные размеры блока
  - `max-width`, `min-width`, `max-height`, `min-height`
  - `max-content`, `min-content`, `fit-content`
- Границы и тени
  - `border-radius`, `border-collapse`, `border-spacing`
  - `box-shadow`, `text-shadow`
- Градиенты (`linear-gradient`, `radial-gradient`)
- Flexbox
  - `display: flex`, `flex-direction`, `justify-content`, `align-items`, `flex-grow`, `flex-shrink`.
- Анимации
  - `transition`, `transform: scale, rotate`

### **3. Адаптивная верстка:**

- Медиа-запросы: `@media`.
- Создание адаптивных макетов
- Подход Mobile First.

---

## **Уровень B1 - Средний**

### **1. HTML**

- Использование `<template>`, `<picture>`, `<source>` для адаптивных изображений
- Группировка контента: `<figure>`, `<figcaption>`, `<details>`, `<summary>`

### **2. Работа с формами**

- Создание форм: `<form>`, `<input>`, `<button>`, `<label>`, `<textarea>`, `<select>`, `<option>`.
- Формы: валидация, атрибуты `required`, `pattern`, `min`, `max`.
- Работа с кастомными элементами форм

### **3. CSS**

- Псевдоклассы `:not()`, `:empty`, `:checked`
- Grid Layout: `display: grid`, `grid-template-columns`, `grid-template-rows`, `grid-gap`, `grid-area`.

### **4. Продвинутая анимация и переходы**

- Анимация с использованием CSS `@keyframes`, `animation`, `animation-delay`
- Создание сложных переходов `transition`
- Переменные: `--variable-name`, `var()`.

### **5. Препроцессоры**

- Основы SASS/SCSS: переменные, вложенности, миксины, импорты.
- Компиляция SASS/SCSS в CSS.
- Автоматизация сборки: Gulp, Webpack.

### **6. Интеграция UI-китов и библиотек**

- Знакомство с Bootstrap: сетка, компоненты, утилиты.
- Использование готовых компонентов: кнопки, карточки, навигация.
- Создание макетов с использованием UI-китов

---

## **Уровень B2 - Продвинутый базовый**

### **1. Продвинутая работа с HTML**

- Оптимизация загрузки контента (`loading="lazy"`, `async`, `defer`)
- Оптимизированные форматы изображений (`WebP`, `AVIF`)
- Использование iframe, взаимодействие с картами (Google Maps API, OpenStreetMap)
- Работа с мета-тегами для SEO: `<title>`, `<meta name="description">`, `<meta name="keywords">`.
- Микроразметка: Schema.org, Open Graph.
- Доступность (ARIA-атрибуты)

### **2. Продвинутые техники CSS**

- Grid + Flexbox (гибридные макеты)
- CSS-методологии (ITCSS, OOCSS)
- CSS-анимации высокого уровня (`scroll-behavior`, `clip-path`, `filter`)
- Адаптивная верстка без медиазапросов (Fluid Layout, `clamp()`, `min()`, `max()`)
- Адаптивный дизайн: media queries, viewport.
- Селекторы: псевдоклассы, псевдоэлементы, комбинаторы.

### **3. Препроцессоры**

- Продвинутые техники SASS/SCSS: функции, циклы, условия.
- Использование PostCSS для оптимизации
- Использование PostCSS для автоматизации задач.

### **4. Проектирование и создание UI-компонентов**

- Работа с Material-UI или Tailwind CSS.
- Создание и стилизация кастомных UI-компонентов
- Использование современных CSS-техник для создания компонентов
- **Figma to HTML** – вёрстка по макетам из Figma

### **5. Методологии:**

- БЭМ (Блок, Элемент, Модификатор).
- Atomic Design.
