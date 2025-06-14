# **Уровень A1 (Начальный)**

_Основные концепции и базовые элементы_

> [Home](../readme.md)

---

## 1. **Введение в HTML и CSS**

### [1.1. **Структура HTML-документа**](./1.1.%20Структура%20HTML-документа.md)

-   Структура HTML-документа
    -   `<!DOCTYPE html>`, `<html>`, `<head>`, `<body>`
-   Основные теги
    -   `<h1>`-`<h6>`, `<p>`, `<a>`, `<img>`, `<ul>`, `<ol>`, `<li>`, `<div>`, `<span>`...
-   Теги форматирования текста
    -   `<b>`, `<i>`, `<s>`, `<u>`, `<tt>`, `<sup>`, `<sub>`, `<small>`...
-   Атрибуты тегов
    -   `id`, `class`, `href`, `src`, `alt`, `title`
-   Работа с таблицами
    -   `<table>`, `<tr>`, `<td>`, `<th>`, `<caption>`
-   Введение в семантическую верстку, использование тегов по назначению

### [1.2. **Подключение CSS, селекторы и свойства**](./1.2.%20Подключение%20CSS,%20селекторы%20и%20свойства.md)

-   Подключение CSS к HTML
    -   каскадность (cascade)
    -   внешние файлы CSS
    -   внутренние стили с использованием тега `<style>`
    -   встроенные стили (Inline Styles)
    -   директива `!important`
-   Базовые селекторы
    -   `*`, `tag`, `.class`, `#id`
    -   специфичность
-   Наследование (inheritance)
    -   `inherit`, `initial`, `unset`
-   Правила нейминга идентификатора
    -   допустимые символы и структура идентификатора
    -   практические рекомендации по неймингу
-   Единицы измерения и цветовые форматы
-   Подключение шрифтов и основные свойства для текста
    -   подключение шрифтов
        -   `@font-face`, `Google Fonts`, `font-family`
    -   свойства шрифтов
        -   `color`, `font-size`, `text-align`, `text-decoration`, `line-height`, `font-family`, `font-weight`, `letter-spacing`, `font`
-   Базовая работа с фоновыми изображениями
    -   `background-color`, `background-image`, `background-size`, `background-repeat`, `background-position`, `background-attachment`, `background`

### [1.3. **Основы верстки**](./1.3.%20Основы%20верстки.md)

-   Основы блочной модели
    -   `width`, `height`, `margin`, `padding`, `border`
    -   `box-sizing`
-   Основы позиционирования
    -   `display` (inline, block, table)
    -   `position` (static, relative, absolute, fixed)
    -   `top`, `right`, `bottom`, `left`, `z-index`
-   Введение в адаптивность
    -   `float`, `clear`, `overflow`
    -   простые макеты с использованием `float` и `clear`

---

## 2. **Основы JavaScript**

### [2.1. **Что такое JavaScript**](./2.1.%20Что%20такое%20JavaScript.md)

-   Стандарт ECMAScript (ES)
    -   история ECMAScript
    -   работа с современными стандартами
-   Подключение JavaScript к HTML
    -   внешний JavaScript
    -   атрибуты `<script>`

### [2.2. **Переменные и типы данных**](./2.2.%20Переменные%20и%20типы%20данных.md)

-   Синтаксис
    -   инструкции
    -   точка с запятой
    -   комментарии
    -   синтаксический сахар
-   Переменные
    -   `let`, `const`, `var`
    -   правила нейминга переменных
    -   константы
    -   семантические названия переменных
-   Строгий режим `strict mode`
    -   способы включения строгого режима
    -   основные изменения и ограничения в строгом режиме
-   Область видимости
-   Hoisting (поднятие)
-   Типы данных
    -   числа, строки, булевы значения, `null`, `undefined`
-   Оператор `typeof`

### 2.3. **Операторы**

-   Операторы: унарные, бинарные, арифметические, логические, присваивания, сравнения
-   Простые операции: `+`, `-`, `*`, `/`, `%`, `**`
-   Базовые операторы сравнения: `==`, `!=`, `===`, `!==`, `>`, `<`
-   Комментарии в коде: `//`, `/* */`

### 2.4. **Условия и циклы**

-   Условные операторы `if`, `else`, `else if`, `switch`
-   Тернарный оператор

### 2.5. **Проекты для закрепления**

-   Написать скрипт на JavaScript, который выводит приветствие в консоль.

---

## 3. **Функции и массивы**

### [3.1. **Функции**](./3.1.%20Функции.md)

-   Объявление и вызов функций
    -   Что такое функция?
    -   Объявление функций: Function Declaration, Function Expression
-   Аргументы, параметры и возвращаемые значения
    -   Передача аргументов
    -   Rest параметры
    -   Возвращаемые значения
    -   Псевдомассив `arguments` в функциях
    -   Примеры реального использования в коде
-   Практика

### 3.2. **Массивы**

-   Создание массивов
-   Доступ к элементам массива
-   Основные методы массивов
    -   `push`, `pop`, `shift`, `unshift`, `concat`

---

## 4. **Объекты и модули**

### 4.1. **Объекты**

-   Создание объектов
-   Доступ к свойствам
    -   точечная нотация и квадратные скобки
    -   удаление свойств

### 4.2. **Модули в JavaScript**

-   Именованный и стандартный экспорт
-   Импорт модулей

---

## 5. **Node.js и работа с пакетами**

### 5.1. **Введение в Node.js**

-   Что такое Node.js
-   Установка Node.js и npm/pnpm/yarn
-   Основы работы с REPL (Read-Eval-Print Loop)
-   Запуск простого скрипта на Node.js
-   Чтение и вывод данных в терминал `process.stdin`, `process.stdout`

### 5.2. **Модули в Node**

-   Модули `require`, `module.exports`
-   Разница между CommonJS и ES-модулями
-   Встроенные модули `fs`, `path`
-   Создание и экспорт собственных модулей
-   Импорт модулей

### 5.3. **Работа с npm**

-   Установка и использование пакетов
-   Управление пакетами: `npm init`, `package.json`, `npm install`
-   Понимание `package.json` и `package-lock.json`.
-   Установка глобальных пакетов (`npm install -g`)
-   `npm scripts` — запуск команд через `package.json`
-   Создание собственного пакета

---

## 6. **DOM и работа с элементами**

### 6.1. **Работа с консолью**

-   Глобальные объекты `global` и `window`
-   Вывод данных `console.log`, `console.error`, `console.warn`
-   Модальные окна в браузере `alert`, `prompt`, `confirm`

### 6.2. **Введение в DOM**

-   Что такое DOM? Как браузер видит HTML-документ
-   Основные понятия: элементы, узлы, атрибуты
-   Навигация по DOM (дочерние, родительские и соседние узлы)

### 6.3. **Работа с элементами DOM**

-   Поиск элементов
    -   `getElementById`, `getElementsByClassName`, `getElementsByTagName`, `querySelector`, `querySelectorAll`
-   Изменение содержимого
    -   `innerHTML`, `textContent`
-   Работа с атрибутами
    -   `getAttribute`, `setAttribute`, `hasAttribute`, `removeAttribute`
-   Изменение `data-атрибутов`

---

## 7. **Начальная работа с Git и GitHub**

### 7.1. **Введение в Git**

-   Что такое система контроля версий? Зачем нужен Git?
-   Установка Git на различных платформах
-   Настройка глобальных и локальных конфигураций (`git config`)
    -   `git config --global user.name`, `git config --global user.email`
-   Использование `.gitignore`
-   `git init` - инициализация репозитория
-   `git status` - просмотр статуса репозитория
-   `git add` - добавление изменений в индекс
-   `git commit` - фиксация изменений

### 7.2. **Журнал коммитов и откат изменений**

-   Просмотр истории коммитов (`git log`)
-   Восстановление файлов и коммитов (`git checkout`, `git reset`)
-   Переключение на предыдущий коммит: `git checkout <хэш_коммита>`
-   Отмена изменений в рабочей директории: `git checkout -- <файл>`

### 7.3. **Создание и управление удаленными репозиториями**

-   Введение в GitHub
-   Создание удаленного репозитория на GitHub
-   Связывание локального репозитория с удаленным (`git remote add`)
-   Отправка изменений в удаленный репозиторий (`git push`)

---

## 8. **Проекты для закрепления материала:**

-   "Hello, World!": вывод текста на страницу
-   "Вывод текста": вывод на странице текста введенного пользователем
-   "Калькулятор": простой калькулятор складывающий значения введенные пользователем и выводящий результат на странице
-   "Простой статический веб-сайт": Создание простого веб-сайта с несколькими страницами и базовой стилизацией, управление его версиями с помощью Git. Размещение его на GitHub.
    -   Создать простую страницу "О себе" с использованием базовых тегов и стилей.
    -   Создать страницу "Контакты" с формой обратной связи.
    -   "Визитка": создание простой визитки с информацией о себе.
    -   "Персональный блог": создание блога с несколькими страницами.
    -   "Новостной сайт": создание макета новостного сайта.
    -   Одностраничная визитка с изображением, текстом и кнопкой (например, резюме или визитка фрилансера). Основной фокус – правильная структура HTML и базовые стили CSS.
