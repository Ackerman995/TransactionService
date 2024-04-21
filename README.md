# Payment Service

RESTful приложение. Сервис прототип микросервиса, который будет интегрирован в существующую банковскую систему.

Transaction:
для приема транзакций (условно интеграция с банковскими сервисами)
получение списка транзакций, превысивших лимит.

Limit - клиентский, для внешних запросов от клиента:
установление нового лимита,
получение всех лимитов.

# Stack
Spring boot, PostgreSQL, Liquibase, Gradle, Hibernate, MapStruct, Swagger, JUnit, Mockito, Lombok, Logback, Docker

# API Documentation
Expense Operations

POST /api/v1/transactions: Submit a new expense transaction.

GET /api/v1/transactions/{accountNumber}/exceeded: Get all limit exceeded transactions.

Monthly Limits

GET /api/v1/limits/{accountNumber}: Get all limits.

PUT /api/v1/limits: Update monthly limit.

# Как запустить
docker-compose build

docker-compose up -d

gradle build

PORT: 9080

SWAGGER - http://localhost:9080/swagger-ui/index.html

# Code
Трехслойная архитектура - Controller, Service, Repository.

Использовал AlphaVantage API для обмена курсов.

Покрыл тестами 70+% кода.

Добавил логирование.
