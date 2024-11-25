![React](https://img.shields.io/badge/react-%2320232a.svg?style=for-the-badge&logo=react&logoColor=%2361DAFB)
![React Router](https://img.shields.io/badge/React_Router-CA4245?style=for-the-badge&logo=react-router&logoColor=white)
![Nginx](https://img.shields.io/badge/nginx-%23009639.svg?style=for-the-badge&logo=nginx&logoColor=white)
![NodeJS](https://img.shields.io/badge/node.js-6DA55F?style=for-the-badge&logo=node.js&logoColor=white)
![TypeScript](https://img.shields.io/badge/typescript-%23007ACC.svg?style=for-the-badge&logo=typescript&logoColor=white)
![NestJS](https://img.shields.io/badge/nestjs-%23E0234E.svg?style=for-the-badge&logo=nestjs&logoColor=white)
![Jest](https://img.shields.io/badge/-jest-%23C21325?style=for-the-badge&logo=jest&logoColor=white)
![Postgres](https://img.shields.io/badge/postgres-%23316192.svg?style=for-the-badge&logo=postgresql&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=for-the-badge&logo=Prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/grafana-%23F46800.svg?style=for-the-badge&logo=grafana&logoColor=white)
![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)

# 🎁 **Kupipodariday**

**Kupipodariday** – это проект, который поможет вам эффективно управлять подарками. Включает в себя фронтенд, бэкенд, базу данных и мониторинг, всё это собрано в мощную систему с использованием Docker.

Проект поддерживает автоматическое обновление HTTPS-сертификатов, резервное копирование данных и мониторинг состояния всех ключевых компонентов.

---

## 🌐 **Живой пример**

Проект уже развернут и доступен онлайн. Ознакомьтесь с его работой по следующим адресам:

- **🌍 Основной домен:**  
  🔗 [https://nc-kupipodariday.ru/](https://nc-kupipodariday.ru/)

- **📡 IP-адрес сервера:**  
  `146.0.79.91`

- **🖥️ Frontend:**  
  🔗 [https://nc-kupipodariday.ru/](https://nc-kupipodariday.ru/)

- **⚙️ Backend (API):**  
  🔗 [https://nc-kupipodariday.ru/api](https://nc-kupipodariday.ru/api)

✨ **Загляните на наш сайт, чтобы увидеть проект в действии!**

---

## 📋 **Содержание**

- [🎁 **Kupipodariday**](#-kupipodariday)
  - [🌐 **Живой пример**](#-живой-пример)
  - [📋 **Содержание**](#-содержание)
  - [✨ **Особенности проекта**](#-особенности-проекта)
  - [🛠️ **Технологии**](#️-технологии)
  - [📦 **Установка и запуск**](#-установка-и-запуск)
    - [1. **Клонируйте репозиторий:**](#1-клонируйте-репозиторий)
    - [2. **Создайте файлы конфигурации:**](#2-создайте-файлы-конфигурации)
    - [3. **Соберите и запустите проект:**](#3-соберите-и-запустите-проект)
    - [4. **Проверьте статус контейнеров:**](#4-проверьте-статус-контейнеров)
  - [⚙️ **Настройка**](#️-настройка)
    - [Настройка HTTPS](#настройка-https)
    - [Настройка мониторинга](#настройка-мониторинга)
  - [📜 **Полезные команды**](#-полезные-команды)
  - [📊 **Мониторинг и администрирование**](#-мониторинг-и-администрирование)
  - [🚀 **Дополнительные функции**](#-дополнительные-функции)
  - [📞 **Контакты**](#-контакты)

---

## ✨ **Особенности проекта**

- 🖥️ **Frontend**: Современный интерфейс на React с быстрой отдачей через NGINX.
- ⚙️ **Backend**: Масштабируемая API на NestJS и TypeScript с тестами на Jest.
- 🗄️ **Database**: Надёжная база данных PostgreSQL с автоматическими бэкапами.
- 📈 **Monitoring**: Мониторинг состояния через Prometheus и Grafana.
- 🔒 **Безопасность**: Поддержка HTTPS с автоматическим обновлением сертификатов.
- 🚀 **Автономность**: Проект разворачивается за пару минут с помощью Docker Compose.

---

## 🛠️ **Технологии**

Проект построен на следующих технологиях:

| Компонент      | Технология                        |
| -------------- | --------------------------------- |
| **Frontend**   | React.js, NGINX                   |
| **Backend**    | Node.js, TypeScript, NestJS, Jest |
| **Database**   | PostgreSQL                        |
| **Monitoring** | Prometheus, Grafana               |
| **DevOps**     | Docker Compose, Certbot           |

---

## 📦 **Установка и запуск**

### 1. **Клонируйте репозиторий:**

```bash
git clone https://github.com/NotACat1/kupipodariday.git
cd kupipodariday
```

### 2. **Создайте файлы конфигурации:**

Создайте `.env` и `.env.deploy`.  
Пример содержимого `.env`:

```env
# -----------------------------
# 🌐 Общая конфигурация проекта
# -----------------------------

# PostgreSQL (База данных)
DB_HOST=db                    # Хост базы данных (контейнер Docker)
DB_CPU_LIMIT=0.5              # Лимит процессорного времени для PostgreSQL
DB_MEM_LIMIT=512M             # Ограничение памяти для PostgreSQL
POSTGRES_DB=kupipodariday     # Имя базы данных
POSTGRES_USER=your_db_user    # 🔑 Укажите пользователя для базы данных
POSTGRES_PASSWORD=your_db_password  # 🛡️ Замените на надёжный пароль

# Frontend (Клиентская часть)
FRONTEND_HOST=frontend        # Хост для фронтенда (контейнер Docker)
FRONTEND_CPU_LIMIT=0.5        # Лимит процессорного времени для фронтенда
FRONTEND_MEM_LIMIT=512M       # Ограничение памяти для фронтенда

# Backend (Серверная часть)
BACKEND_HOST=api              # Хост для бэкенда (контейнер Docker)
BACKEND_CPU_LIMIT=1           # Лимит процессорного времени для бэкенда
BACKEND_MEM_LIMIT=1024M       # Ограничение памяти для бэкенда
JWT_SECRET=your_jwt_secret_key  # 🔑 Укажите секретный ключ для токенов
JWT_EXPIRATION=1h             # Срок действия токена (например, 1 час)
BCRYPT_SALT_ROUNDS=10         # Количество раундов хеширования паролей

# -----------------------------
# 📡 Порты для сервисов
# -----------------------------
FRONTEND_PORT=3000            # Порт для фронтенда
BACKEND_PORT=5000             # Порт для бэкенда
DB_PORT=5432                  # Порт для PostgreSQL
PROMETHEUS_PORT=9090          # Порт для Prometheus
GRAFANA_PORT=3002             # Порт для Grafana
NGINX_PORT=80                 # Порт для NGINX
PGADMIN_PORT=8080             # Порт для pgAdmin

# -----------------------------
# 📊 Мониторинг
# -----------------------------
GRAFANA_USER=grafana_admin    # Имя пользователя Grafana
GRAFANA_PASSWORD=secure_password  # 🛡️ Надёжный пароль для Grafana

# -----------------------------
# 🛠️ Управление базой данных
# -----------------------------
PGADMIN_EMAIL=admin@example.com   # 📧 Email администратора для pgAdmin
PGADMIN_PASSWORD=pgadmin_password # 🛡️ Пароль администратора для pgAdmin

# -----------------------------
# 🔐 Безопасность
# -----------------------------
DOMAIN=nc-kupipodariday.ru    # Домен вашего проекта
EMAIL=your_email@example.com  # 📧 Email для уведомлений и SSL
```

Пример содержимого `.env.deploy`:

```env
# -----------------------------
# 🖥️ Параметры сервера
# -----------------------------
USER=root                     # Имя пользователя для подключения к серверу
SERVER_IP=192.168.1.1         # IP-адрес вашего сервера
DEPLOY_PATH=/var/www/kupipodariday  # Путь для развертывания проекта

# -----------------------------
# 🛠️ Репозиторий и ветка
# -----------------------------
GITHUB_REPO=git@github.com:username/kupipodariday.git  # 🔗 URL вашего репозитория
GITHUB_BRANCH=main            # Ветка, из которой выполняется деплой

# -----------------------------
# 🔐 SSL Сертификаты
# -----------------------------
DOMAIN=nc-kupipodariday.ru    # Ваш домен
EMAIL=your_email@example.com  # 📧 Email для генерации SSL-сертификатов

# -----------------------------
# 🔑 SSH Ключи
# -----------------------------
SSH_GITHUB=/path/to/github_deploy_key  # 🗝️ Путь к SSH-ключу для GitHub
SSH_SERVER=/path/to/server_ssh_key     # 🗝️ Путь к SSH-ключу для сервера
```

### 3. **Соберите и запустите проект:**

```bash
docker-compose up -d
```

### 4. **Проверьте статус контейнеров:**

```bash
docker-compose ps
```

---

## ⚙️ **Настройка**

### Настройка HTTPS

Для безопасной работы проекта с HTTPS используется **Certbot**. Сертификаты автоматически обновляются через cron.

Пример задания в cron для еженедельного обновления сертификатов:

```bash
0 3 * * 7 ./scripts/ssl_cert.sh
```

### Настройка мониторинга

**Prometheus** и **Grafana** предустановлены и запускаются в отдельных контейнерах.

- **Prometheus:** доступен по адресу `http://<ваш-домен>:9090`
- **Grafana:** доступен по адресу `http://<ваш-домен>:3002`

---

## 📜 **Полезные команды**

| Команда                         | Описание                                           | Способ вызова                         |
| ------------------------------- | -------------------------------------------------- | ------------------------------------- |
| **`backup_db.sh`**              | Создаёт бэкап базы данных и сохраняет его локально | `./scripts/backup_db.sh`              |
| **`connect.sh`**                | Подключается к серверу по SSH                      | `./scripts/connect.sh`                |
| **`deploy.sh`**                 | Разворачивает проект на сервере                    | `./scripts/deploy.sh`                 |
| **`docker_containers_info.sh`** | Отображает информацию о контейнерах Docker         | `./scripts/docker_containers_info.sh` |
| **`setup_passwordless_ssh.sh`** | Настраивает SSH-доступ без пароля                  | `./scripts/setup_passwordless_ssh.sh` |
| **`setup_ssh.sh`**              | Настраивает SSH-ключи для сервера и GitHub         | `./scripts/setup_ssh.sh`              |
| **`ssl_cert.sh`**               | Обновляет SSL-сертификаты на сервере               | `./scripts/ssl_cert.sh`               |
| **`start.sh`**                  | Запускает проект на сервере                        | `./scripts/start.sh`                  |
| **`stop.sh`**                   | Останавливает проект на сервере                    | `./scripts/stop.sh`                   |
| **`update_env.sh`**             | Обновляет файл `.env` на сервере                   | `./scripts/update_env.sh`             |
| **`update.sh`**                 | Обновляет проект на сервере                        | `./scripts/update.sh`                 |

---

## 📊 **Мониторинг и администрирование**

- **Prometheus**: Мониторинг системных метрик.
- **Grafana**: Настраиваемые дашборды для визуализации данных.
- **Docker Compose**: Лёгкое управление всеми контейнерами из одного файла.

Для доступа к метрикам просто откройте соответствующие адреса в браузере.

---

## 🚀 **Дополнительные функции**

1. **Автоматические бэкапы базы данных:**  
   Ежедневный бэкап настроен через cron.

   ```bash
   0 2 * * * ./scripts/backup_db.sh
   ```

2. **Лёгкое обновление проекта:**  
   Используйте `deploy.sh`, чтобы обновить проект на сервере:

   ```bash
   ./scripts/deploy.sh
   ```

3. **Безопасная работа с ключами:**  
   SSH-ключи для сервера и GitHub надёжно защищены.

---

## 📞 **Контакты**

📧 Email: [notacat.mail@gmail.com](mailto:notacat.mail@gmail.com)  
🐱 GitHub: [NotACat1](https://github.com/NotACat1)

💡 Если у вас есть идеи или предложения по улучшению проекта, будем рады вашим сообщениям!

---

✨ **Спасибо за интерес к нашему проекту!**
💡 _Если у вас есть вопросы или предложения, не стесняйтесь обращаться!_
