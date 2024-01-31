# Telegram Bot Backend

Включает в себя: Backend Telegram bot`a "BestExChange bot"

---
Подразумевается, что на компьютере установлены Docker, docker-compose, Git.
Версии, используемые при разработке:
- Docker - 24.0.7
- Git - 2.34.1
---

# Инструкция по сборке проекта

Склонируйте репозиторий к себе:
```
git clone https://github.com/TelegramMiniApps-2023/bestexchange_tg_bot.git
```
Перейдите в папку проекта:
```
cd bestexchange_tg_bot
```
---
Откройте файл .env:
```
nano .env
```

Добавьте в файл .env следующее содержимое:
```
TOKEN=

WEBAPP_URL_ONE=
WEBAPP_URL_TWO=
WEBAPP_URL_THREE=
```

Выйдите и сохраните файл .env:
- нажмите Ctrl + X
- подтвердите изменения нажав Y
- нажмите Enter
---

**Перед сборкой убедитесь, что service Docker активен!**

**Перед сборкой убедитесь, image с именем "tg_bot" не существует!**

---
Соберите Docker образ
```
docker build --tag 'tg_bot' .
```
Запустите контейнер
```
docker run -d 'tg_bot'
```
