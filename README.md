# Буренков М.М. — Full-Stack Developer

Создаю веб-приложения, мобильные приложения и Telegram-боты под ключ, внедряю ИИ и автоматизирую бизнес-процессы.
3 года коммерческого опыта, продукты с живой аудиторией в Google Play. Основатель студии [Narodniy Team](https://narodniy-team.ru).

**Мои сервисы:** [🛡 narodniyvpn.online](https://narodniyvpn.online/) — собственный VPN-сервис · [🤖 narodniy-team.ru/ai](https://narodniy-team.ru/ai/) — AI-ассистент для бизнеса

---

## 🛠 Технологический стек

| Категория | Технологии |
|-----------|-----------|
| **Frontend** | React, Next.js, TypeScript, Tailwind CSS |
| **Mobile** | Flutter, React Native, Dart |
| **Backend** | Node.js, Python (FastAPI, Aiogram), PostgreSQL |
| **AI & автоматизация** | Gemini API, OpenRouter, RAG, Playwright, парсинг данных |
| **Telegram** | Telegram Bot API, Mini-Apps, Web Apps |
| **Инструменты** | Git, Docker, Nginx, Firebase, Figma |

---

## 🤖 ИИ и автоматизация

Отдельное направление студии: беру рутину, которую в компании делают руками, и превращаю её в сервис, который работает сам.

**Что делаю:**

- **AI-ассистенты для клиентского сервиса** — отвечают в Telegram, WhatsApp, на сайте и Avito круглосуточно, по загруженному прайсу и базе знаний компании. Записывают в календарь, принимают заказы, эскалируют сложные вопросы менеджеру и присылают отчёт по диалогам за сутки.
- **Автоматизация контента** — сбор из RSS/источников, AI-обработка (перевод, рерайт, форматирование, эмодзи и хештеги) и публикация по расписанию без участия человека.
- **Сбор и обогащение данных** — парсеры на Playwright с антидетектом, второй проход по сайтам компаний за email и соцсетями, выгрузка в Excel/CSV для отдела продаж.
- **Интеграции** — приём заявок в Telegram, вебхуки платёжных систем, CRM, Яндекс.Метрика и цели по воронке.

### [🤖 AI-ассистент 24/7 — лендинг направления](https://github.com/bmxer32/ai-assistant-landing)

Живой сайт: **[narodniy-team.ru/ai](https://narodniy-team.ru/ai/)**

Продающий одностраничник услуги, сделанный принципиально «не как у всех»: постерная стикерная эстетика с толстыми обводками и жёсткими смещёнными тенями вместо привычных градиентов со стеклянными карточками.

- **Работающее чат-демо** в первом экране вместо списка возможностей — посетитель жмёт вопрос, ассистент «печатает» и отвечает.
- **Калькулятор упущенной выручки** — два ползунка (обращения в месяц и средний чек), сумма пересчитывается с анимацией, допущения расчёта выписаны прямо под ним.
- **Приём заявок** — свой Node-сервис без зависимостей (systemd + nginx), заявка пишется в журнал и дублируется в Telegram. Форма работает и без JavaScript.
- **Ноль внешних запросов** — шрифты локальные, страница не ходит ни на один сторонний домен. Скрипт ~10 КБ, полностью читается с выключенным JS.
- Доступность: семантическая разметка, видимый фокус, `aria-live` в чате, уважается `prefers-reduced-motion`.

**Стек:** ванильные HTML/CSS/JS без сборки, Node.js (приём заявок), nginx, Яндекс.Метрика

---

## 📂 Избранные проекты

### [Narodniy VPN — собственный VPN-сервис](https://narodniyvpn.online/)

Живой сервис: **[narodniyvpn.online](https://narodniyvpn.online/)** · клиенты для [Windows](https://github.com/bmxer32/NarodniyVPN-PC) и [Android](https://github.com/bmxer32/NarodniyVPN-Android)

VPN с боевым сервером и живой аудиторией: split-tunneling, маршрутизация Discord/Telegram/YouTube, шифрование лицензий, Telegram Mini-App магазин и платёжный бэкенд. Выдача ключа через бота за минуты, без регистрации. Android-клиент — Flutter с нативными каналами (MethodChannel) к Xray, [опубликован в Google Play](https://play.google.com/store/apps/details?id=online.narodniyvpn.app).

**Стек:** Flutter/Dart, VLESS/Reality (Xray), Electron, FastAPI, PostgreSQL, Telegram Mini-Apps

### [Yandex Maps Scraper — десктоп-приложение для сбора данных](https://github.com/bmxer32/yandex-maps-scraper)

Windows-приложение (.exe с установщиком), которое собирает базу организаций с Яндекс.Карт: сфера, адрес, телефон, координаты, рейтинг, часы работы, сайт, соцсети и email.

- **Географический каскад** — страна → область → город → район/метро, с полными списками районов и станций для Москвы и Санкт-Петербурга.
- **Два прохода** — сначала карточки организаций за сайтами и соцсетями, затем обход самих сайтов за email-адресами.
- **Антидетект** — stealth-маскировка headless Chromium, рандомизация профиля браузера (UA, viewport, timezone), «человеческие» задержки, поддержка прокси.
- **Прогресс в реальном времени** через Server-Sent Events, фильтры и сортировка в таблице, экспорт в Excel/CSV.

**Стек:** Python, FastAPI, Playwright, SQLAlchemy/SQLite, Next.js 15, React 19, Electron + electron-builder

### [Reko — AI Fitness & Nutrition Diary](https://github.com/bmxer32/reko)
Flutter-приложение для отслеживания питания и тренировок с ИИ-сканером еды на базе Google Gemini. [Опубликовано в Google Play](https://play.google.com/store/apps/details?id=com.buren.fitness_app). Offline-first, Firebase-синхронизация, тёмная тема.

**Стек:** Flutter, Riverpod, Drift, Firebase, Gemini API, OpenFoodFacts

### [MegaBot — RSS → AI → Telegram](https://github.com/bmxer32/RSS-tg-bot)
Бот автоматизации ведения каналов: собирает материалы из RSS-лент, обрабатывает через AI (перевод, форматирование, эмодзи/хештеги) и публикует по расписанию.

**Стек:** Python, Aiogram 3, SQLAlchemy 2.0, APScheduler

### [Narodniy Team — сайт студии](https://github.com/bmxer32/narodniy-team)
Продающий сайт студии разработки с анимациями, SEO-посадочными под каждую услугу и кастомным UI без конструкторов. Живой сайт: [narodniy-team.ru](https://narodniy-team.ru).

**Стек:** Next.js 14, React 18, Framer Motion, Lenis, Vercel

### [KOKO Studio — сайт салона бровей и ресниц](https://github.com/bmxer32/koko-studio-demo)

Живой сайт: **[bmxer32.github.io/koko-studio-demo](https://bmxer32.github.io/koko-studio-demo/)**

[![KOKO Studio — первый экран на десктопе и телефоне](https://raw.githubusercontent.com/bmxer32/koko-studio-demo/main/docs/preview.png)](https://bmxer32.github.io/koko-studio-demo/)

Салон у м. Войковская с рейтингом 5.0 и 148 отзывами на Яндекс Картах, у которого не было сайта: только карточка в Яндекс Бизнесе и запись перепиской в Telegram. Весь контент собственный — 65 работ студии, 26 услуг с ценами и длительностью, отзывы дословно.

- **Шкала объёма 1D–5D** на первом экране. «D» — это сколько наращённых ресниц крепится на одну свою, и ползунок рисует ровно это: SVG-схема ресничного ряда генерируется на лету, дробный объём чередует (1,5D — то одна, то две). Отвечает на вопрос, который клиентки чаще всего задают в личку, и не выдаёт конкретную работу за объём, которым её никто не подписывал.
- **Онлайн-запись вместо переписки** — рабочий YCLIENTS студии открывается в модалке: услуга, мастер, живое расписание. Telegram и WhatsApp остались запасным путём.
- **Галерея на 65 работ** с фильтрами по направлениям, лайтбоксом и ленивой загрузкой; webp в двух размерах, ~1,7 МБ на первый экран сетки.
- **Mobile-first** с липкой панелью записи — почти весь трафик приходит с Яндекс Карт с телефона. Фокус с клавиатуры, `prefers-reduced-motion`, alt у всех изображений.
- Прайс, отзывы и фотографии вынесены в один файл данных — контент правится без вёрстки.

**Стек:** ванильные HTML/CSS/JS без сборки, SVG-графика на лету, виджет записи YCLIENTS, GitHub Pages

### [ВАШ Эксперт — сайт под ключ для клиента](https://github.com/bmxer32/v-experto)
Корпоративный сайт оценочной компании (г. Иваново): дизайн, разработка, деплой, приём заявок в Telegram, аналитика. Живой сайт: [v-experto.ru](https://v-experto.ru).

**Стек:** Next.js 15, React 19, Tailwind CSS v4, Telegram Bot API, Vercel

### [Мир волос — сайт записи для мастера](https://github.com/bmxer32/mirvolos)
Mobile-first лендинг мастера наращивания волос: онлайн-запись с заявками в Telegram/WhatsApp, галерея работ «до/после», SEO. Живой сайт: [mirvolos32.ru](https://mirvolos32.ru).

**Стек:** Next.js 15, TypeScript, Tailwind CSS 4, Framer Motion

---

## 📞 Контакты

| | |
|---|---|
| **Telegram** | [@webe9](https://t.me/webe9) |
| **Сайт студии** | [narodniy-team.ru](https://narodniy-team.ru) |
| **AI-ассистент** | [narodniy-team.ru/ai](https://narodniy-team.ru/ai/) |
| **VPN-сервис** | [narodniyvpn.online](https://narodniyvpn.online/) |
| **Email** | [v71072587@gmail.com](mailto:v71072587@gmail.com) |

---

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=bmxer32&label=Profile+views&color=0e75b6&style=flat" alt="Profile views" />
</p>
