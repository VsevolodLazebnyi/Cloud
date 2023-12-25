<a name="Вернуться в начало"></a>

<div align="center">

  <h3>Лабораторные работы команды "На тоненьком"</h3>
  <h4>по дисциплине: "Облачные технологии и услуги"</h4>

```
    Состав команды:
    Боровский Максим (@unf1x)
    Лазебный Всеволод (@vllazebnyi)
```

</div>


<details>
  <summary> Навигация </summary>
  <ol>
    <li>
      <a href="#Аналитические ЛАБЫ">Аналитические ЛАБЫ</a>
      <ul>
        <li><a href="#Лабораторная AWS">Лабораторная AWS</a></li>
      <ul>
        <li><a href="#Заполнение">Заполнение</a></li>
      </ul>
    </li>
  </ol>
</details>


<a name="Аналитические ЛАБЫ"></a>
# Аналитические ЛАБЫ

<a name="Лабораторная AWS"></a>
## Лабораторная Azure

*Цель работы:* узнать о назначении различных облачных сервисов, проанализировать фичи, то, за что проходит оплата каждого из них, понять, к какому уровню абстракции относится каждый, исходя из этих знаний найти аналоги среди российских сервисов.

---
**Дано:**
Документ таблица:

|IT Tower|Service Family|Service Type|Service Sub Type|Service Usage Type|Meter Category      |Meter Sub-Category |Meter Name                   |Consumed Service                 |FIELD10|FIELD11|
|--------|--------------|------------|----------------|------------------|--------------------|-------------------|-----------------------------|---------------------------------|-------|-------|
|        |              |            |                |                  |Container Instances |Container Instances|Core Duration                |Microsoft.ContainerInstance      |       |       |
|        |              |            |                |                  |Container Instances |Container Instances|Duration                     |Microsoft.ContainerInstance      |       |       |
|        |              |            |                |                  |Container Instances |Container Instances|Executions                   |Microsoft.ContainerInstance      |       |       |
|        |              |            |                |                  |Container Instances |                   |Memory Duration              |Microsoft.ContainerInstance      |       |       |
|        |              |            |                |                  |Container Instances |                   |vCPU Duration                |Microsoft.ContainerInstance      |       |       |
|        |              |            |                |                  |Container Registry  |Small              |Registry Unit                |Microsoft.ContainerRegistry      |       |       |
|        |              |            |                |                  |Container Registry  |Basic              |Registry Unit                |Microsoft.ContainerRegistry      |       |       |
|        |              |            |                |                  |Container Registry  |Standard           |Registry Unit                |Microsoft.ContainerRegistry      |       |       |
|        |              |            |                |                  |Container Registry  |Premium            |Registry Unit                |Microsoft.ContainerRegistry      |       |       |
|        |              |            |                |                  |Container Registry  |                   |%Duration                    |Microsoft.ContainerRegistry      |       |       |
|        |              |            |                |                  |Container Registry  |                   |Small Registry Unit          |Microsoft.ContainerRegistry      |       |       |
|        |              |            |                |                  |Container Registry  |                   |Basic Registry Unit          |Microsoft.ContainerRegistry      |       |       |
|        |              |            |                |                  |Container Registry  |                   |Standard Registry Unit       |Microsoft.ContainerRegistry      |       |       |
|        |              |            |                |                  |Container Registry  |                   |Premium Registry Unit        |Microsoft.ContainerRegistry      |       |       |
|        |              |            |                |                  |Cortana Intelligence|Customer Insights  |Basic (Daily Unit)           |Microsoft.CustomerInsights       |       |       |
|        |              |            |                |                  |Data Box            |                   |                             |Microsoft.DataBox                |       |       |
|        |              |            |                |                  |Data Lake Analytics |                   |Pay-as-you-go Analytics Units|Microsoft.DataLakeAnalytics      |       |       |
|        |              |            |                |                  |Data Lake Store     |                   |Pay-as-you-go Data at Rest   |Microsoft.DataLakeStore          |       |       |
|        |              |            |                |                  |Data Lake Store     |                   |%Transactions%               |Microsoft.DataLakeStore          |       |       |
|        |              |            |                |                  |Data Management     |                   |Geo-Replicated Data Transfer%|                                 |       |       |
|        |              |            |                |                  |Data Management     |Geo Redundant      |                             |                                 |       |       |
|        |              |            |                |                  |Data Management     |                   |                             |                                 |       |       |
|        |              |            |                |                  |Data Services       |                   |                             |                                 |       |       |
|        |              |            |                |                  |SQL Data Warehouse  |Compute Optimized% |100 DWUs                     |Microsoft.Sql                    |       |       |
|        |              |            |                |                  |Bandwidth           |                   |%Data Transfer%              |Microsoft.MachineLearningServices|       |       |
|        |              |            |                |                  |Bandwidth           |                   |%Data Transfer%              |Microsoft.Search                 |       |       |
|        |              |            |                |                  |Network Watcher     |Network Watcher    |Diagnostic Tool API          |Microsoft.Network                |       |       |
|        |              |            |                |                  |Network Watcher     |                   |%                            |microsoft.operationalinsights    |       |       |
|        |              |            |                |                  |Network Watcher     |                   |%                            |Microsoft.Network                |       |       |
|        |              |            |                |                  |Application Gateway |Standard v2        |Fixed Cost                   |Microsoft.Network                |       |       |
|        |              |            |                |                  |Application Gateway |Standard v2        |Capacity Units               |Microsoft.Network                |       |       |
|        |              |            |                |                  |Application Gateway |Basic              |%Data%                       |Microsoft.Network                |       |       |
|        |              |            |                |                  |Application Gateway |Basic              |%Gateway%                    |Microsoft.Network                |       |       |
|        |              |            |                |                  |Application Gateway |WAF                |%Gateway%                    |Microsoft.Network                |       |       |
|        |              |            |                |                  |Application Gateway |WAF v2             |                             |Microsoft.Network                |       |       |



---
**Ход работы:**

<a name="Заполнение AWS"></a>
## Заполнение


Список данных был просмотрен на сайте windows azure - [https://azure.microsoft.com/ru-ru/products].
Обобщенное описание многих сервисов - [https://ecm-journal.ru/material/Azure-Service-Platform] и [https://satyenkumar.medium.com/demystifying-the-cloud-computing-an-overview-of-the-microsoft-azure-6a5c1fb1799d].

в соответствии с фильтрами, подобран самый вероятный ответ в ячейку таблицы.с 
(проведен анализ списков сервисов и был подобран отечественный вариант Yandex, Vk, Else)

![azur1](https://github.com/VsevolodLazebnyi/cloud-ict-2023/blob/main/add/azur1.png?raw=true)
![azur2](https://github.com/VsevolodLazebnyi/cloud-ict-2023/blob/main/add/azur2.png?raw=true)

|IT Tower     |Service Family   |Service Type           |Service Sub Type          |Service Usage Type         |Meter Category     |Meter Sub-Category          |Meter Name|Consumed Service                 |YandexCloud Service           |YandexCloud Service        |Else         |
|-------------|-----------------|-----------------------|--------------------------|---------------------------|-------------------|----------------------------|----------|---------------------------------|------------------------------|---------------------------|-------------|
|Compute      |Containers       |Azure Container Instanses|Container group           |Compute Hours              |Container Instances|Container Instances         |Core Duration|Microsoft.ContainerInstance      | Yandex Serverless Containers |Cloud Containers           |SberCloud    |
|Compute      |Containers       |Azure Container Instanses|Container group           |Compute Hours              |Container Instances|Container Instances         |Duration  |Microsoft.ContainerInstance      | Yandex Serverless Containers |Cloud Containers           |SberCloud    |
|Compute      |Containers       |Azure Container Instanses|Container group           |Number of Executions       |Container Instances|Container Instances         |Executions|Microsoft.ContainerInstance      | Yandex Serverless Containers |Cloud Containers           |SberCloud    |
|Compute      |Containers       |Azure Container Instanses|Container group           |Compute Hours              |Container Instances|                            |Memory Duration|Microsoft.ContainerInstance      | Yandex Serverless Containers |Cloud Containers           |SberCloud    |
|Compute      |Containers       |Azure Container Instanses|Container group           |Compute Hours              |Container Instances|                            |vCPU Duration|Microsoft.ContainerInstance      | Yandex Serverless Containers |Cloud Containers           |SberCloud    |
|Infrastructure|Containers       |Azure Container Registry|Small Registry            |Storage Capacity           |Container Registry |Small                       |Registry Unit|Microsoft.ContainerRegistry      |Yandex Container Registry     |                           |             |
|Infrastructure|Containers       |Azure Container Registry|Registry                  |Storage Capacity           |Container Registry |Basic                       |Registry Unit|Microsoft.ContainerRegistry      |Yandex Container Registry     |                           |             |
|Infrastructure|Containers       |Azure Container Registry|Standard Registry         |Storage Capacity           |Container Registry |Standard                    |Registry Unit|Microsoft.ContainerRegistry      |Yandex Container Registry     |                           |             |
|Infrastructure|Containers       |Azure Container Registry|Premium Registry          |Storage Capacity           |Container Registry |Premium                     |Registry Unit|Microsoft.ContainerRegistry      |Yandex Container Registry     |                           |             |
|Infrastructure|Containers       |Azure Container Registry|Additional Storage        |Compute Hours              |Container Registry |                            |%Duration |Microsoft.ContainerRegistry      |Yandex Container Registry     |                           |             |
|Infrastructure|Containers       |Azure Container Registry|Small Registry            |Additional storage Capacity|Container Registry |                            |Small Registry Unit|Microsoft.ContainerRegistry      |Yandex Container Registry     |                           |             |
|Infrastructure|Containers       |Azure Container Registry|Basic Registry            |Additional storage Capacity|Container Registry |                            |Basic Registry Unit|Microsoft.ContainerRegistry      |Yandex Container Registry     |                           |             |
|Infrastructure|Containers       |Azure Container Registry|Standard Registry         |Additional storage Capacity|Container Registry |                            |Standard Registry Unit|Microsoft.ContainerRegistry      |Yandex Container Registry     |                           |             |
|Infrastructure|Containers       |Azure Container Registry|Premium Registry          |Additional storage Capacity|Container Registry |                            |Premium Registry Unit|Microsoft.ContainerRegistry      |Yandex Container Registry     |                           |             |
|Application  |AI               |Azure Cortana Intelligence Suite|Customer Insights         |Consumption Time           |Cortana Intelligence|Customer Insights           |Basic (Daily Unit)|Microsoft.CustomerInsights       |SpeechKit + DataSphere        |Cloud ML Platform          |             |
|Infrastructure|Storage          |Azure Data Box         |Data Box                  |Service Fee per Unit       |Data Box           |                            |          |Microsoft.DataBox                |Yandex Data Transfer          |Cloud Storage              |             |
|Data         |Analitycs        |Azure Data Lake Analytics|Analytics Unit            |Unit usage per Hour        |Data Lake Analytics|                            |Pay-as-you-go Analytics Units|Microsoft.DataLakeAnalytics      |Yandex DataProc               |Cloud Big Data             |             |
|Data         |Data Storage     |Azure Data Lake Storage|Data Storage Gen1         |Capacity in TB             |Data Lake Store    |                            |Pay-as-you-go Data at Rest|Microsoft.DataLakeStore          |Object Storage                |VK Cloud Storage           |SberCloud    |
|Data         |Data Storage     |Azure Data Lake Storage|Data Storage Gen2         |Transactions Amount        |Data Lake Store    |                            |%Transactions%|Microsoft.DataLakeStore          |Object Storage                |VK Cloud Storage           |SberCloud    |
|Data         |Data Storage     |Azure Blob Storage     |Data Storage Gen3         |Operations and Data Transfer|Data Management    |                            |Geo-Replicated Data Transfer%|                                 |Object Storage                |VK Cloud Storage           |SberCloud    |
|Data         |Data Storage     |Azure Blob Storage     |Data Storage              |Storage Capacity           |Data Management    |Geo Redundant               |Geo-Replicated Data Transfer%|Microsoft.DataLakeAnalytics      |Object Storage                |VK Cloud Storage           |SberCloud    |
|Data         |Data Storage     |Azure Blob Storage     |Data Storage              |SSH File Transfer Protocol |Data Management    |                            |Geo-Replicated Data Transfer%|Microsoft.DataLakeAnalytics      |Object Storage                |VK Cloud Storage           |SberCloud    |
|Data         |Data Storage     |Microsoft Purview      |Data Storage              |Duration of Scans          |Data Services      |                            |Geo-Replicated Data Transfer%|Microsoft.DataLakeAnalytics      |                              |                           |SberCloud    |
|Data         |Data Analysis    |Azure Synapse Analytics|Data Warehousing          |Dedicated Consumption model|SQL Data Warehouse |Compute Optimized%          |100 DWUs  |Microsoft.Sql                    |Yandex Managed Service for YDB|Arenadata DB               |             |
|Application  |AI               |Azure Machine Learning |ML Endpoints              |Bandwith                   |Bandwidth          |                            |%Data Transfer%|Microsoft.MachineLearningServices|Yandex DataSphere             |VK Cloud ML Platform       |             |
|Cloud Service|Content Delivery |Azure CDN              |Acceleration Data Transfers|Bandwith                   |Bandwidth          |                            |%Data Transfer%|Microsoft.Search                 |Yandex Cloud CDN              |VK Content Delivery Network|             |
|Network      |Network Diagnostics|Azure Network Watcher  |Network Diagnostic Tool   |Amount of Checks           |Network Watcher    |Network Watcher             |Diagnostic Tool API|Microsoft.Network                |Yandex Monitoring             |VK Cloud Logging           |Cloud Logging|
|Network      |Network Monitoring|Azure Monitor          |Ingestion                 |Analytics Logs             |Network Watcher    |                            |%         |microsoft.operationalinsights    |Yandex Monitoring             |VK Cloud Logging           |Cloud Logging|
|Network      |Network Diagnostics|Azure Network Watcher  |Network Performance       |Units per Connections      |Network Watcher    |                            |%         |Microsoft.Network                |Yandex Monitoring             |VK Cloud Logging           |Cloud Logging|
|Network      |Appplication Gateway|Azure Application Gateway|Standard Application Getaway|Getaway-Hours              |Application Gateway|Standard v2                 |Fixed Cost|Microsoft.Network                |Yandex API Gateway            |Load Balancer Vk Cloud     |             |
|Network      |Appplication Gateway|Azure Application Gateway|Standard Application Getaway|Capacity Unit-Hours        |Application Gateway|Standard v2                 |Capacity Units|Microsoft.Network                |Yandex API Gateway            |Load Balancer Vk Cloud     |             |
|Network      |Appplication Gateway|Azure Application Gateway|Data Transfer             |Data going into data centres|Application Gateway|Basic                       |%Data%    |Microsoft.Network                |Yandex API Gateway            |Load Balancer Vk Cloud     |             |
|Network      |Appplication Gateway|Azure Application Gateway|Data Transfer             |Amount of Data Processed   |Application Gateway|Basic                       |%Gateway% |Microsoft.Network                |Yandex API Gateway            |Load Balancer Vk Cloud     |             |
|Network      |Appplication Gateway|Azure Application Gateway|Web Application Firewall Application Gateway V1|Gateway-Hour               |Application Gateway|WAF                         |%Gateway% |Microsoft.Network                |Yandex API Gateway            |Load Balancer Vk Cloud     |             |
|Network      |Appplication Gateway|Azure Application Gateway|Web Application Firewall Application Gateway V2|Capacity Unit-Hours        |Application Gateway|WAF v2                      |%Gateway% |Microsoft.Network                |Yandex API Gateway            |Load Balancer Vk Cloud     |             |


![azureanlab](https://github.com/VsevolodLazebnyi/cloud-ict-2023/blob/main/add/azureanlab.png?raw=true)

---

## ***Описание сервисов Azure*** ## 

__Azure Container Instances__ Это сервис для запуска контейнеров (Linux и Windows) в облаке без необходимости виртуальных машин или инструментов для оркестрации. Поддерживает управление через командную строку, хранение данных и настройки для доступа к виртуальным сетям.

__Azure Container Registry__ Служба хранения и управления образами контейнеров без пользовательского интерфейса, доступная только через командную строку.

__Azure Cortana Intelligence Suite__ Предоставляет возможности для анализа данных и искусственного интеллекта, включая Power BI, HDInsight Spark, инструменты для машинного обучения и интеграцию с Cortana, а также поддержку ботов и инструменты для обработки естественного языка.

__Azure Data Box__ Сервис для безопасной транспортировки больших объемов данных в облако без интернета, используя протоколы NAS.

__Azure Data Lake Analytics__ Сервис для анализа больших данных с масштабируемыми вычислительными возможностями, позволяющий выполнение аналитики с использованием U-SQL.

__Azure Data Lake Store__ Масштабируемое хранилище данных, оптимизированное для анализа больших объемов данных и совместимое с Apache Hadoop.

__Arenadata DB__ Аналитическая база данных для хранения и обработки больших данных в облаке, интегрирующаяся с сервисами анализа данных.

__Microsoft Purview__ Централизованный сервис управления данными в облаке и локальных средах с аналитикой, схемами данных и автоматизированным получением метаданных.

__Azure Machine Learning__ Сервис для автоматизации выбора моделей машинного обучения с поддержкой различных языков и библиотек, обеспечивающий высокую защиту данных.

__Azure CDN__ Инфраструктура для быстрой доставки контента по всему миру с масштабированием и поддержкой HTTPS и защитой от DDoS.

__Azure Network Watcher__ Инструмент для мониторинга и управления сетевыми элементами в Azure, включая анализ состояния сети и трафика.

__Azure Application Gateway__ Управляет трафиком к веб-приложениям с функциями защиты, маршрутизации на уровне приложения, SSL завершением и управлением сессиями.


----
## ***отечественные аналоги *** ##

__Yandex Serverless Containers__ Сервис для запуска контейнеров без управления серверами, с автоматическим масштабированием и оплатой по факту использования ресурсов.

__Cloud Containers (VK)__ Аналогичен Yandex Serverless Containers, но ориентирован только на Kubernetes. Предоставляет богатые метрики и инструменты мониторинга.

__Yandex Container Registry__ Хранилище Docker-образов с поддержкой развёртывания и управления контейнерами, предоставляющее различные инструменты управления и взаимодействия с образами.

__VK Cloud__ Нет узкоспециализированных сервисов, только общий сервис для облачного оркестратора.

__Cloud Voice__ Подходит для автораспознавания и синтеза речи, работает стабильно, поддерживает потоковое аудио и звуковые файлы.

__Yandex Data Transfer__ Платформа для миграции данных, позволяющая переносить большие объемы данных с минимальным временем простоя.

__Cloud Storage__ Хранилище данных для VK Cloud, предоставляющее место для хранения данных различных типов.

__Yandex DataProc__ Сервис обработки больших объемов данных, взаимодействующий с Hadoop, Spark и другими системами для ETL и других видов обработки данных.

__Cloud Big Data__ Решение для анализа больших объемов данных, включающее Apache Hadoop и поддерживающее работу с озёрами данных.

__Yandex Object Storage__ Хранилище для больших объемов данных с высокой доступностью и автоматическим масштабированием, с поддержкой Apache Airflow из коробки.

__VK Cloud Storage__ Широкопрофильное решение для хранения данных, включая большие данные и Data Lakes, с поддержкой различных инструментов для работы с хранилищем.

__Azure Synapse Analytics__ Платформа для обработки и анализа масштабных датасетов, объединяющая преимущества больших данных и аналитических возможностей.

__Yandex Managed Service for YDB__  Управляемая база данных с гибкими возможностями обработки данных с использованием SQL и NoSQL методов.

__Yandex DataSphere__ Платформа для разработки, анализа и внедрения данных и моделей машинного обучения в облаке.

__VK Cloud ML Platform__ Облачная среда для создания и внедрения моделей машинного обучения с инструментами для разработки и хранения в российских ЦОДах.

__Yandex Cloud CDN__ Уменьшает нагрузку на основной сервер через распределение и кэширование. Более 140 CDN-ов, предоставляет инструменты аналитики трафика.

__VK Content Delivery Network__ Разгружает основной сервер, принимая на себя весь трафик. Обещает среднюю задержку в 20 мс и более 400 ЦОДов на 5 континентах.

__Yandex Monitoring__ Позволяет отслеживать состояние и производительность ресурсов в реальном времени, анализировать логи. Cloud Logging специализируется на работе с логами.

__VK Cloud Logging__ Собирает, анализирует и хранит данные о событиях, обеспечивает быстрый поиск и визуализацию данных для мониторинга приложений и системы.

__Yandex API Gateway__  Аналог от Microsoft, но позволяет создавать API-шлюзы для связи внешних приложений с внутренними ресурсами компании.

__Load Balancer Vk Cloud__ Отказоустойчивый балансировщик веб-трафика с автомасштабированием. Предоставляет аналитику для решения проблем, использует продвинутые алгоритмы для выбора оптимального сервера для каждого запроса.

__SberCloud__ Провайдер услуг и сервисов по моделям IaaS и PaaS (IT-инфраструктура в аренду) для бизнеса и государственных организаций.

__Sber GigaChat__ нейросеть от Сбера, которая умеет отвечать на вопросы, писать код, рисовать изображения по запросу на русском языке.

----
## Вывод

В результате выполнения данной лабораторной работы была сформирована и заполнена таблица с данными из документации Amazon. Были проанализированы и описаны сервисы azure и их отечественные аналоги, а также получены данные о подтипах этих сервисов и других характеристиках.


Все готово!


