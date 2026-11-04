---

# 📘 AI Screenshot Assistant Ultimate (Multi-Provider Edition)

© 2025 **Diberlog**
Licensed under the **MIT License**

---

## 🧩 Описание

**AI Screenshot Assistant Ultimate** — это интеллектуальный помощник для анализа и обработки текста со скриншотов.
Программа автоматически распознаёт текст (через **Tesseract OCR**) и отправляет его в выбранный AI-провайдер (Google Gemini, Groq, OpenAI, DeepSeek, Together или Custom API).

Поддерживает горячие клавиши, мгновенные ответы, сохранение настроек, красивый интерфейс и загрузочный экран.
Работает полностью локально, без установки серверов или сторонних модулей.

---

## ⚙️ Возможности

✅ Снятие скриншотов и OCR-распознавание текста
✅ Работа с **6 AI-провайдерами:**

* 🟦 Google Gemini (по умолчанию)
* 🟪 OpenAI (GPT-3.5, GPT-4)
* 🟩 Groq (очень быстрый, OpenAI-совместимый)
* 🟧 DeepSeek (OpenAI-альтернатива)
* 🟨 Together AI (бесплатные кредиты)
* ⚙️ Custom API (любой OpenAI-совместимый эндпоинт)

✅ Индивидуальные настройки для каждого провайдера
✅ Автоочистка Markdown (`**`, `_`, `#` и т.д.)
✅ Поддержка горячих клавиш (`Ctrl+B`, `Ctrl+C`, `Ctrl+V`)
✅ Тёмная/светлая тема интерфейса
✅ Splash-экран при запуске
✅ Сохранение всех конфигураций в `ai_gui_config.json`

---

## 🖥️ Системные требования

* Windows 10 / 11 (64-бит)
* Python 3.11+ *(если используется исходный код)*
* [Tesseract OCR](https://github.com/UB-Mannheim/tesseract/wiki)

  > После установки укажи путь:
  > `C:\Program Files\Tesseract-OCR\tesseract.exe`

---

## 📦 Установка и запуск

### 🧩 Вариант 1 — Готовый EXE

1. Распакуй архив.
2. Запусти `AI_Screenshot_Assistant.exe`.
3. Если SmartScreen предупреждает — «Дополнительно → Всё равно выполнить».

### 🧠 Вариант 2 — Из исходников

```bash
pip install -r requirements.txt
python chat_gui_ultimate.py
```

Или собрать `.exe` самому:

```bash
pyinstaller --noconsole --onefile --icon "icon_robot.ico" --name "AI_Screenshot_Assistant" --add-data "ai_gui_config.json;." chat_gui_ultimate.py
```

---

## 🔑 Настройки провайдеров

Файл конфигурации: **`ai_gui_config.json`**

```json
{
  "provider": "google",
  "api_key": "ВАШ_КЛЮЧ_API",
  "model": "gemini-2.0-flash",
  "theme": "dark",
  "hotkey": "ctrl+b",
  "tesseract_path": "C:\\Program Files\\Tesseract-OCR\\tesseract.exe",
  "screenshot_dir": "C:\\AI_Screenshot_Assistant\\screenshot_temp",
  "providers": {
    "google": {
      "base_url": "https://generativelanguage.googleapis.com/v1beta/models/gemini-2.0-flash:generateContent"
    },
    "openai": {
      "base_url": "https://api.openai.com/v1"
    },
    "groq": {
      "base_url": "https://api.groq.com/openai/v1"
    },
    "deepseek": {
      "base_url": "https://api.deepseek.com"
    },
    "together": {
      "base_url": "https://api.together.ai"
    },
    "custom": {
      "base_url": "",
      "auth_header_name": "Authorization"
    }
  }
}
```

> 💾 Все настройки сохраняются автоматически и индивидуальны для каждого провайдера.

---

## 🔥 Быстрые клавиши

| Комбинация     | Действие                 |
| -------------- | ------------------------ |
| `Ctrl + B`     | Сделать скриншот области |
| `Ctrl + C`     | Скопировать ответ        |
| `Ctrl + V`     | Вставить текст           |
| `Ctrl + Enter` | Отправить запрос         |

---

## 📚 Используемые библиотеки Python

```
customtkinter
pillow
pytesseract
keyboard
pyperclip
requests
google-genai
groq
```

*(автоматически устанавливаются при первом запуске)*

---

## 🧰 Технологии

| Компонент                     | Назначение                |
| ----------------------------- | ------------------------- |
| **CustomTkinter**             | современный интерфейс GUI |
| **Pillow**                    | работа с изображениями    |
| **Pytesseract**               | OCR-распознавание текста  |
| **Keyboard**                  | горячие клавиши           |
| **Requests**                  | HTTP-запросы              |
| **Google GenAI / OpenAI API** | взаимодействие с AI       |
| **PyInstaller**               | сборка `.exe`             |

---

## 🚀 Основной функционал

* 📸 Снимай область экрана
* 🧠 Распознавай текст с изображения
* 🤖 Отправляй запросы в выбранную нейросеть
* 💬 Получай форматированные ответы без Markdown
* 💾 Сохраняй индивидуальные ключи и модели
* ⚙️ Настраивай провайдеры через интерфейс

---

## 🧑‍💻 Автор

**Diberlog**
📅 Версия: *2025.1 (Multi-Provider Edition)*
📍 Дата сборки: *19 октября 2025 г.*

---

## 🌐 Полезные ссылки

* 🔗 [Документация Tesseract OCR](https://docs.coro.net/featured/agent/install-tesseract-windows/)
* 🔗 [Google Gemini API Docs](https://cloud.google.com/vertex-ai/generative-ai/docs)
* 🔗 [Groq Console](https://console.groq.com)
* 🔗 [Together AI Docs](https://api.together.ai)

---

## 📜 Лицензия (MIT)

Создай рядом с программой файл **`LICENSE.txt`** со следующим содержимым:

```
MIT License

Copyright (c) 2025 Diberlog

Настоящим разрешается, бесплатно, любому лицу, получившему копию данного программного обеспечения и 
сопутствующей документации (далее «Программное обеспечение»), без ограничений использовать Программное обеспечение, 
включая без ограничения права на использование, копирование, изменение, слияние, публикацию, распространение, 
сублицензирование и/или продажу копий Программного обеспечения, а также лицам, которым предоставляется данное 
Программное обеспечение, разрешается то же, при соблюдении следующих условий:

Указанное выше уведомление об авторском праве и настоящее уведомление о разрешении 
должны быть включены во все копии или значимые части данного Программного Обеспечения.

ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ ПРЕДОСТАВЛЯЕТСЯ «КАК ЕСТЬ», БЕЗ КАКИХ-ЛИБО ГАРАНТИЙ, ЯВНЫХ ИЛИ ПОДРАЗУМЕВАЕМЫХ, 
ВКЛЮЧАЯ, НО НЕ ОГРАНИЧИВАЯСЬ ГАРАНТИЯМИ ТОВАРНОЙ ПРИГОДНОСТИ, СООТВЕТСТВИЯ ОПРЕДЕЛЕННОЙ ЦЕЛИ И 
НЕНАРУШЕНИЯ ПРАВ. НИ ПРИ КАКИХ ОБСТОЯТЕЛЬСТВАХ АВТОРЫ ИЛИ ПРАВООБЛАДАТЕЛИ НЕ НЕСУТ ОТВЕТСТВЕННОСТИ 
ПО КАКИМ-ЛИБО ИСКАМ, УБЫТКАМ ИЛИ ИНЫМ ТРЕБОВАНИЯМ, ВОЗНИКАЮЩИМ ИЗ, ИЛИ В СВЯЗИ С, ПРОГРАММНЫМ ОБЕСПЕЧЕНИЕМ 
ИЛИ ИСПОЛЬЗОВАНИЕМ ИЛИ ДРУГИМИ ДЕЙСТВИЯМИ С ПРОГРАММНЫМ ОБЕСПЕЧЕНИЕМ.
```

---

## 📜 Лицензия
Проект распространяется по лицензии **MIT License**  
© 2025 Diberlog