# Ableton Landing Page Clone

![Project Status](https://img.shields.io/badge/Status-In%20Progress-orange)
![License](https://img.shields.io/badge/License-ISC-blue)

Цей репозиторій містить навчальний проєкт — верстку лендінгу (клону)
сайту [Ableton](https://www.ableton.com/). Головна мета проєкту — практика
сучасної, семантичної та адаптивної верстки з використанням методології BEM та
препроцесора SCSS.

🔗 **[Подивитися демо]** https://kovalykvadym.github.io/ableton-project/

## 🛠 Технічний стек

* **HTML5**: Семантична розмітка, використання тегу `<dialog>` для модальних
  вікон.
* **SCSS (Sass)**: Модульна архітектура, змінні, міксіни, вкладеність.
* **BEM**: Методологія найменування класів (Block Element Modifier).
* **JavaScript**: Базова логіка взаємодії (відкриття/закриття меню).

## ✨ Особливості реалізації

У проєкті використані сучасні підходи до написання CSS:

1. **Модульна архітектура SCSS**:
   Стилі розбиті на окремі файли за принципом **7-1 pattern** (частково):

* `_variables.scss` — CSS змінні для легкої зміни теми.
* `_mixins.scss` — допоміжні інструменти.
* `_normalize.scss` — кастомний сучасний скидання стилів (reset) з використанням
  `:where()`.
* `blocks/` — стилі для окремих компонентів (Header, Hero, Burger Button тощо).

2. **Адаптивна типографіка (Fluid Typography)**:
   Використано функцію `clamp()` через власний міксін `fluid-text`. Розмір
   шрифтів плавно змінюється між мінімальним та максимальним значенням залежно
   від ширини в'юпорту, без різких стрибків на брейкпоїнтах.

   ```scss
   /* Приклад використання */
   @include fluid-text($max: 48, $min: 16);
   ```

3. **Нативний Dialog API**:
   Мобільне меню реалізовано через HTML-тег `<dialog>`, що забезпечує нативну
   доступність та зручне керування станами (відкрито/закрито) без важких
   JS-бібліотек.

4. **Адаптивність (Mobile First / Desktop First)**:
   Використання міксінів `@include mobile`, `@include tablet`,
   `@include desktop` для зручного керування медіа-запитами.

## 📂 Структура проєкту

```text
.
├── assets/              # Зображення, шрифти
├── styles/              # SCSS файли
│   ├── blocks/          # Компоненти (BEM блоки)
│   │   ├── _burger_button.scss
│   │   ├── _header.scss
│   │   ├── _hero.scss
|   |   ├── _mobile_overlay.scss
│   ├── _fonts.scss      # Підключення шрифтів
│   ├── _globals.scss    # Загальні стилі body, h1-h6
│   ├── _media.scss      # Брейкпоїнти та медіа-міксіни
│   ├── _mixins.scss     # Утилітарні міксіни (fluid-text, flex-center)
│   ├── _normalize.scss  # Нормалізація стилів
│   ├── _utils.scss      # Допоміжні класи (container, hidden-mobile)
│   ├── _variables.scss  # Кольори, розміри, шрифти
│   └── styles.scss      # Головний файл зборки
├── index.html           # Головна сторінка
├── package.json         # Інформація про проєкт
└── .gitignore
```

🚀 Як запустити проєкт

1. **Клонуйте репозиторій:**

```bash 
git clone https://github.com/kovalykvadym/ableton-project
```

2. **Відкрийте проєкт:**
   Відкрийте папку проєкту у вашому редакторі коду (наприклад, **VS Code**).
3. **Компіляція SCSS:**

- Якщо ви використовуєте розширення **Live Sass Compiler** для VS Code, просто
  натисніть "Watch Sass".
- Або встановіть Sass глобально та запустіть відстеження:

```bash 
sass --watch styles/styles.scss styles/styles.css
```

4. **Запуск:**
   Відкрийте файл `index.html` у браузері або скористайтеся розширенням **Live
   Server**.

## 👨‍💻 Автор

**Kovalyk Vadym**

* GitHub: [kovalykvadym](https://github.com/kovalykvadym)
