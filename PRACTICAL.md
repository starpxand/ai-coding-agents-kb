# 🛠️ Практический раздел: Hello World в Cursor

> Создание базового проекта с помощью AI-агента Cursor

---

## Почему Cursor?

Для практической демонстрации выбран **Cursor** как наиболее функциональный и распространённый инструмент среди Standalone IDE-агентов. Обоснование выбора изложено в [разделе выводов](CONCLUSION.md).

Мы создадим простой веб-проект «Hello World» — HTML-страницу с CSS и JavaScript — полностью через диалог с AI-агентом, без написания кода вручную.

---

## Установка и настройка Cursor

### Шаг 1: Скачать и установить

1. Перейдите на [cursor.com](https://cursor.com)
2. Нажмите **Download** — Cursor автоматически определит вашу ОС (Windows / macOS / Linux)
3. Установите приложение стандартным способом

### Шаг 2: Первый запуск

При первом запуске Cursor предложит:
- **Импортировать настройки из VS Code** — рекомендуется, если работали в VS Code
- Выбрать тему оформления
- **Авторизоваться** — создайте аккаунт на cursor.com (бесплатный тариф доступен сразу)

### Шаг 3: Ориентация в интерфейсе

```
┌─────────────────────────────────────────────────────┐
│  CURSOR IDE                                          │
│                                                     │
│  ┌──────────┐  ┌───────────────────┐  ┌──────────┐ │
│  │ Explorer │  │   Редактор кода    │  │ AI Chat  │ │
│  │ (файлы)  │  │                   │  │ (Cmd+L)  │ │
│  └──────────┘  └───────────────────┘  └──────────┘ │
│                                                     │
│  ┌─────────────────────────────────────────────────┐ │
│  │  Терминал (Ctrl+`)                              │ │
│  └─────────────────────────────────────────────────┘ │
└─────────────────────────────────────────────────────┘
```

**Основные горячие клавиши:**

| Команда | Действие |
|---------|----------|
| `Cmd/Ctrl + L` | Открыть AI Chat |
| `Cmd/Ctrl + K` | Inline редактирование выделенного кода |
| `Cmd/Ctrl + I` | Открыть Composer (агентный режим) |
| `Tab` | Принять автодополнение |

---

## Создание проекта Hello World

### Этап 1: Открыть папку проекта

1. Откройте Cursor
2. **File → Open Folder**
3. Создайте новую папку `hello-world-ai` и откройте её
4. Откройте терминал: `` Ctrl + ` ``

### Этап 2: Запрос к AI-агенту через Composer

Нажмите `Cmd/Ctrl + I` для открытия **Composer** (агентный режим).

Введите следующий промпт:

```
Создай базовый Hello World веб-проект со следующей структурой:
- index.html — главная страница
- style.css — стили
- script.js — небольшой JavaScript

Требования:
1. Страница должна отображать "Hello, World!" с красивым оформлением
2. Добавь кнопку, при нажатии на которую текст меняет цвет
3. Используй современный CSS (flexbox, переменные, анимации)
4. Код должен быть чистым и прокомментированным
```

### Этап 3: Агент создаёт проект

Cursor Composer начнёт работу и вы увидите:

```
● Создание файловой структуры проекта...
  ○ Создан index.html
  ○ Создан style.css  
  ○ Создан script.js

● Применение изменений...
  ✓ 3 файла создано
```

Агент создаст все три файла автоматически. Ниже — пример того, что будет сгенерировано.

---

### Результат: Сгенерированные файлы

#### `index.html`
```html
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hello World — AI Demo</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="container">
        <h1 class="greeting" id="greeting">Hello, World!</h1>
        <p class="subtitle">Создано с помощью Cursor AI</p>
        <button class="btn" id="colorBtn">Сменить цвет</button>
        <div class="counter">
            Нажатий: <span id="count">0</span>
        </div>
    </div>
    <script src="script.js"></script>
</body>
</html>
```

#### `style.css`
```css
/* CSS-переменные для темизации */
:root {
    --primary: #6366f1;
    --bg: #0f172a;
    --text: #f1f5f9;
    --accent: #818cf8;
}

* { margin: 0; padding: 0; box-sizing: border-box; }

body {
    background: var(--bg);
    color: var(--text);
    font-family: 'Segoe UI', sans-serif;
    min-height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
}

.container { text-align: center; padding: 2rem; }

/* Анимация появления */
.greeting {
    font-size: clamp(2rem, 8vw, 5rem);
    color: var(--primary);
    animation: fadeInDown 0.8s ease;
    transition: color 0.3s ease;
    margin-bottom: 1rem;
}

.btn {
    background: var(--primary);
    color: white;
    border: none;
    padding: 0.75rem 2rem;
    border-radius: 8px;
    font-size: 1rem;
    cursor: pointer;
    transition: transform 0.2s, box-shadow 0.2s;
}

.btn:hover {
    transform: translateY(-2px);
    box-shadow: 0 8px 20px rgba(99, 102, 241, 0.4);
}

@keyframes fadeInDown {
    from { opacity: 0; transform: translateY(-20px); }
    to   { opacity: 1; transform: translateY(0); }
}
```

#### `script.js`
```javascript
// Набор цветов для смены
const colors = [
    '#6366f1', // indigo
    '#ec4899', // pink
    '#10b981', // emerald
    '#f59e0b', // amber
    '#3b82f6', // blue
];

let colorIndex = 0;
let clickCount = 0;

const greeting = document.getElementById('greeting');
const btn = document.getElementById('colorBtn');
const counter = document.getElementById('count');

// Обработчик нажатия кнопки
btn.addEventListener('click', () => {
    colorIndex = (colorIndex + 1) % colors.length;
    greeting.style.color = colors[colorIndex];

    clickCount++;
    counter.textContent = clickCount;

    // Небольшая анимация кнопки
    btn.style.transform = 'scale(0.95)';
    setTimeout(() => btn.style.transform = '', 100);
});
```

---

### Этап 4: Запуск проекта

**Открыть напрямую в браузере:**
```bash
open index.html        # macOS
start index.html       # Windows
xdg-open index.html    # Linux
```

**Или через Live Server** (расширение совместимо с Cursor как с VS Code):
1. Правая кнопка на `index.html` → **Open with Live Server**
2. Браузер откроет `localhost:5500`

---

### Этап 5: Дальнейшие итерации с AI

Открываем Chat (`Cmd + L`) и продолжаем диалог:

**Добавить функциональность:**
```
Добавь dark/light mode toggle в правом верхнем углу.
Сохрани выбор пользователя в localStorage.
```

**Улучшить адаптивность:**
```
Кнопка не адаптирована для мобильных устройств.
Исправь, сделай страницу полностью responsive.
```

**Объяснить код:**
```
Объясни, как работает функция смены цвета в script.js.
Какие паттерны JavaScript здесь используются?
```

---

## Ключевые наблюдения

**Что Cursor сделал агентно:**

1. Создал все три файла сразу — не спрашивал «а теперь CSS?», сам понял структуру и создал проект целиком
2. Код соответствует современным практикам: CSS-переменные, flexbox, семантический HTML
3. Выполнил требование о комментариях из промпта
4. При дальнейших итерациях помнит контекст и добавляет изменения согласованно

**Ограничения бесплатного тарифа:**
- После 50 premium-запросов скорость снижается (используются менее мощные модели)
- 2 000 автодополнений в месяц достаточно для учебных проектов

---

## Итог

За несколько минут и без ручного написания кода получили:
- ✅ Структуру проекта (3 файла)
- ✅ Современный HTML с семантической разметкой
- ✅ CSS с переменными, flexbox и анимациями
- ✅ Интерактивный JavaScript
- ✅ Прокомментированный, читаемый код

Cursor наглядно демонстрирует агентный подход: понял задачу целиком, самостоятельно декомпозировал на файлы и создал согласованный результат.

---

*← [Сравнительная таблица](COMPARISON_TABLE.md) | [Выводы →](CONCLUSION.md)*