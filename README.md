> ⚠️ **ВНИМАНИЕ: Этот репозиторий устарел**  
> Поддержка шаблона для `aiogram 2.x` более не ведётся.  
> Мы рекомендуем перейти на новую актуальную версию для **Aiogram 3.x**:  
> 🔗 [Новый репозиторий — Sample-Template-Aiogram-3.x](https://github.com/AlgorithmAlchemy/Sample-Template-Aiogram-3.x)

# 🤖 Aiogram 2.x Template

**Современный модульный шаблон для создания Telegram ботов на aiogram 2.x**

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://python.org)
[![Aiogram](https://img.shields.io/badge/Aiogram-3.20.0-green.svg)](https://aiogram.dev)
[![Peewee](https://img.shields.io/badge/Peewee-ORM-orange.svg)](https://docs.peewee-orm.com)
[![APScheduler](https://img.shields.io/badge/APScheduler-Scheduler-red.svg)](https://apscheduler.readthedocs.io)
[![SQLite](https://img.shields.io/badge/SQLite-Database-lightgrey.svg)](https://sqlite.org)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

## 🚀 Особенности.

- **Модульная архитектура** с классовыми структурами
- **Готовая система администраторов** с правами доступа
- **Полноценная база данных** с моделями пользователей, настроек и статистики
- **Система модерации** с банами, мутами и предупреждениями
- **Inline клавиатуры** с callback обработчиками
- **Планировщик задач** для автоматических операций
- **Логирование** с настраиваемыми уровнями
- **Безопасность** с защитой конфиденциальных данных
- **Готовые команды** для быстрого старта

## 🛠 Технологии

- **Python 3.8+**
- **Aiogram 2.25.2** - современный асинхронный фреймворк
- **SQLite + Peewee ORM** - легкая база данных с ORM
- **APScheduler** - планировщик задач
- **python-dotenv** - управление переменными окружения
- **Redis** - опциональное хранилище состояний

## 📦 Быстрый старт

### 1. Клонирование репозитория
```bash
git clone https://github.com/your-username/aiogram-2x-template.git
cd aiogram-2x-template
```

### 2. Установка зависимостей
```bash
pip install -r requirements.txt
```

### 3. Настройка конфигурации
```bash
cp env.example .env
# Отредактируйте .env файл, добавив свои данные
```

### 4. Запуск бота
```bash
python main.py
```

## 🔒 Безопасность

**ВАЖНО**: Никогда не коммитьте файл `.env` в репозиторий!

### Настройка переменных окружения:

1. **Скопируйте** `env.example` в `.env`
2. **Заполните** в `.env` ваши реальные данные:
   - `BOT_TOKEN` - токен от @BotFather
   - `OWNER_IDS` - ID администраторов (через запятую)
   - `CHAT_ID` - ID чата/группы
   - `SUPPORT_USERNAME` - username поддержки

### Получение необходимых данных:

- **Токен бота**: @BotFather → `/newbot`
- **ID пользователя**: @userinfobot
- **ID группы**: @getidsbot

## 📂 Структура проекта

```
├── data/
│   ├── config.py          # Конфигурация с классовыми структурами
│   └── image/             # Изображения и медиафайлы
├── handlers/
│   ├── users/             # Обработчики для пользователей
│   │   ├── message/       # Обработчики сообщений
│   │   │   ├── start.py   # Команды /start, /menu, /about и др.
│   │   │   ├── admin_commands.py  # Админские команды
│   │   │   └── user_commands.py   # Пользовательские команды
│   │   └── callback/      # Обработчики callback кнопок
│   ├── groups/            # Обработчики для групп
│   ├── supergroups/       # Обработчики для супергрупп
│   └── errors/            # Обработчики ошибок
├── keyboards/
│   ├── inline/            # Inline клавиатуры
│   │   ├── keyboards.py   # Классы клавиатур
│   │   └── __init__.py
│   └── reply/             # Reply клавиатуры
├── models/
│   ├── user.py            # Модели пользователей, настроек, статистики
│   └── sqlite3_creator.py # Создание базы данных
├── states/                # FSM состояния
├── utils/                 # Утилиты и вспомогательные функции
├── filters/               # Фильтры для обработчиков
│   ├── admin_filter.py    # Фильтры для администраторов
│   └── user_filter.py     # Фильтры для пользователей
├── loader.py              # Инициализация бота и диспетчера
├── main.py                # Точка входа с менеджером бота
├── requirements.txt       # Зависимости
├── .env.example           # Пример конфигурации
├── .gitignore             # Исключения Git
└── README.md              # Документация
```

## 🎯 Основные команды

### Пользовательские команды (15+):
- `/start` - Запустить бота и показать главное меню
- `/menu` - Показать главное меню
- `/help` - Показать справку
- `/about` - Информация о боте
- `/profile` - Показать ваш профиль
- `/settings` - Открыть настройки
- `/commands` - Показать все команды
- `/feedback` - Отправить отзыв
- `/support` - Связаться с поддержкой
- `/version` - Версия бота
- `/status` - Статус бота
- `/ping` - Проверить соединение
- `/uptime` - Время работы бота

### Админские команды:
- `/ban_user` - Забанить пользователя
- `/unban_user` - Разбанить пользователя
- `/warn_user` - Предупредить пользователя
- `/stats` - Статистика бота
- `/users` - Список пользователей
- `/broadcast` - Отправить рассылку
- `/backup` - Создать резервную копию
- `/restore` - Восстановить из резервной копии
- `/logs` - Показать логи
- `/restart` - Перезапустить бота

## 🔧 Настройка и кастомизация

### Добавление новых команд:
1. Создайте обработчик в `handlers/users/message/`
2. Используйте классовую структуру как в примерах
3. Зарегистрируйте обработчик в конце файла

### Создание новых клавиатур:
1. Добавьте метод в соответствующий класс в `keyboards/inline/keyboards.py`
2. Создайте обработчик в `handlers/users/callback/`
3. Используйте в нужных обработчиках

### Работа с базой данных:
1. Создайте модель в `models/`
2. Используйте Peewee ORM для запросов
3. Не забудьте создать миграции

## 🚀 Развертывание

### Локальная разработка:
```bash
python main.py
```

### Продакшн (с Redis):
1. Установите Redis
2. Настройте переменные Redis в `.env`
3. Запустите с помощью systemd или supervisor

### Docker (опционально):
```bash
docker build -t aiogram-bot .
docker run -d --name bot aiogram-bot
```

## 📝 Примеры использования

### Создание простого обработчика:
```python
from aiogram import types
from loader import dp

@dp.message_handler(commands=['hello'])
async def hello_handler(message: types.Message):
    await message.answer("Привет! 👋")
```

### Создание inline клавиатуры:
```python
from keyboards.inline.keyboards import KeyboardBuilder

def get_example_keyboard():
    buttons = [
        [
            {'text': 'Кнопка 1', 'callback_data': 'btn_1'},
            {'text': 'Кнопка 2', 'callback_data': 'btn_2'}
        ]
    ]
    return KeyboardBuilder.create_keyboard(buttons)
```

### Работа с FSM:
```python
from aiogram.dispatcher import FSMContext
from aiogram.dispatcher.filters.state import State, StatesGroup

class ExampleStates(StatesGroup):
    waiting_for_input = State()

@dp.message_handler(state=ExampleStates.waiting_for_input)
async def process_input(message: types.Message, state: FSMContext):
    await state.finish()
    await message.answer("Спасибо за ввод!")
```

## 🤝 Вклад в проект

1. Fork репозитория
2. Создайте ветку для новой функции (`git checkout -b feature/amazing-feature`)
3. Commit изменения (`git commit -m 'Add amazing feature'`)
4. Push в ветку (`git push origin feature/amazing-feature`)
5. Откройте Pull Request

## 📄 Лицензия

Этот проект распространяется под лицензией MIT. См. файл `LICENSE` для получения дополнительной информации.

## 🆘 Поддержка

Если у вас есть вопросы или проблемы:

- 📧 Создайте Issue в GitHub
- 💬 Обратитесь к документации aiogram
- 🔗 Присоединитесь к сообществу aiogram

---

**Создано с ❤️ для сообщества aiogram**
