# 3. Фронтенд

## **Уровень A1 - Начальный**

### **1. Введение в DOM**

- Что такое DOM? Как браузер видит HTML-документ.
- Основные понятия: элементы, узлы, атрибуты
- Навигация по DOM (дочерние, родительские и соседние узлы)

### **2. Работа с элементами DOM**

- Поиск элементов
  - `getElementById`, `getElementsByClassName`, `getElementsByTagName`, `querySelector`, `querySelectorAll`
- Изменение содержимого
  - `innerHTML`, `textContent`
- Работа с атрибутами
  - `getAttribute`, `setAttribute`, `hasAttribute`, `removeAttribute`
- Изменение `data-атрибутов`.

### **3. Работа с консолью**

- Глобальные объекты `global` и `window`
- Вывод данных `console.log`, `console.error`, `console.warn`
- Модальные окна в браузере `alert`, `prompt`, `confirm`
- Чтение и вывод данных в терминал `process.stdin`, `process.stdout`

## **Уровень A2 - Базовый**

### **1. Манипуляции с DOM**

- Создание новых элементов `document.createElement`
- Добавление элементов в DOM `appendChild`, `insertBefore`, `append`, `prepend`
- Удаление элементов `removeChild`, `remove`
- Клонирование элементов `cloneNode`
- Работа с родительскими и дочерними элементами
  - `parentElement`, `children`, `firstElementChild`, `lastElementChild`
  - `parentNode`, `childNodes`, `firstChild`, `lastChild`, `nextSibling`, `previousSibling`.

### **2. Работа с событиями в браузере**

- Введение в события
- Назначение обработчиков событий
  - `addEventListener`, `removeEventListener`
  - `this` в обработчиках событий
- Обработчики событий для различных типов событий
  - `click`, `mouseover`, `mouseout`, `keydown`, `keyup`, `load`, `DOMContentLoaded`, `submit`

### **3. Стилевые изменения элементов**

- Изменение стилей через `element.style`
- Работа с классами
  - `classList.add`, `classList.remove`, `classList.toggle`, `classList.contains`

## **Уровень B1 - Средний**

### **1. Продвинутая работа с событиями**

- Объект события: `event.target`, `event.type`, `event.preventDefault()`, `event.stopPropagation()`.
- Всплытие и погружение событий
- Делегирование событий (`event.target`).
- Предотвращение поведения по умолчанию (`preventDefault`)
- Остановка распространения событий (`stopPropagation`)

### **2. Формы и валидация**

- Доступ к элементам формы
- Получение значений полей формы: `input.value`, `select.value`, `textarea.value`.
- Работа с `textarea`, `checkbox`, `radio`, `select`.
- Простая валидация формы
- Отправка данных на сервер
- Основы `fetch` для простых GET-запросов.

### **3. Локальное хранилище**

- Работа с `cookies`
- Сохранение данных в `localStorage`
- Сохранение данных в `sessionStorage`
- Извлечение и удаление данных из хранилища
- Разница между `localStorage` и `sessionStorage`.
- Основы работы с `history.pushState()` (навигация без перезагрузки).

### **4. Инструменты разработчика Developer Tools**

- Отладка кода с помощью `node debug` или `chrome://inspect`
- Профилирование производительности

### **5. Анимации и таймеры**

- Использование `setTimeout`, `setInterval`.
- Простые анимации через `requestAnimationFrame`.

## **Уровень B2 - Продвинутый базовый**

### **1. Модификация структуры DOM**

- Создание сложных структур DOM
- Работа с шаблонами (`template` элемент)
- Динамическое изменение DOM на основе загруженных данных.
- Использование `MutationObserver` для отслеживания изменений в DOM.
- Работа с `DocumentFragment` для оптимизации вставки элементов.
- Использование `Shadow DOM` для изоляции компонентов.
- Основы работы с `IntersectionObserver` (ленивая загрузка изображений).
- Работа с `Template` и `Slot`.
- Создание кастомных элементов (`customElements.define()`).
- Навигация по истории браузера (`window.history`).

### **2. Работа с таблицами и списками**

- Создание и модификация таблиц
- Создание и модификация списков

### **3. События**

- Кастомные события: `CustomEvent`, `dispatchEvent`.
- Работа с `EventTarget`.

### **4. Работа с мультимедиа**

- Анимация через `CSS animations` и `JavaScript`.
- Использование `Clipboard API` (копирование в буфер обмена).
- Работа с `Canvas` для рисования простых фигур
- Работа с `requestAnimationFrame()` для плавных анимаций.
- Воспроизведение аудио и видео (`<audio>`, `<video>`, методы `play`, `pause`)
- Использование `speechSynthesis` для работы с голосом.
- Использование `Media API` (например, `getUserMedia`)

### **5. Кроссбраузерность (Частота использования: Средняя)**

- Проверка совместимости в разных браузерах.
- Использование префиксов.

### **6. Продвинутая работа с анимациями**

- Анимации с использованием JavaScript и CSS
- Создание сложных анимаций с использованием библиотек (например, GSAP)

## **Уровень C1 - Продвинутый**

### **1. Использование API браузера**

- `Geolocation API`
  - Работа с `navigator.geolocation` (получение координат).
- `File API` для работы с файловой системой
- Использование `FileReader` для чтения файлов.
- Работа с `Blob` и `File` API.
- `Streams API`

### **2. Работа с веб-API**

- Работа с `WebRTC` для видео- и аудиосвязи.
- Использование `Web Audio API` для обработки звука.
- Работа с `IndexedDB` для сложных хранилищ данных.

### **3. Драг-н-дроп**

- Использование `Drag and Drop API`.

### **4. Работа с графикой**

- Продвинутое использование `Canvas` и `WebGL`.
- SVG (Scalable Vector Graphics)
- Web Animations API
  - создание сложных анимаций
- Intersection Observer API
  - отслеживание пересечения элементов с областью просмотра

## **Уровень C2 - Экспертный**

### **1. Работа с DOM**

- Использование `Custom Elements` и `Web Components`.
- Работа с `MutationObserver` для сложных сценариев.

### **2. Продвинутые Web API**

- `WebSockets` для реального времени
- `Service Workers` для поддержки `PWA` (Прогрессивных веб-приложений)
- `WebAssembly` для высокопроизводительных приложений
- Использование `WebRTC` (видеозвонки без серверов).
- Работа с `Credential Management API`.
- Обмен данными с Bluetooth (`Web Bluetooth API`).
- Доступ к USB (`WebUSB API`).
- Использование `Gamepad API` (геймпады в браузере).
- Работа с `WebGPU` (рендеринг на GPU в браузере).
- Работа с `WebXR` для виртуальной и дополненной реальности.
- Использование `Payment Request API` для платежей.

### **3. Экспериментальные API**

- Использование новых и экспериментальных API, таких как `WebGPU`, `WebHID`, `WebNFC`.
