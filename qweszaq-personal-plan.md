# Персональный план подготовки к AZ-204 (30 дней)

Этот план разбит на 30 дней и охватывает все ключевые темы экзамена AZ-204, включая теорию, практические задания и прохождение квизов. План составлен с учетом [официального руководства Microsoft (Study Guide)](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/az-204) и актуальных требований к экзамену.

## Распределение тем на экзамене (Skills Measured)
* **Develop Azure compute solutions** (25–30%)
* **Develop for Azure storage** (15–20%)
* **Implement Azure security** (15–20%)
* **Monitor, troubleshoot, and optimize Azure solutions** (5–10%)
* **Connect to and consume Azure services and third-party services** (20–25%)

---

## Неделя 1: Вычислительные решения (Compute Solutions) - 25-30% экзамена
**Цель:** Изучить основные вычислительные сервисы Azure. Это самая объемная часть экзамена.

* **День 1:** Введение в Azure Compute. Изучение [Compute Solutions](./Topics/Compute%20Solutions.md).
* **День 2:** Контейнеры в Azure. Изучение [Containers](./Topics/Containers.md). 
  * *Что нужно знать:* Создание образов, публикация в Azure Container Registry (ACR), запуск в Azure Container Instances (ACI) и Azure Container Apps (ACA).
  * *Практика:* Развертывание контейнера (см. папку `Exercises/`).
* **День 3:** Azure App Service (Часть 1). Изучение [App Service](./Topics/App%20Service.md).
  * *Что нужно знать:* Создание Web App, деплой кода и контейнеров, настройка TLS, API settings.
* **День 4:** Azure App Service (Часть 2). 
  * *Что нужно знать:* Настройка диагностики и логирования, автомасштабирование (autoscaling), слоты развертывания (deployment slots).
  * *Практика:* Прохождение квиза по App Service.
* **День 5:** Azure Functions (Часть 1). Изучение [Functions](./Topics/Functions.md).
  * *Что нужно знать:* Создание и настройка Function app, триггеры (data operations, timers, webhooks).
* **День 6:** Azure Functions (Часть 2). 
  * *Что нужно знать:* Реализация input и output bindings, Durable Functions.
  * *Практика:* Создание функции через VS Code.
* **День 7:** Повторение недели 1. Прохождение Knowledge Check по Compute и Functions.

## Неделя 2: Хранилища данных (Storage) - 15-20% экзамена
**Цель:** Освоить работу с Blob Storage и Cosmos DB.

* **День 8:** Azure Blob Storage (Часть 1). Изучение [Blob Storage](./Topics/Blob%20Storage.md).
  * *Что нужно знать:* Установка и получение свойств и метаданных, политики хранения и управление жизненным циклом данных (lifecycle management).
* **День 9:** Azure Blob Storage (Часть 2). 
  * *Что нужно знать:* Выполнение операций с данными с использованием SDK.
  * *Практика:* Работа с .NET SDK для Blob Storage. Прохождение квиза.
* **День 10:** Azure Cosmos DB (Часть 1). Изучение [Cosmos DB](./Topics/Cosmos%20DB.md).
  * *Что нужно знать:* Выбор правильного уровня согласованности (consistency level), партиционирование.
* **День 11:** Azure Cosmos DB (Часть 2). 
  * *Что нужно знать:* Операции с контейнерами и элементами через SDK, реализация уведомлений change feed.
  * *Практика:* Создание ресурсов Cosmos DB. Прохождение квиза.
* **День 12:** Введение в безопасность (Начало 15-20% блока). Изучение [Entra ID](./Topics/Entra%20ID.md) и [Managed Identities](./Topics/Managed%20Identities.md).
  * *Что нужно знать:* Аутентификация и авторизация пользователей и приложений через Microsoft Entra ID, реализация Managed Identities для ресурсов Azure.
* **День 13:** Microsoft Graph API и Microsoft Identity platform. Изучение [Graph](./Topics/Graph.md). 
  * *Что нужно знать:* Взаимодействие с Microsoft Graph, аутентификация через Microsoft Identity platform.
  * *Практика:* Интерактивная аутентификация MSAL.NET.
* **День 14:** Повторение недели 2. Прохождение Knowledge Check по Storage.

## Неделя 3: Безопасность (Окончание) и Мониторинг (5-10% экзамена)
**Цель:** Завершить темы безопасности и научиться мониторить приложения.

* **День 15:** Управление секретами. Изучение [Key Vault](./Topics/Key%20Vault.md). 
  * *Что нужно знать:* Разработка кода, использующего ключи, секреты и сертификаты из Key Vault.
  * *Практика:* Сохранение и получение секретов через Azure CLI.
* **День 16:** Конфигурация приложений. Изучение [App Configuration](./Topics/App%20Configuration.md).
  * *Что нужно знать:* Безопасное хранение конфигурации с помощью Azure App Configuration.
* **День 17:** Доступ к хранилищам. Изучение [Shared Access Signatures (SAS)](./Topics/Shared%20Access%20Signatures.md).
  * *Что нужно знать:* Создание и реализация SAS.
* **День 18:** Мониторинг и оптимизация. Изучение [Application Insights](./Topics/Application%20Insights.md).
  * *Что нужно знать:* Мониторинг метрик, логов и трейсов, реализация тестов доступности (availability tests) и алертов.
* **День 19:** Инструментирование приложений. 
  * *Что нужно знать:* Как добавить Application Insights в приложение или сервис.
  * *Практика:* Настройка Application Insights в тестовом проекте.
* **День 20:** Кэширование и доставка контента. Изучение [Cache for Redis](./Topics/Cache%20for%20Redis.md) и [Content Delivery Network](./Topics/Content%20Delivery%20Network.md).
* **День 21:** Повторение недели 3. Прохождение квизов по Security и Monitoring.

## Неделя 4: Интеграция сервисов и Обмен сообщениями (20-25% экзамена)
**Цель:** Изучить API Management, события и очереди сообщений.

* **День 22:** Управление API. Изучение [API Management](./Topics/API%20Management.md).
  * *Что нужно знать:* Создание инстанса APIM, создание и документирование API, настройка доступа, реализация политик (policies).
* **День 23:** Событийно-ориентированная архитектура. Изучение [Event Grid](./Topics/Event%20Grid.md). 
  * *Что нужно знать:* Разработка решений на базе Azure Event Grid.
  * *Практика:* Маршрутизация событий.
* **День 24:** Потоковая передача данных. Изучение [Event Hub](./Topics/Event%20Hub.md).
  * *Что нужно знать:* Разработка решений на базе Azure Event Hubs.
* **День 25:** Очереди сообщений (Часть 1). Изучение [Service Bus](./Topics/Service%20Bus.md). 
  * *Что нужно знать:* Разработка решений на базе Azure Service Bus.
  * *Практика:* Отправка и получение сообщений.
* **День 26:** Очереди сообщений (Часть 2). Изучение [Queue Storage](./Topics/Queue%20Storage.md). 
  * *Что нужно знать:* Разработка решений на базе Azure Queue Storage. Сравнение Service Bus и Queue Storage.
* **День 27:** Повторение недели 4. Прохождение квизов по Integration и Messaging.

## Финальные дни: Практика и Симуляция экзамена
**Цель:** Закрепить знания, выполнить оставшиеся лабораторные и пройти все тесты.

* **День 28:** Глубокая практика. Работа с [AZ CLI](./Topics/AZ%20CLI.md) и порталом. Выполнение оставшихся заданий из папки `Exercises/`.
* **День 29:** Повторение слабых мест. Просмотр [NOTES.md](./NOTES.md) и [Synopsis.md](./Synopsis.md). Повторное прохождение сложных квизов в `quiz-app`.
* **День 30:** Симуляция экзамена. Прохождение всех доступных Knowledge Checks и финальный прогон вопросов из папки `Questions/`.

---
**Полезные ссылки для подготовки:**
* [Официальный Study Guide AZ-204](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/az-204)
* [Официальная страница сертификации AZ-204](https://learn.microsoft.com/en-us/credentials/certifications/azure-developer/)
* [Репозиторий с лабораторными работами от Microsoft](https://github.com/MicrosoftLearning/AZ-204-DevelopingSolutionsforMicrosoftAzure)

**Ежедневная рутина:**
1. Читать теорию по теме дня.
2. Выполнять соответствующую практику (если есть).
3. Запускать `quiz-app` и проходить вопросы по пройденной теме.
