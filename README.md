**Проект "Сервер авторизации и аутентификации на основе событий и CQRS с использованием Axon Framework"**

**Описание проекта**

Этот проект представляет собой серверную часть системы авторизации и аутентификации, построенную на основе принципов событийного программирования (Event Sourcing) и шаблона команд и запросов (CQRS). В проекте используется Axon Framework для управления событиями, командами и запросами.

**Требования**

_Java 17_

_Axon Server_ (версия 2013.1.2)

_База данных H2_ (версия 1.4.200)

**Установка и настройка**

**Клонируйте репозиторий:**

git clone https://github.com/zipepic/Project.git

**Перейдите в директорию проекта:**


cd Project

Настройте файлы конфигурации, включая параметры подключения к базе данных, настройки безопасности и другие необходимые параметры.

**Запустите приложение:**

./mvnw run

Или используйте вашу среду разработки для запуска приложения.

**Использование**

_Эндпоинт для Аутентификации_

POST /auth/login

Этот эндпоинт используется для аутентификации пользователя и генерации токена доступа.

**Параметры запроса:**

username: Имя пользователя

password: Пароль пользователя

tokenType: Тип токена (например, "Bearer")

Пример запроса:

POST /auth/login

Content-Type: application/x-www-form-urlencoded

username=exampleUser&password=examplePassword&tokenType=Bearer

Пример ответа (в случае успешной аутентификации):

{
"accessToken": "exampleAccessToken",
"refreshToken": "exampleRefreshToken"
}

**Контакты**

_zipepic Konstantin Kokoshnikov_
email: kokoshnikov.k@bk.ru

Мы приветствуем вклады, исправления ошибок и предложения улучшений. Пожалуйста, создавайте issues и pull requests в этом репозитории.

Спасибо за использование нашего проекта!
