 # pz9-auth

Минимальный сервис аутентификации с регистрацией и входом пользователей, реализованный на Go с использованием bcrypt для безопасного хранения паролей.

<b>Структура проекта</b>
<br>
<img src="screen/Снимок экрана 2025-11-18 232355.png">


Функциональность
    POST /auth/register - регистрация нового пользователя.
    POST /auth/login - аутентификация пользователя.
    Безопасное хэширование паролей с использованием bcrypt.
    Валидация входных данных.
    Работа с PostgreSQL через GORM.

Установка и запуск

1. Клонирование и инициализация проекта:

```bash
mkdir pz9-auth && cd pz9-auth
go mod init example.com/pz9-auth
```

2. Установка зависимостей:

```bash

go get github.com/go-chi/chi/v5
go get gorm.io/gorm gorm.io/driver/postgres
go get golang.org/x/crypto/bcrypt
```

3. Настройка переменных окружения:
```bash
# Windows PowerShell
setx DB_DSN "postgres://user:pass@localhost:5432/pz9?sslmode=disable"
setx BCRYPT_COST "12"
setx APP_ADDR ":8080"

# macOS/Linux
export DB_DSN="postgres://user:pass@localhost:5432/pz9?sslmode=disable"
export BCRYPT_COST=12
export APP_ADDR=":8080"
```

4. Запуск приложения:
```bash

go run cmd/api/main.go
```

<img src="screen/Снимок экрана 2025-11-18 231113.png">

<img src="screen/Снимок экрана 2025-11-18 231451.png">

<img src="screen/Снимок экрана 2025-11-18 231240.png">

<img src="screen/Снимок экрана 2025-11-18 231310.png">

<img src="screen/Снимок экрана 2025-11-18 232017.png">
