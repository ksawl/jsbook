# **8. Проекты для закрепления материала**

## Проект "Hello, World!"

Создайте простую HTML страницу с JavaScript, который выводит приветствие.

### Требования

- HTML страница с базовой структурой
- JavaScript вывод в консоль и на страницу
- Интерактивность через `prompt()`

```html
<!DOCTYPE html>
<html lang="ru">
  <head>
    <meta charset="UTF-8" />
    <title>Hello World</title>
  </head>
  <body>
    <h1>Мой первый JavaScript</h1>
    <button onclick="sayHello()">Поприветствовать</button>
    <script>
      function sayHello() {
        const name = prompt("Как вас зовут?");
        if (name) {
          document.body.innerHTML += `<p>Привет, ${name}!</p>`;
          console.log(`Пользователь представился как: ${name}`);
        }
      }
    </script>
  </body>
</html>
```

## Проект "Вывод текста"

Интерактивная страница для ввода и отображения текста пользователя.

### Функциональность

- Поле для ввода текста
- Кнопка для отображения введенного текста
- Счетчик символов
- Валидация ввода

```javascript
class TextDisplay {
  constructor() {
    this.setupEventListeners();
  }

  setupEventListeners() {
    const input = document.getElementById("textInput");
    const button = document.getElementById("displayBtn");
    const output = document.getElementById("output");

    button.addEventListener("click", () => {
      const text = input.value.trim();
      if (text) {
        output.innerHTML = `<p>Вы ввели: <strong>${text}</strong></p>`;
        output.innerHTML += `<p>Количество символов: ${text.length}</p>`;
      } else {
        output.innerHTML = '<p style="color: red;">Введите текст!</p>';
      }
    });
  }
}

new TextDisplay();
```

## Проект "Калькулятор"

Простой калькулятор для основных математических операций.

### Основные функции

- Сложение, вычитание, умножение, деление
- История операций
- Обработка ошибок
- Очистка результата

```javascript
class Calculator {
  constructor() {
    this.history = [];
    this.init();
  }

  init() {
    this.setupEventListeners();
    this.updateDisplay();
  }

  calculate(num1, operator, num2) {
    const a = parseFloat(num1);
    const b = parseFloat(num2);

    if (isNaN(a) || isNaN(b)) {
      throw new Error("Введите корректные числа");
    }

    let result;
    switch (operator) {
      case "+":
        result = a + b;
        break;
      case "-":
        result = a - b;
        break;
      case "*":
        result = a * b;
        break;
      case "/":
        if (b === 0) throw new Error("Деление на ноль");
        result = a / b;
        break;
      default:
        throw new Error("Неизвестная операция");
    }

    const operation = `${a} ${operator} ${b} = ${result}`;
    this.history.push(operation);
    return result;
  }

  setupEventListeners() {
    document.getElementById("calculateBtn").addEventListener("click", () => {
      try {
        const num1 = document.getElementById("num1").value;
        const operator = document.getElementById("operator").value;
        const num2 = document.getElementById("num2").value;

        const result = this.calculate(num1, operator, num2);
        document.getElementById("result").textContent = result;
        this.updateHistory();
      } catch (error) {
        document.getElementById("result").textContent = error.message;
      }
    });
  }

  updateHistory() {
    const historyDiv = document.getElementById("history");
    historyDiv.innerHTML = this.history
      .slice(-5)
      .map((op) => `<div>${op}</div>`)
      .join("");
  }
}

new Calculator();
```

## Проект "Простой статический веб-сайт"

Многостраничный сайт с навигацией и базовой стилизацией.

### Структура проекта

```
website/
├── index.html
├── about.html
├── contact.html
├── css/
│   └── style.css
├── js/
│   └── script.js
└── images/
```

### Основные страницы

1. **Главная страница** - приветствие и навигация
2. **О себе** - информация о разработчике
3. **Контакты** - форма обратной связи

### CSS стили

```css
/* Базовые стили */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: Arial, sans-serif;
  line-height: 1.6;
  color: #333;
}

nav {
  background: #333;
  padding: 1rem;
}

nav ul {
  list-style: none;
  display: flex;
  justify-content: center;
}

nav a {
  color: white;
  text-decoration: none;
  padding: 0 1rem;
}

nav a:hover {
  background: #555;
}

main {
  max-width: 800px;
  margin: 2rem auto;
  padding: 0 1rem;
}

.card {
  background: #f4f4f4;
  padding: 2rem;
  margin: 1rem 0;
  border-radius: 8px;
}
```

### JavaScript функциональность

```javascript
// Активная навигация
document.addEventListener("DOMContentLoaded", () => {
  const currentPage = window.location.pathname.split("/").pop();
  const navLinks = document.querySelectorAll("nav a");

  navLinks.forEach((link) => {
    if (link.getAttribute("href") === currentPage) {
      link.classList.add("active");
    }
  });
});

// Форма контактов
class ContactForm {
  constructor() {
    this.form = document.getElementById("contactForm");
    if (this.form) {
      this.setupEventListeners();
    }
  }

  setupEventListeners() {
    this.form.addEventListener("submit", (e) => {
      e.preventDefault();
      this.submitForm();
    });
  }

  submitForm() {
    const formData = new FormData(this.form);
    const data = Object.fromEntries(formData.entries());

    // Простая валидация
    if (!data.name || !data.email || !data.message) {
      alert("Заполните все поля");
      return;
    }

    if (!this.validateEmail(data.email)) {
      alert("Введите корректный email");
      return;
    }

    // Имитация отправки
    alert("Спасибо за сообщение! Мы свяжемся с вами.");
    this.form.reset();
  }

  validateEmail(email) {
    return /^[^\s@]+@[^\s@]+\.[^\s@]+$/.test(email);
  }
}

new ContactForm();
```

## Git и GitHub интеграция

### Инициализация проекта

```bash
# Создание репозитория
git init
git add .
git commit -m "Инициальный коммит: добавлен базовый сайт"

# Создание репозитория на GitHub
git remote add origin https://github.com/username/my-website.git
git push -u origin main

# Настройка GitHub Pages
# Settings → Pages → Source: Deploy from branch
```

### Система коммитов

```bash
# Функциональные коммиты
git commit -m "Добавлена навигация между страницами"
git commit -m "Стилизована форма контактов"
git commit -m "Добавлена валидация формы"
git commit -m "Исправлена адаптивность на мобильных"
```

## Дополнительные идеи проектов

### 1. Визитка фрилансера

- Одностраничный сайт
- Информация о услугах
- Портфолио работ
- Контактная форма

### 2. Персональный блог

- Список статей
- Чтение отдельной статьи
- Поиск по статьям
- Система тегов

### 3. Новостной сайт

- Лента новостей
- Категории новостей
- Детальный просмотр новости
- Адаптивный дизайн

### 4. Лендинг продукта

- Продающая страница
- Секции с преимуществами
- Отзывы клиентов
- Форма заказа

## Критерии оценки проектов

### Техническая реализация

- [ ] Корректная HTML структура
- [ ] Семантическая разметка
- [ ] Валидный CSS код
- [ ] Работающий JavaScript
- [ ] Обработка ошибок

### Пользовательский интерфейс

- [ ] Интуитивная навигация
- [ ] Адаптивный дизайн
- [ ] Читаемость контента
- [ ] Логичная структура

### Git и версионирование

- [ ] Осмысленные коммиты
- [ ] Структурированная история
- [ ] Корректное использование веток
- [ ] Документация в README

### Дополнительные баллы

- [ ] Использование современных CSS возможностей
- [ ] JavaScript ES6+ фичи
- [ ] Автоматизация (GitHub Actions)
- [ ] Тестирование кода

## Рекомендации по развитию

1. **Начните с простого** - сначала базовая функциональность
2. **Итеративное улучшение** - постепенно добавляйте фичи
3. **Изучайте чужой код** - анализируйте открытые проекты
4. **Получайте обратную связь** - показывайте проекты другим
5. **Документируйте процесс** - ведите заметки о решениях

---

[⬅️ Назад к Git проектам](./26-projects-7.md) | [🏠 На главную](../index.md)
