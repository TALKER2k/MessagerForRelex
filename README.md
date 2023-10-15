# Пример использования API

Данный репозиторий содержит примеры запросов к API нашего проекта. Здесь представлены различные запросы и их описания.

## Регистрация пользователя

### Запрос
```http
POST http://localhost:8089/api/auth/signup
{
    "username": "userTest",
    "email": "userTest@mail.com",
    "password": "12345678"
}

### Регистрация пользователя
```http
POST http://localhost:8089/api/auth/signup
{
    "username": "userTest",
    "email": "userTest@mail.com",
    "password": "12345678"
}
```

### Вход пользователя
```http
POST http://localhost:8089/api/auth/signin
{
    "username": "userTest",
    "password": "12345678"
}

```

### Выход пользователя
```http
POST http://localhost:8089/api/auth/signout
```

### Получение информации о пользователе (модере, админе)
```http
GET http://localhost:8089/api/test/user
GET http://localhost:8089/api/test/mod
GET http://localhost:8089/api/test/admin
```

### Изменение пароля пользователя
```http
POST http://localhost:8089/api/profile/settings/password
{
    "newPassword": "123123"
}
```

### Изменение основной информации о пользователе
```http
POST http://localhost:8089/api/profile/settings/main
{
    "username": "user",
    "firstname": "",
    "lastname": "",
    "email": ""
}
```

### Удаление аккаунта пользователя
```http
DELETE http://localhost:8089/api/profile/settings/delete
```

### Активация аккаунта
```http
POST http://localhost:8089/api/auth/activate
{
    "username": "userTest"
}
```

### Отправка сообщения
```http
POST http://localhost:8089/api/message/send
{
    "username": "user",
    "message": "Hello my friend!"
}
```

### Отображение сообщений
```http
POST http://localhost:8089/api/message/show
{
    "username": "user"
}
```

### Удаление сообщения
```http
DELETE http://localhost:8089/api/message/delete
```