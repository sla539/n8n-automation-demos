# n8n Automation Demos

Три демонстраційні воркфлоу на n8n з AI-інтеграціями та Telegram. Це навчальні проєкти для портфоліо на вигаданих бізнес-сценаріях. Кожен демонструє окремий підхід до автоматизації.

| Демо | Що робить | Технології |
|---|---|---|
| [Demo 1 — Telegram AI-бот барбершопу](demo1-telegram-ai-bot) | Відповідає клієнтам на питання про ціни й години, збирає дані для запису, пам'ятає контекст розмови | n8n, AI Agent, OpenAI, Telegram Bot API |
| [Demo 2 — Заявки з сайту](demo2-lead-to-sheets) | Приймає заявку через вебхук, AI визначає категорію й пріоритет, записує в Google Sheets, сповіщає в Telegram | n8n, Webhook, OpenAI, Google Sheets |
| [Demo 3 — Щоденний AI-дайджест](demo3-daily-ai-digest) | Щодня о 9:00 бере новини з RSS, AI коротко переказує їх українською та надсилає в Telegram | n8n, Schedule, RSS, OpenAI |

## Структура

```
n8n-automation-demos/
├── demo1-telegram-ai-bot/
│   ├── workflow.json   # файл для імпорту в n8n
│   ├── schema.png      # схема воркфлоу
│   ├── demo.mp4        # коротка анімація схеми
│   ├── demo.gif        # те саме для превʼю в README
│   └── README.md
├── demo2-lead-to-sheets/
└── demo3-daily-ai-digest/
```

## Як запустити

1. Підніми n8n: хмарна версія на n8n.io або локально
   `docker run -it --rm -p 5678:5678 docker.n8n.io/n8nio/n8n`
2. У n8n: **Workflows → Create → меню «⋯» → Import from file** і вибери `workflow.json` потрібного демо.
3. Підключи свої credentials (Telegram, OpenAI, за потреби Google Sheets). Докладніше в README кожного демо.
4. Натисни **Execute workflow** для перевірки, потім **Activate**.

## Безпека

У файлах немає ключів і токенів, і їх не можна додавати в репозиторій. Токен Telegram-бота, API-ключ OpenAI та chat_id зберігаються лише в credentials самого n8n. Перед завантаженням власних змін перевіряй, що в експортованих JSON немає секретів.

## Примітка

Файли `demo.mp4` і `demo.gif` — це анімації схем воркфлоу, а не записи екрана. Реальні скриншоти та записи роботи можна додати в папку кожного демо після запуску в n8n.

## Автор

Ірина Калин
