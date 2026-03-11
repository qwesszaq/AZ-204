# Персональный план подготовки к AZ-204 (30 дней)

Этот план сделан “как маршрут”: на каждый день есть четкие **цели (что уметь на экзамене)**, **точечные ссылки на официальные страницы**, **что прочитать в этом репозитории**, **какую практику сделать** и **как себя проверить**.

Официальная матрица навыков (Skills Measured, актуальная версия):
- Study guide AZ-204: https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/az-204

Вес тем на экзамене (ориентир):
- Develop Azure compute solutions — 25–30%
- Develop for Azure storage — 15–20%
- Implement Azure security — 15–20%
- Monitor, troubleshoot, and optimize Azure solutions — 5–10%
- Connect to and consume Azure services and third-party services — 20–25%

## Как работать по плану (одинаково каждый день)
**Время:** 2–3 часа в будни, 3–5 часов в выходные (можно меньше, но тогда растянется).

**Шаблон дня (Definition of Done):**
1) Прочитал “что уметь” и выписал 5–10 тезисов в свои заметки.
2) Прочитал локальные конспекты из [Topics/](./Topics/).
3) Открыл 1–3 официальные страницы Docs и разобрал примеры/термины.
4) Сделал 1 упражнение из [Exercises/](./Exercises/) (или мини‑практику в Portal/CLI).
5) Самопроверка: квиз в [quiz-app/](./quiz-app/) + 10–20 вопросов из [Questions/](./Questions/).

**Как использовать квизы:**
- Локально: `cd quiz-app && npm run dev` → http://localhost:5173
- Или hosted версия: https://az-204.vercel.app/ (есть “by topic”)

---

## Неделя 1 — Compute (самая “дорогая” тема)

### День 1 — Каркас экзамена + базовые инструменты
**Цель (что уметь):**
- Понимать, какие типы задач покрывает AZ-204 (compute/storage/security/monitor/integration).
- Уметь быстро делать базовые операции через Portal и Azure CLI.

**Репозиторий (прочитать):**
- [README.md](./README.md) (разделы Skills measured + resources)
- [NOTES.md](./NOTES.md) (Exam strategies)
- [Topics/Resource Group.md](./Topics/Resource%20Group.md), [Topics/AZ CLI.md](./Topics/AZ%20CLI.md), [Topics/Azure Portal.md](./Topics/Azure%20Portal.md)
- [Learning Path/README.md](./Learning%20Path/README.md) (список модулей/путей, по сути “курс” внутри репо)

**Официально (точечные ссылки):**
- Azure CLI overview: https://learn.microsoft.com/en-us/cli/azure/
- Azure Resource Manager overview: https://learn.microsoft.com/en-us/azure/azure-resource-manager/management/overview

**Практика:**
- Создать ресурс‑группу и вывести список ресурсов (Portal + `az group create`, `az resource list`).

**Самопроверка:**
- Пройти 10–20 вопросов из [Questions/AZ CLI.md](./Questions/AZ%20CLI.md) и [Questions/Azure.md](./Questions/Azure.md).

### День 2 — Контейнеры: основы + ACR (Container Registry)
**Цель (что уметь):**
- Разница образ/контейнер, registry, tag, digest.
- Создать/собрать образ, залогиниться в ACR, запушить образ.
- Понимать ACR Tasks: когда выгоднее билдить в облаке.

**Репозиторий:**
- [Topics/Containers.md](./Topics/Containers.md)
- [Learning Path/Containers.md](./Learning%20Path/Containers.md)

**Официально:**
- ACR overview: https://learn.microsoft.com/en-us/azure/container-registry/container-registry-intro
- ACR Tasks overview: https://learn.microsoft.com/en-us/azure/container-registry/container-registry-tasks-overview
- Quickstart (ACR + CLI): https://learn.microsoft.com/en-us/azure/container-registry/container-registry-get-started-azure-cli

**Практика (из Exercises):**
- [Exercises/Build and run a container image by using Azure Container Registry Tasks/README.md](./Exercises/Build%20and%20run%20a%20container%20image%20by%20using%20Azure%20Container%20Registry%20Tasks/README.md)

**Самопроверка:**
- [Knowledge Check/Containers.md](./Knowledge%20Check/Containers.md)
- В [quiz-app/](./quiz-app/) пройти тему Containers (или блок вопросов по контейнерам).

### День 3 — Контейнеры: ACI vs Container Apps
**Цель (что уметь):**
- Когда выбирать ACI (простые одноразовые/джобы) vs Container Apps (микросервисы, revisions, scale to zero).
- Базовый деплой контейнера в ACI и в Container Apps.

**Репозиторий:**
- [Topics/Containers.md](./Topics/Containers.md) (часть про ACI/ACA)
- [Learning Path/Containers.md](./Learning%20Path/Containers.md) (как “лекция” по контейнерному блоку)

**Официально:**
- ACI overview: https://learn.microsoft.com/en-us/azure/container-instances/container-instances-overview
- Container Apps overview: https://learn.microsoft.com/en-us/azure/container-apps/overview
- Container Apps revisions: https://learn.microsoft.com/en-us/azure/container-apps/revisions

**Практика (из Exercises):**
- [Exercises/Deploy a container instance by using the Azure CLI/README.md](./Exercises/Deploy%20a%20container%20instance%20by%20using%20the%20Azure%20CLI/README.md)
- [Exercises/Deploy a container app/README.md](./Exercises/Deploy%20a%20container%20app/README.md)

**Самопроверка:**
- 15–25 вопросов из [Questions/Containers.md](./Questions/Containers.md).

### День 4 — App Service: создание, конфиги, деплой
**Цель (что уметь):**
- Создать Web App и понять план (SKU), регионы, ограничения.
- Настроить app settings / connection strings, понимать slot settings.
- Варианты деплоя (zip deploy, GitHub Actions, container).

**Репозиторий:**
- [Topics/App Service.md](./Topics/App%20Service.md)
- [Learning Path/App Service.md](./Learning%20Path/App%20Service.md)

**Официально:**
- App Service overview: https://learn.microsoft.com/en-us/azure/app-service/overview
- Configure app settings: https://learn.microsoft.com/en-us/azure/app-service/configure-common
- Deploy to App Service (overview): https://learn.microsoft.com/en-us/azure/app-service/deploy-best-practices

**Практика (из Exercises):**
- [Exercises/Create a static HTML web app by using Azure Cloud Shell/README.md](./Exercises/Create%20a%20static%20HTML%20web%20app%20by%20using%20Azure%20Cloud%20Shell/README.md)
- [Exercises/Create a backend API/README.md](./Exercises/Create%20a%20backend%20API/README.md) (если там App Service/деплой API — отлично ложится)

**Самопроверка:**
- [Knowledge Check/App Service.md](./Knowledge%20Check/App%20Service.md)
- 15–25 вопросов из [Questions/App Service.md](./Questions/App%20Service.md).

### День 5 — App Service: диагностика, слоты, autoscale
**Цель (что уметь):**
- Включить и читать логи (app logs, web server logs) + диагностика.
- Deployment slots: swap, прогрев, как не уронить prod.
- Autoscale: scale out/in vs scale up/down.

**Репозиторий:**
- [Topics/App Service.md](./Topics/App%20Service.md)
- [NOTES.md](./NOTES.md) (подсказки про scaling и “update vs create”)
- [Learning Path/App Service.md](./Learning%20Path/App%20Service.md)

**Официально:**
- Enable diagnostics logging: https://learn.microsoft.com/en-us/azure/app-service/troubleshoot-diagnostic-logs
- Deployment slots: https://learn.microsoft.com/en-us/azure/app-service/deploy-staging-slots
- Autoscale overview: https://learn.microsoft.com/en-us/azure/azure-monitor/autoscale/autoscale-overview

**Практика:**
- Создать slot, задеплоить туда, сделать swap (можно на минимальном примере).

**Самопроверка:**
- Квиз (App Service) в [quiz-app/](./quiz-app/).

### День 6 — Azure Functions: базовые понятия, триггеры
**Цель (что уметь):**
- Что такое Function App, host/runtime, consumption vs premium.
- Триггеры: HTTP, Timer, Storage/ServiceBus/Cosmos (как минимум на уровне “что где”).

**Репозиторий:**
- [Topics/Functions.md](./Topics/Functions.md)
- [Learning Path/Functions.md](./Learning%20Path/Functions.md)

**Официально:**
- Functions overview: https://learn.microsoft.com/en-us/azure/azure-functions/functions-overview
- Triggers and bindings concepts: https://learn.microsoft.com/en-us/azure/azure-functions/functions-triggers-bindings
- Hosting options: https://learn.microsoft.com/en-us/azure/azure-functions/functions-scale

**Практика (из Exercises):**
- [Exercises/Create an Azure Function by using Visual Studio Code/README.md](./Exercises/Create%20an%20Azure%20Function%20by%20using%20Visual%20Studio%20Code/README.md)

**Самопроверка:**
- [Knowledge Check/Functions.md](./Knowledge%20Check/Functions.md)
- 15–25 вопросов из [Questions/Functions.md](./Questions/Functions.md).

### День 7 — Azure Functions: bindings + “как это сдаётся на экзамене”
**Цель (что уметь):**
- Input/output bindings: как объявляются, что такое binding data.
- Понимать типичные сценарии: HTTP → Queue/ServiceBus/Blob; Timer → cleanup.

**Репозиторий:**
- [Topics/Functions.md](./Topics/Functions.md)
- [Learning Path/Functions.md](./Learning%20Path/Functions.md)

**Официально:**
- Binding expressions and patterns: https://learn.microsoft.com/en-us/azure/azure-functions/functions-bindings-expressions-patterns
- HTTP trigger: https://learn.microsoft.com/en-us/azure/azure-functions/functions-bindings-http-webhook

**Практика:**
- Сделать 1 маленькую функцию: HTTP trigger + output binding (например, в Queue).

**Самопроверка:**
- Пройти “compute week recap” (квиз + вопросы):
  - [Knowledge Check/Containers.md](./Knowledge%20Check/Containers.md)
  - [Knowledge Check/Functions.md](./Knowledge%20Check/Functions.md)
  - [Knowledge Check/App Service.md](./Knowledge%20Check/App%20Service.md)

---

## Неделя 2 — Storage (Blob + Cosmos) + закрепление Compute

### День 8 — Blob Storage: архитектура, структуры, доступ
**Цель (что уметь):**
- Storage account, контейнеры, blob types (block/append/page).
- Уровни доступа (hot/cool/archive) и что это значит.
- Metadata vs properties, когда что использовать.

**Репозиторий:**
- [Topics/Blob Storage.md](./Topics/Blob%20Storage.md)
- [Learning Path/Blob Storage.md](./Learning%20Path/Blob%20Storage.md)

**Официально:**
- Blob Storage overview: https://learn.microsoft.com/en-us/azure/storage/blobs/storage-blobs-overview
- Access tiers: https://learn.microsoft.com/en-us/azure/storage/blobs/access-tiers-overview

**Практика (из Exercises):**
- [Exercises/Create Blob storage resources by using the .NET client library/README.md](./Exercises/Create%20Blob%20storage%20resources%20by%20using%20the%20.NET%20client%20library/README.md)

**Самопроверка:**
- [Knowledge Check/Blob Storage.md](./Knowledge%20Check/Blob%20Storage.md)
- 15–25 вопросов из [Questions/Blob Storage.md](./Questions/Blob%20Storage.md).

### День 9 — Blob Storage: SDK операции + lifecycle management
**Цель (что уметь):**
- Базовые операции SDK: upload/download/list, set metadata/properties.
- Lifecycle rules: переходы по tier, удаление по возрасту.

**Репозиторий:**
- [Topics/Blob Storage.md](./Topics/Blob%20Storage.md)
- [Learning Path/Blob Storage.md](./Learning%20Path/Blob%20Storage.md)

**Официально:**
- Lifecycle management overview: https://learn.microsoft.com/en-us/azure/storage/blobs/lifecycle-management-overview
- .NET quickstart: https://learn.microsoft.com/en-us/azure/storage/blobs/storage-quickstart-blobs-dotnet

**Практика:**
- Настроить одну lifecycle policy (например, через Portal) и объяснить, что она делает.

**Самопроверка:**
- Квиз Blob Storage (в [quiz-app/](./quiz-app/)).

### День 10 — Cosmos DB: основы, модели, partitioning
**Цель (что уметь):**
- Что такое RU/s, partition key, logical vs physical partitions.
- Выбор partition key (кардинальность/равномерность) — частый экзаменационный момент.

**Репозиторий:**
- [Topics/Cosmos DB.md](./Topics/Cosmos%20DB.md)
- [Learning Path/CosmoDB.md](./Learning%20Path/CosmoDB.md)

**Официально:**
- Cosmos DB overview: https://learn.microsoft.com/en-us/azure/cosmos-db/introduction
- Partitioning: https://learn.microsoft.com/en-us/azure/cosmos-db/partitioning-overview

**Практика (из Exercises):**
- [Exercises/Create Azure Cosmos DB resources by using the Azure portal/README.md](./Exercises/Create%20Azure%20Cosmos%20DB%20resources%20by%20using%20the%20Azure%20portal/README.md)

**Самопроверка:**
- 15–25 вопросов из [Questions/Cosmos DB.md](./Questions/Cosmos%20DB.md).

### День 11 — Cosmos DB: consistency + change feed
**Цель (что уметь):**
- 5 уровней consistency и компромиссы (latency/throughput/availability).
- Что такое change feed, когда использовать.

**Репозиторий:**
- [Topics/Cosmos DB.md](./Topics/Cosmos%20DB.md)
- [Learning Path/CosmoDB.md](./Learning%20Path/CosmoDB.md)

**Официально:**
- Consistency levels: https://learn.microsoft.com/en-us/azure/cosmos-db/consistency-levels
- Change feed (NoSQL): https://learn.microsoft.com/en-us/azure/cosmos-db/nosql/change-feed

**Практика:**
- Описать 2 сценария: 1) строгая согласованность; 2) eventual + change feed.

**Самопроверка:**
- Квиз Cosmos DB (в [quiz-app/](./quiz-app/)).

### День 12 — “SDK mindset”: когда использовать SDK vs CLI/Portal
**Цель (что уметь):**
- Понимать, как на экзамене спрашивают “через SDK”: клиенты, authentication, connection strings.
- Уметь распознать, где нужен managed identity вместо секретов.

**Репозиторий:**
- [Topics/Compute Solutions.md](./Topics/Compute%20Solutions.md) (обзор)
- [Topics/Blob Storage.md](./Topics/Blob%20Storage.md), [Topics/Cosmos DB.md](./Topics/Cosmos%20DB.md)
- [Learning Path/README.md](./Learning%20Path/README.md) (если хочешь добрать официальные модули по SDK)

**Официально:**
- Azure SDKs overview: https://learn.microsoft.com/en-us/azure/developer/intro/azure-developer-intro

**Практика (из Exercises):**
- [Exercises/Create resources by using the Microsoft .NET SDK v3/README.md](./Exercises/Create%20resources%20by%20using%20the%20Microsoft%20.NET%20SDK%20v3/README.md)

**Самопроверка:**
- 10–20 вопросов из [Questions/Compute Solutions.md](./Questions/Compute%20Solutions.md) + [Questions/Storage Security.md](./Questions/Storage%20Security.md).

### День 13 — Повторение Storage (Blob + Cosmos)
**Цель:** закрыть пробелы и сделать быстрый “dry run” по типовым вопросам.

**Что сделать:**
- Перечитать свои тезисы за дни 8–11.
- Пройти Knowledge Check: [Knowledge Check/Blob Storage.md](./Knowledge%20Check/Blob%20Storage.md).
- Пройти 30–50 вопросов из [Questions/Blob Storage.md](./Questions/Blob%20Storage.md) и [Questions/Cosmos DB.md](./Questions/Cosmos%20DB.md).

### День 14 — Буфер/догонялка + мини‑симуляция
**Цель:** догнать невыполненные упражнения + один “мини‑экзамен”.

**Мини‑экзамен (40–60 минут):**
- 20 вопросов по compute + 20 по storage (любые файлы из [Questions/](./Questions/)).

---

## Неделя 3 — Security + Monitor (и постоянно “практика на понимание”) 

### День 15 — Entra ID + Microsoft Identity platform (база)
**Цель (что уметь):**
- Разница authentication vs authorization.
- App registrations: client id, tenant id, redirect URIs.
- Что такое scopes/permissions (delegated vs application) на концептуальном уровне.

**Репозиторий:**
- [Topics/Entra ID.md](./Topics/Entra%20ID.md)
- [Learning Path/Entra ID.md](./Learning%20Path/Entra%20ID.md)

**Официально:**
- Microsoft Identity platform overview: https://learn.microsoft.com/en-us/entra/identity-platform/
- App registration (concept): https://learn.microsoft.com/en-us/entra/identity-platform/quickstart-register-app

**Самопроверка:**
- 15–25 вопросов из [Questions/Entra ID.md](./Questions/Entra%20ID.md).

### День 16 — MSAL: интерактивная аутентификация (как в упражнениях)
**Цель (что уметь):**
- Что такое MSAL, access token vs id token.
- Как выбирать flow (interactive vs confidential client) на уровне “что куда подходит”.

**Репозиторий:**
- [Topics/Entra ID.md](./Topics/Entra%20ID.md) + [Topics/Graph.md](./Topics/Graph.md)
- [Learning Path/Entra ID.md](./Learning%20Path/Entra%20ID.md)

**Официально:**
- MSAL overview: https://learn.microsoft.com/en-us/entra/identity-platform/msal-overview

**Практика (из Exercises):**
- [Exercises/Implement interactive authentication by using MSAL.NET/README.md](./Exercises/Implement%20interactive%20authentication%20by%20using%20MSAL.NET/README.md)

**Самопроверка:**
- Квиз по Security (в [quiz-app/](./quiz-app/)).

### День 17 — Managed Identities (ключевой “экзаменационный” паттерн)
**Цель (что уметь):**
- System-assigned vs user-assigned.
- Как MI заменяет секреты/connection strings.
- Где назначаются права: RBAC, scopes.

**Репозиторий:**
- [Topics/Managed Identities.md](./Topics/Managed%20Identities.md)
- [Learning Path/Managed Identities.md](./Learning%20Path/Managed%20Identities.md)

**Официально:**
- Managed identities overview: https://learn.microsoft.com/en-us/entra/identity/managed-identities-azure-resources/overview

**Практика:**
- В Portal создать managed identity для сервиса (или хотя бы пройти шаги “как делается”).

**Самопроверка:**
- 15–25 вопросов из [Questions/Managed Identities.md](./Questions/Managed%20Identities.md).

### День 18 — Key Vault: secrets/keys/certs + доступ
**Цель (что уметь):**
- Разница secrets vs keys vs certificates.
- Access policies vs RBAC (на уровне “что где настраивается”).
- Soft delete/purge protection — когда обязательно.

**Репозиторий:**
- [Topics/Key Vault.md](./Topics/Key%20Vault.md)
- [Learning Path/Key Vault.md](./Learning%20Path/Key%20Vault.md)

**Официально:**
- Key Vault overview: https://learn.microsoft.com/en-us/azure/key-vault/general/overview
- Secrets in Key Vault: https://learn.microsoft.com/en-us/azure/key-vault/secrets/about-secrets

**Практика (из Exercises):**
- [Exercises/Set and retrieve a secret from Azure Key Vault by using Azure CLI/README.md](./Exercises/Set%20and%20retrieve%20a%20secret%20from%20Azure%20Key%20Vault%20by%20using%20Azure%20CLI/README.md)

**Самопроверка:**
- 15–25 вопросов из [Questions/Key Vault.md](./Questions/Key%20Vault.md).

### День 19 — App Configuration: фичефлаги/конфиги + интеграция
**Цель (что уметь):**
- Чем App Configuration отличается от Key Vault.
- Как хранить настройки безопасно: конфиги отдельно, секреты отдельно.

**Репозиторий:**
- [Topics/App Configuration.md](./Topics/App%20Configuration.md)
- [Learning Path/App Configuration.md](./Learning%20Path/App%20Configuration.md)

**Официально:**
- App Configuration overview: https://learn.microsoft.com/en-us/azure/azure-app-configuration/overview
- Feature management overview: https://learn.microsoft.com/en-us/azure/azure-app-configuration/overview-feature-management

**Самопроверка:**
- 10–20 вопросов из [Questions/App Configuration.md](./Questions/App%20Configuration.md).

### День 20 — SAS: подписи доступа к Storage (часто ловушки)
**Цель (что уметь):**
- Account SAS vs Service SAS vs User delegation SAS (на уровне отличий).
- Что входит в SAS: permissions + expiry + resource.

**Репозиторий:**
- [Topics/Shared Access Signatures.md](./Topics/Shared%20Access%20Signatures.md)
- [Learning Path/Shared Access Signatures.md](./Learning%20Path/Shared%20Access%20Signatures.md)

**Официально:**
- SAS overview: https://learn.microsoft.com/en-us/azure/storage/common/storage-sas-overview

**Практика:**
- Сгенерировать SAS (через Portal) и объяснить: какие права и на сколько.

**Самопроверка:**
- 15–25 вопросов из [Questions/Shared Access Signatures.md](./Questions/Shared%20Access%20Signatures.md).

### День 21 — Microsoft Graph: что это и как спрашивают на экзамене
**Цель (что уметь):**
- Что такое Microsoft Graph и какие данные он предоставляет.
- Как обычно выглядит вызов: permissions → token → запрос.

**Репозиторий:**
- [Topics/Graph.md](./Topics/Graph.md)
- [Learning Path/Graph.md](./Learning%20Path/Graph.md)

**Официально:**
- Graph overview: https://learn.microsoft.com/en-us/graph/overview
- Auth for Graph: https://learn.microsoft.com/en-us/graph/auth/

**Самопроверка:**
- 15–25 вопросов из [Questions/Graph.md](./Questions/Graph.md).

---

## Неделя 4 — Monitor + Integration/Messaging (вторая “дорогая” зона)

### День 22 — Azure Monitor + Application Insights: основы
**Цель (что уметь):**
- Разница logs vs metrics vs traces.
- Что такое instrumentation (в коде) и что такое “настройки мониторинга” (снаружи).

**Репозиторий:**
- [Topics/Application Insights.md](./Topics/Application%20Insights.md)
- [Learning Path/Application Insights.md](./Learning%20Path/Application%20Insights.md)

**Официально:**
- Azure Monitor overview: https://learn.microsoft.com/en-us/azure/azure-monitor/overview
- Application Insights overview: https://learn.microsoft.com/en-us/azure/azure-monitor/app/app-insights-overview

**Самопроверка:**
- 10–20 вопросов из [Questions/Application Insights.md](./Questions/Application%20Insights.md).

### День 23 — Application Insights: alerts + availability tests
**Цель (что уметь):**
- Настроить alert rule по метрике/логу.
- Availability tests: что проверяют и чем полезны.

**Официально:**
- Alerts overview: https://learn.microsoft.com/en-us/azure/azure-monitor/alerts/alerts-overview
- Availability tests overview: https://learn.microsoft.com/en-us/azure/azure-monitor/app/availability-overview

**Практика:**
- Создать 1 availability test + 1 alert (можно на тестовом web app).

**Самопроверка:**
- Квиз Monitoring (в [quiz-app/](./quiz-app/)).

### День 24 — API Management (APIM): instance, APIs, policies
**Цель (что уметь):**
- Что такое APIM: gateway + publisher portal + developer portal.
- Как ограничивать доступ: subscriptions/keys, OAuth2/JWT validate.
- Базовые policies: rate-limit, rewrite-uri, validate-jwt, caching.

**Репозиторий:**
- [Topics/API Management.md](./Topics/API%20Management.md)
- [Learning Path/API Management.md](./Learning%20Path/API%20Management.md)

**Официально:**
- APIM key concepts: https://learn.microsoft.com/en-us/azure/api-management/api-management-key-concepts
- Policies overview: https://learn.microsoft.com/en-us/azure/api-management/api-management-policies
- Policy reference: https://learn.microsoft.com/en-us/azure/api-management/api-management-policies-reference

**Самопроверка:**
- 15–25 вопросов из [Questions/API Management.md](./Questions/API%20Management.md).

### День 25 — Event Grid: event-driven интеграции
**Цель (что уметь):**
- Что такое event subscription, handlers (webhook, functions, etc.).
- Разница Event Grid vs Event Hubs (события vs поток).

**Репозиторий:**
- [Topics/Event Grid.md](./Topics/Event%20Grid.md) + [Topics/Events.md](./Topics/Events.md)
- [Learning Path/Event Grid.md](./Learning%20Path/Event%20Grid.md)

**Официально:**
- Event Grid overview: https://learn.microsoft.com/en-us/azure/event-grid/overview
- Event handlers: https://learn.microsoft.com/en-us/azure/event-grid/event-handlers

**Практика (из Exercises):**
- [Exercises/Route custom events to web endpoint by using Azure CLI/README.md](./Exercises/Route%20custom%20events%20to%20web%20endpoint%20by%20using%20Azure%20CLI/README.md)

**Самопроверка:**
- 15–25 вопросов из [Questions/Event Grid.md](./Questions/Event%20Grid.md).

### День 26 — Event Hubs: ingestion/streaming
**Цель (что уметь):**
- Consumer groups, partitions (на уровне концептов).
- Когда выбрать Event Hubs (телеметрия/стрим) вместо Event Grid.

**Репозиторий:**
- [Topics/Event Hub.md](./Topics/Event%20Hub.md) + [Topics/Events.md](./Topics/Events.md)
- [Learning Path/Event Hub.md](./Learning%20Path/Event%20Hub.md)

**Официально:**
- Event Hubs overview: https://learn.microsoft.com/en-us/azure/event-hubs/event-hubs-about

**Самопроверка:**
- 15–25 вопросов из [Questions/Event Hubs.md](./Questions/Event%20Hubs.md).

### День 27 — Service Bus: queues/topics/subscriptions + SDK
**Цель (что уметь):**
- Очередь vs topic/subscription.
- Dead-letter queue, sessions (на уровне “когда применимо”).
- Basic send/receive через SDK.

**Репозиторий:**
- [Topics/Service Bus.md](./Topics/Service%20Bus.md) + [Topics/Message Queues.md](./Topics/Message%20Queues.md)
- [Learning Path/Service Bus.md](./Learning%20Path/Service%20Bus.md)
- [Learning Path/Message Queues.md](./Learning%20Path/Message%20Queues.md)

**Официально:**
- Service Bus overview: https://learn.microsoft.com/en-us/azure/service-bus-messaging/service-bus-messaging-overview
- Queues, topics, subscriptions: https://learn.microsoft.com/en-us/azure/service-bus-messaging/service-bus-queues-topics-subscriptions

**Практика (из Exercises):**
- [Exercises/Send and receive message from a Service Bus queue by using .NET/README.md](./Exercises/Send%20and%20receive%20message%20from%20a%20Service%20Bus%20queue%20by%20using%20.NET/README.md)

**Самопроверка:**
- 15–25 вопросов из [Questions/Service Bus.md](./Questions/Service%20Bus.md).

### День 28 — Queue Storage: когда проще, чем Service Bus
**Цель (что уметь):**
- Queue Storage vs Service Bus (фичи, цена, гарантии).
- Базовые операции: enqueue/dequeue/visibility timeout.

**Репозиторий:**
- [Topics/Queue Storage.md](./Topics/Queue%20Storage.md) + [Topics/Message Queues.md](./Topics/Message%20Queues.md)
- [Learning Path/Queue Storage.md](./Learning%20Path/Queue%20Storage.md)

**Официально:**
- Queue Storage overview: https://learn.microsoft.com/en-us/azure/storage/queues/storage-queues-introduction

**Самопроверка:**
- 15–25 вопросов из [Questions/Queue Storage.md](./Questions/Queue%20Storage.md).

---

## Финальные 2 дня — Итоговая сборка и симуляция

### День 29 — Полный обзор слабых мест (таргетированный повтор)
**Цель:** закрыть пробелы, а не читать всё заново.

**Как делать:**
1) Открой список ошибок/сомнений из своих заметок.
2) По каждой теме открой 1–2 официальные страницы и добей терминологию.
3) Пройди квизы по темам, где <70% правильных.

**Репозиторий (на выбор по слабым местам):**
- [Topics/](./Topics/) + соответствующие файлы из [Questions/](./Questions/)

**Официально (быстрые “прощупывания”):**
- Exam demo: https://aka.ms/examdemo
- Practice assessment: https://learn.microsoft.com/en-us/certifications/exams/az-204/practice/assessment?assessment-type=practice&assessmentId=35

### День 30 — Симуляция экзамена + разбор
**Цель:** научиться “сдавать” (темп, внимание к условиям), а не просто знать теорию.

**Симуляция (60–120 минут):**
- 60–80 вопросов из [Questions/](./Questions/) (разные темы) без подсказок.

**Разбор (30–60 минут):**
- В каждом неправильном ответе выпиши: “какой сигнал в вопросе я пропустил?”
- Составь список “триггерных” слов: cost, latency, simplest, secure, minimal changes, must use SDK, must use managed identity и т.д.

---

## Ссылки (точки входа, если нужно быстро открыть официальные разделы)
- AZ-204 Study guide: https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/az-204
- Exam page (details + scheduling): https://learn.microsoft.com/en-us/credentials/certifications/exams/az-204/
- Exam Readiness Zone (5 видео по доменам):
  - Compute: https://learn.microsoft.com/en-us/shows/exam-readiness-zone/preparing-for-az-204-develop-azure-compute-solutions-1-of-5
  - Storage: https://learn.microsoft.com/en-us/shows/exam-readiness-zone/preparing-for-az-204-develop-for-azure-storage-segment-2-of-5
  - Security: https://learn.microsoft.com/en-us/shows/exam-readiness-zone/preparing-for-az-204-implement-azure-security-segment-3-of-5
  - Monitor: https://learn.microsoft.com/en-us/shows/exam-readiness-zone/preparing-for-az-204-monitor-troubleshoot-and-optimize-azure-solutions-segment-4-of-5
  - Integration: https://learn.microsoft.com/en-us/shows/exam-readiness-zone/preparing-for-az-204-connect-to-and-consume-azure-services-and-third-party-services-segment-5-of-5
