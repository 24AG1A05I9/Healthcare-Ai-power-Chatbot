# 🚀 **OpenHealth**

<div align="center">

**AI-асистент здоров'я | Працює на ваших даних**

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Web-blue?style=for-the-badge" alt="Platform">
  <img src="https://img.shields.io/badge/Language-TypeScript-blue?style=for-the-badge" alt="Language">
  <img src="https://img.shields.io/badge/Framework-Next.js-black?style=for-the-badge" alt="Framework">
</p>

> **📢 Тепер доступно у веб-версії!**  
> Ми зробили OpenHealth доступнішим з двома спеціалізованими варіантами:  
> **[Клініка](https://qna.open-health.me/)** - Швидкі та прості консультації з питань здоров'я  
> **[Повна платформа](https://www.open-health.me/)** - Розширені інструменти для комплексного управління здоров'ям

### 🌍 Виберіть свою мову
[English](../../README.md) | [Français](README.fr.md) | [Deutsch](README.de.md) | [Español](README.es.md) | [한국어](README.ko.md) | [中文](README.zh.md) | [日本語](README.ja.md) | [Українська](README.uk.md)

</div>

---

<p align="center">
  <img src="/intro/openhealth.avif" alt="Демонстрація OpenHealth">
</p>

## 🌟 Огляд

> OpenHealth допомагає вам **контролювати дані про своє здоров'я**. Використовуючи ШІ та вашу інформацію про особисте здоров'я,
> OpenHealth надає приватного помічника, який допомагає краще розуміти своє здоров'я та керувати ним. Для максимального захисту конфіденційності ви можете повністю запускати його локально.

## ✨ Можливості проекту

<details open>
<summary><b>Ключові можливості</b></summary>

- 📊 **Централізоване введення даних про здоров'я:** Легко об'єднайте всі дані про здоров'я в одному місці.
- 🛠️ **Розумний аналіз:** автоматично аналізує ваші дані про здоров'я та створює файли структурованих даних.
- 🤝 **Контекстуальні бесіди:** Використовуйте структуровані дані як контекст для персоналізованої взаємодії з AI на основі GPT.

</details>

## 📥 Підтримка джерел даних і мовних моделей

<table>
  <tr>
    <th>Джерела даних, які можна додати</th>
    <th>Підтримувані мовні моделі</th>
  </tr>
  <tr>
    <td>
      • Результати аналізу крові<br>
      • Дані перевірки стану здоров'я<br>
      • Особиста фізична інформація<br>
      • Сімейна історія<br>
      • Симптоми
    </td>
    <td>
      • LLaMA<br>
      • DeepSeek-V3<br>
      • GPT<br>
      • Claude<br>
      • Gemini
    </td>
  </tr>
</table>

## 🤔 Чому ми створили OpenHealth

> - 💡 **Ваше здоров'я - ваша відповідальність.**
> - ✅ Справжнє управління здоров'ям поєднує **ваші дані** + **інтелект**, перетворюючи розуміння на дієві плани.
> - 🧠 ШІ діє як неупереджений інструмент, який допомагає вам ефективно керувати своїм довгостроковим здоров'ям.

## 🗺️ Діаграма проекту

```mermaid
graph LR
    subgraph Джерела даних здоров'я
        A1[Клінічні записи<br>Аналізи крові/Діагнози/<br>Рецепти/Знімки]
        A2[Платформи здоров'я<br>Apple Health/Google Fit]
        A3[Носимі пристрої<br>Oura/Whoop/Garmin]
        A4[Особисті записи<br>Дієта/Симптоми/<br>Сімейна історія]
    end

    subgraph Обробка даних
        B1[Аналізатор даних<br>і стандартизація]
        B2[Уніфікований формат<br>медичних даних]
    end

    subgraph Інтеграція ШІ
        C1[Обробка LLM<br>Комерційні та локальні<br>моделі]
        C2[Методи взаємодії<br>RAG/Кеш/Агенти]
    end

    A1 & A2 & A3 & A4 --> B1
    B1 --> B2
    B2 --> C1
    C1 --> C2

    style A1 fill:#e6b3cc,stroke:#cc6699,stroke-width:2px,color:#000
    style A2 fill:#b3d9ff,stroke:#3399ff,stroke-width:2px,color:#000
    style A3 fill:#c2d6d6,stroke:#669999,stroke-width:2px,color:#000
    style A4 fill:#d9c3e6,stroke:#9966cc,stroke-width:2px,color:#000
    
    style B1 fill:#c6ecd9,stroke:#66b399,stroke-width:2px,color:#000
    style B2 fill:#c6ecd9,stroke:#66b399,stroke-width:2px,color:#000
    
    style C1 fill:#ffe6cc,stroke:#ff9933,stroke-width:2px,color:#000
    style C2 fill:#ffe6cc,stroke:#ff9933,stroke-width:2px,color:#000

    classDef default color:#000
```

> **Примітка.** Функціональність синтаксичного аналізу даних наразі реалізована на окремому сервері Python, а в майбутньому її планується перенести на TypeScript.

## Початок роботи

## ⚙️ Як запустити OpenHealth

<details open>
<summary><b>Інструкції з монтажу</b></summary>

1. **Клонуйте репозиторій:**
   ```bash
   git clone https://github.com/OpenHealthForAll/open-health.git
   cd open-health
   ```

2. **Налаштувати та запустити:**
   ```bash
   # Скопіюйте файл середовища
   cp .env.example .env

   # Запустіть програму за допомогою Docker Compose
   docker compose --env-file .env up
   ```

   Для існуючих користувачів використовуйте:
   ```bash
   # Згенеруйте ENCRYPTION_KEY для файлу .env:
   # Виконайте команду нижче та додайте вивід до ENCRYPTION_KEY у .env
   echo $(head -c 32 /dev/urandom | base64)

   # Перебудувати та запустити програму
   docker compose --env-file .env up --build
   ```

3. **Доступ до OpenHealth:**
   Відкрийте браузер і перейдіть до `http://localhost:3000`, щоб почати використовувати OpenHealth.

> **Примітка.** Система складається з двох основних компонентів: аналізу та LLM. Для аналізу ви можете використовувати docling для повного локального виконання, а компонент LLM може працювати повністю локально за допомогою Ollama.

> **Примітка.** Якщо ви використовуєте Ollama з Docker, обов'язково встановіть кінцеву точку Ollama API на: `http://docker.for.mac.localhost:11434` для Mac або `http://host.docker.internal:11434` для Windows.

</details>

---

## 🌐 Спільнота та Підтримка

<div align="center">

### 💫 Поділіться Своєю Історією та Отримуйте Оновлення
[![AIDoctor Subreddit](https://img.shields.io/badge/r/AIDoctor-FF4500?style=for-the-badge&logo=reddit&logoColor=white)](https://www.reddit.com/r/AIDoctor/)
[![Discord](https://img.shields.io/badge/Discord-7289DA?style=for-the-badge&logo=discord&logoColor=white)](https://discord.gg/B9K654g4wf)

### 📬 Контакти
[![Reddit](https://img.shields.io/badge/Reddit-FF4500?style=for-the-badge&logo=reddit&logoColor=white)](https://www.reddit.com/user/Dry_Steak30/)

### 🤝 Поговорити з Командою
[![Calendly](https://img.shields.io/badge/Запланувати_Зустріч-00A2FF?style=for-the-badge&logo=calendar&logoColor=white)](https://calendly.com/open-health/30min)
[![Email](https://img.shields.io/badge/Надіслати_Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:sj@open-health.me)

</div>

