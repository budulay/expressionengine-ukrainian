# Українська локалізація для ExpressionEngine 7 (Ukrainian Language Pack)

[![ExpressionEngine](https://img.shields.io/badge/ExpressionEngine-7.x-blue.svg)](https://expressionengine.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Files](https://img.shields.io/badge/Language%20Files-74%20files-orange.svg)](#структура-пакету)
[![Coverage](https://img.shields.io/badge/Translation-100%25-brightgreen.svg)](#про-переклад)

<p align="center">
  <img src="assets/banner.jpg" alt="ExpressionEngine 7 Ukrainian Language Pack Banner" width="100%">
</p>

Офіційний та повний український мовний пакет для системи керування контентом **ExpressionEngine 7.x** (протестовано на версіях 7.5.x).

---

## 🇺🇦 Про переклад

Цей мовний пакет містить повний переклад інтерфейсу ExpressionEngine українською мовою:
- **Панель керування (Control Panel):** усі меню, форми, списки та налаштування.
- **Модулі та поля:** Канали, записи, файловий менеджер, учасники, коментарі, зв'язки, RTE, форми каналів тощо.
- **Командний рядок (CLI):** повна локалізація команд утиліти `ee-cli`.
- **Електронні листи:** системні сповіщення, шаблони листів відновлення пароля, реєстрації та активації.
- **Захист від спаму:** модуль `spam` з базою українських стоп-слів (`stopwords.php`).

---

## 🚀 Встановлення

### Варіант 1: Встановлення через завантаження архіву (Рекомендований)

1. Перейдіть у розділ **[Releases](../../releases)** на GitHub та завантажте останній релізний ZIP-архів.
2. Розпакуйте архів.
3. Скопіюйте теку `ukrainian` у каталог вашого сайту:
   ```text
   system/user/language/ukrainian/
   ```
4. Переконайтеся, що права доступу дозволяють вебсерверу читати файли з цієї директорії.

---

### Варіант 2: Встановлення через Git

Ви можете клонувати переклад безпосередньо у теку мов ExpressionEngine:

```bash
cd /шлях/до/сайту/system/user/language/
git clone https://github.com/budulay/expressionengine-ukrainian.git ukrainian-repo
cp -r ukrainian-repo/ukrainian .
rm -rf ukrainian-repo
```

Або підключити як Git Submodule:

```bash
cd /шлях/до/сайту/
git submodule add https://github.com/budulay/expressionengine-ukrainian.git system/user/language/ukrainian
```

---

## ⚙️ Активація в ExpressionEngine

Після копіювання файлів мовний пакет автоматично з'явиться у списку доступних мов:

### Для всього сайту (глобально):
1. Увійдіть у панель керування ExpressionEngine.
2. Перейдіть до **Settings** (Налаштування) → **General Settings** (Загальні налаштування).
3. У полі **Default Language** (Мова за замовчуванням) виберіть **Ukrainian** (або `ukrainian`).
4. Натисніть кнопку **Save Settings** (Зберегти налаштування).

### Для окремого користувача / профілю:
1. Натисніть на аватар або ім'я користувача у правому верхньому куті CP.
2. Перейдіть до **Personal Settings** (Особисті налаштування).
3. У полі **Control Panel Language** оберіть **Ukrainian**.
4. Збережіть зміни.

---

## 📁 Структура пакету

```text
expressionengine-ukrainian/
├── ukrainian/                      # Папка перекладу (копіюється в system/user/language/)
│   ├── addons_lang.php
│   ├── admin_lang.php
│   ├── channel_lang.php
│   ├── cli_lang.php
│   ├── content_lang.php
│   ├── cp_lang.php
│   ├── email_data.php
│   ├── filemanager_lang.php
│   ├── member_lang.php
│   ├── members_lang.php
│   ├── settings_lang.php
│   ├── ...                         # Загалом 74 мовних файли
│   └── spam/
│       └── stopwords.php           # Українські стоп-слова
├── .github/
│   └── workflows/
│       └── lint.yml                # CI валідація синтаксису PHP
├── .gitattributes
├── .gitignore
├── CONTRIBUTING.md                 # Інструкція для бажаючих долучитися
├── LICENSE                         # Ліцензія MIT
└── README.md                       # Цей файл
```

---

## 🤝 Внесок у розвиток (Contributing)

Якщо ви помітили одруківку, неточність або маєте пропозиції щодо кращого перекладу термінів:
1. Перегляньте [CONTRIBUTING.md](CONTRIBUTING.md) та наш [глосарій термінів](CONTRIBUTING.md#глосарій-термінів-expressionengine).
2. Створіть [Issue](../../issues) з описом пропозиції або надішліть [Pull Request](../../pulls).

---

## 📄 Ліцензія

Цей проєкт поширюється на умовах відкритої ліцензії **MIT**. Детальніше дивіться у файлі [LICENSE](LICENSE).

---

## 🇬🇧 English Summary

This repository contains the full Ukrainian language pack for **ExpressionEngine 7.x** (compatible with 7.5.x).
To install, simply place the `ukrainian/` directory into `system/user/language/` in your ExpressionEngine installation, then go to **Settings → General Settings** and set **Default Language** to **Ukrainian**.
Distributed under the **MIT License**.
