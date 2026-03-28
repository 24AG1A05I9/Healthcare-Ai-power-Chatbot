# 🚀 **OpenHealth**

<div align="center">

**ИИ-ассистент здоровья | Работает на ваших данных**

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Web-blue?style=for-the-badge" alt="Platform">
  <img src="https://img.shields.io/badge/Language-TypeScript-blue?style=for-the-badge" alt="Language">
  <img src="https://img.shields.io/badge/Framework-Next.js-black?style=for-the-badge" alt="Framework">
</p>

> **📢 Теперь доступно в веб-версии!**  
> Мы сделали OpenHealth доступнее с двумя специализированными вариантами:  
> **[Клиника](https://qna.open-health.me/)** - Быстрые и простые консультации по вопросам здоровья  
> **[Полная платформа](https://www.open-health.me/)** - Расширенные инструменты для комплексного управления здоровьем

### 🌍 Выберите язык
[English](../../README.md) | [Français](README.fr.md) | [Deutsch](README.de.md) | [Español](README.es.md) | [한국어](README.ko.md) | [中文](README.zh.md) | [日本語](README.ja.md) | [Українська](README.uk.md) | [Русский](README.ru.md) | [اردو](README.ur.md)

</div>

---

<p align="center">
  <img src="/intro/openhealth.avif" alt="OpenHealth Demo">
</p>

## 🌟 Обзор

> OpenHealth помогает вам **взять под контроль ваши данные о здоровье**. Используя ИИ и вашу личную медицинскую информацию,
> OpenHealth предоставляет приватного ассистента, который помогает вам лучше понимать и управлять своим здоровьем. Для максимальной конфиденциальности вы можете полностью запускать его локально.

## ✨ Особенности проекта

<details open>
<summary><b>Основные функции</b></summary>

- 📊 **Централизованный ввод данных о здоровье:** Легко объединяйте все ваши данные о здоровье в одном месте.
- 🛠️ **Умный парсинг:** Автоматически анализирует ваши данные о здоровье и создает структурированные файлы данных.
- 🤝 **Контекстные разговоры:** Используйте структурированные данные как контекст для персонализированного взаимодействия с ИИ на базе GPT.

</details>

## 🌐 Сообщество и поддержка

<div align="center">

### 💫 Поделитесь своей историей и получайте обновления
[![AIDoctor Subreddit](https://img.shields.io/badge/r/AIDoctor-FF4500?style=for-the-badge&logo=reddit&logoColor=white)](https://www.reddit.com/r/AIDoctor/)
[![Discord](https://img.shields.io/badge/Discord-7289DA?style=for-the-badge&logo=discord&logoColor=white)](https://discord.gg/B9K654g4wf)

### 📬 Контакты
[![Reddit](https://img.shields.io/badge/Reddit-FF4500?style=for-the-badge&logo=reddit&logoColor=white)](https://www.reddit.com/user/Dry_Steak30/)

</div>

2. **Настройка и запуск:**
   ```bash
   # Скопируйте файл окружения
   cp .env.example .env

   # Запустите приложение с помощью Docker Compose
   docker compose --env-file .env up
   ```

   Для существующих пользователей:
   ```bash
   # Сгенерируйте ENCRYPTION_KEY для файла .env:
   # Выполните команду ниже и добавьте вывод в ENCRYPTION_KEY в .env
   echo $(head -c 32 /dev/urandom | base64)

   # Пересоберите и запустите приложение
   docker compose --env-file .env up --build
   ```

> **Примечание:** Система состоит из двух основных компонентов: парсинга и LLM. Для парсинга вы можете использовать docling для полного локального выполнения, а компонент LLM может работать полностью локально с помощью Ollama. 