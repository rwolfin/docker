# 🐳 Docker

Полностью готовая площадка для разработки на базе **Docker Compose**.  
Включает отдельные контейнеры для:  

- 🌐 **Nginx** — веб-сервер  
- 🐘 **PHP-FPM (8.2)** — обработка PHP-кода  
- 🗄️ **MySQL (8.0)** — база данных  

---

## 📂 Структура проекта

```
docker/
├── docker-compose.yml
├── nginx/
│   ├── Dockerfile
│   └── default.conf
├── php/
│   ├── Dockerfile
│   └── php.ini
├── mysql/
│   ├── Dockerfile
│   └── my.cnf
└── src/
    ├── index.php
    ├── phpinfo.php
    └── test_db.php
```

---

## ⚙️ Запуск проекта

1. Установи и запусти **Docker Desktop** 🐳  
2. Клонируй репозиторий:
   ```bash
   git clone https://github.com/rwolfin/project.git
   cd project
   ```
3. Подними контейнеры:
   ```bash
   docker compose build
   docker compose up -d
   ```
4. Пропиши в `hosts`:
   ```
   127.0.0.1 application.local
   ```
5. Открой в браузере 👉 [http://application.local](http://application.local)  

---

## 🖥️ Доступные страницы

- `/` → приветствие 🎉  
- `/phpinfo.php` → информация о PHP ⚙️  

---

## 🔑 MySQL доступы

Подключение из контейнера:
```bash
docker exec -it mysql_app mysql -u root -p
```

---

## 📌 Примечания

- ✨ Можно менять настройки PHP в `php/php.ini`  
- ⚡ MySQL принимает подключения снаружи (`bind-address=0.0.0.0`)  
- 🔧 Все контейнеры объединены в общую сеть `app-network`  

---


## 👨‍💻 Для Школы Skillfactory

Разработано с ❤️ для учебных и рабочих проектов.  
