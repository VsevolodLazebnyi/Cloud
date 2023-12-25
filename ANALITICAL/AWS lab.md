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
## Лабораторная AWS

*Цель работы:* узнать о назначении различных облачных сервисов, проанализировать фичи, то, за что проходит оплата каждого из них, понять, к какому уровню абстракции относится каждый, исходя из этих знаний найти аналоги среди российских сервисов.

---
**Дано:**
Документ таблица:
![awsanlab](https://github.com/VsevolodLazebnyi/cloud-ict-2023/blob/main/add/awsanlab.png?raw=true)

|IT Tower     |Service Family   |Service Type           |Service Sub Type          |Service Usage Type         |Product Code       |Usage Type                  |[lineItem/Operation]|lineItem/LineItemDescription     |
|-------------|-----------------|-----------------------|--------------------------|---------------------------|-------------------|----------------------------|--------------------|---------------------------------|
|             |                 |                       |                          |                           |AmazonEC2          |%BoxUsage%                  |                    |                                 |
|             |                 |                       |                          |                           |AmazonEC2          |                            |                    |Tax%                             |
|             |                 |                       |                          |                           |ComputeSavingsPlans|ComputeSP%AllUpfront        |                    |                                 |
|             |                 |                       |                          |                           |ComputeSavingsPlans|ComputeSP%NoUpfront         |                    |                                 |
|             |                 |                       |                          |                           |AmazonEC2          |%DedicatedUsage%            |Surcharge           |                                 |
|             |                 |                       |                          |                           |AmazonEC2          |%DedicatedUsage%            |                    |                                 |
|             |                 |                       |                          |                           |AmazonEC2          |%HostUsage%                 |                    |                                 |
|             |                 |                       |                          |                           |AmazonEC2          |%EGpuUsage%                 |                    |                                 |
|             |                 |                       |                          |                           |AmazonEC2          |%SpotUsage%                 |                    |                                 |
|             |                 |                       |                          |                           |AmazonEC2          |%CPUCredits%                |                    |                                 |
|             |                 |                       |                          |                           |AmazonEC2          |%Purchase%                  |                    |Sign up charge for subscription:%|
|             |                 |                       |                          |                           |AmazonEC2          |%ExchangeUsage              |                    |                                 |
|             |                 |                       |                          |                           |AmazonEC2          |%HeavyUsage%                |                    |                                 |
|             |                 |                       |                          |                           |AmazonEC2RIResale2 |%RIResaleServiceFee         |                    |                                 |
|             |                 |                       |                          |                           |AmazonCloudFront   |                            |                    |Tax%                             |
|             |                 |                       |                          |                           |AmazonCloudFront   |%Requests-Tier1             |                    |                                 |
|             |                 |                       |                          |                           |AmazonCloudFront   |%Requests-Tier1             |                    |                                 |
|             |                 |                       |                          |                           |AmazonCloudFront   |%Requests-Tier2-HTTPS       |                    |                                 |
|             |                 |                       |                          |                           |AmazonCloudFront   |%Requests-HTTP%             |                    |                                 |
|             |                 |                       |                          |                           |AmazonCloudFront   |%Invalidations              |                    |                                 |
|             |                 |                       |                          |                           |AmazonCloudFront   |%FMS-Out-Bytes              |                    |                                 |
|             |                 |                       |                          |                           |AmazonCloudFront   |%DataTransfer%              |                    |                                 |
|             |                 |                       |                          |                           |AmazonCloudFront   |SSL-Cert-Custom             |                    |                                 |
|             |                 |                       |                          |                           |AmazonKendra       |%KendraEnterpriseEdition    |                    |                                 |
|             |                 |                       |                          |                           |AmazonKendra       |%DocumentsScanned           |                    |                                 |
|             |                 |                       |                          |                           |AmazonKendra       |%ConnectorSync              |                    |                                 |
|             |                 |                       |                          |                           |AmazonLex          |                            |                    |Tax%                             |
|             |                 |                       |                          |                           |AmazonLex          |%Req%                       |                    |                                 |
|             |                 |                       |                          |                           |AmazonRoute53      |                            |                    |Tax%                             |
|             |                 |                       |                          |                           |AmazonRoute53      |%Health-Check-Option-AWS    |                    |                                 |
|             |                 |                       |                          |                           |AmazonRoute53      |%Health-Check-AWS           |                    |                                 |
|             |                 |                       |                          |                           |AmazonRoute53      |%DNS-Queries                |                    |                                 |
|             |                 |                       |                          |                           |AmazonRoute53      |%LBR-Queries                |                    |                                 |
|             |                 |                       |                          |                           |AmazonRoute53      |%Intra-AWS-DNS-Queries      |                    |                                 |
|             |                 |                       |                          |                           |AmazonRoute53      |%HostedZone                 |                    |                                 |
|             |                 |                       |                          |                           |AmazonRoute53      |%Health-Check-Non-AWS       |                    |                                 |
|             |                 |                       |                          |                           |AmazonRoute53      |%Traffic-Flow-Policy-Records|                    |                                 |
|             |                 |                       |                          |                           |AmazonRoute53      |%Health-Check%              |%Latency%           |                                 |
|             |                 |                       |                          |                           |AmazonRoute53      |%Health-Check-Option-Non-AWS|                    |                                 |
|             |                 |                       |                          |                           |AmazonRoute53      |%Geo-Queries%               |                    |                                 |
|             |                 |                       |                          |                           |AmazonRoute53      |%ResolverNetworkInterface   |                    |                                 |



---
**Ход работы:**

<a name="Заполнение AWS"></a>
## Заполнение


Список данных был просмотрен на сайте AWS amazon - [https://docs.aws.amazon.com/].
в соответствии с фильтрами, подобран самый вероятный ответ в ячейку таблицы.с 
(проведен анализ списков сервисов и был подобран отечественный вариант Yandex, Vk, Else)

![awssite](https://github.com/VsevolodLazebnyi/cloud-ict-2023/blob/main/add/awssite.png?raw=true)

Все сервисы были расположены в порядке IT Tower от сетевого уровня к уровню приложений. 

|IT Tower     |Service Family   |Service Type           |Service Sub Type          |Service Usage Type         |Product Code       |Usage Type                  |[lineItem/Operation]|lineItem/LineItemDescription     |Yandex Cloud                       |VK Cloud                   |ELSE         |
|-------------|-----------------|-----------------------|--------------------------|---------------------------|-------------------|----------------------------|--------------------|---------------------------------|-----------------------------------|---------------------------|-------------|
|Compute      |Container Service|AWS Container Instanses|Compute Optimized         |On-Demand Instances        |AmazonEC2          |%BoxUsage%                  |                    |                                 |Yandex Compute Cloud               |Cloud Servers              |-            |
|Compute      |Container Service|AWS Container Instanses|General Purpose           |Virtual Machine            |AmazonEC2          |                            |                    |Tax%                             |Yandex Compute Cloud               |Cloud Servers              |-            |
|Compute      |Savings Plans    |AWS Savings Plans      |Saving Plans              |Saving Plans               |ComputeSavingsPlans|ComputeSP%AllUpfront        |                    |                                 |Reserved Consumption               |                           |-            |
|Compute      |Savings Plans    |AWS Savings Plans      |Saving Plans              |Saving Plans               |ComputeSavingsPlans|ComputeSP%NoUpfront         |                    |                                 |Reserved Consumption               |                           |-            |
|Compute      |Container Service|AWS Container Instanses|Compute Optimized         |Dedicated Instances        |AmazonEC2          |%DedicatedUsage%            |Surcharge           |                                 |Yandex Compute Cloud               |Cloud Servers              |SberCloud    |
|Compute      |Container Service|AWS Container Instanses|Compute Optimized         |Dedicated Instances        |AmazonEC2          |%DedicatedUsage%            |                    |                                 |Yandex Compute Cloud               |Cloud Servers              |SberCloud    |
|Compute      |Container Service|AWS Container Instanses|Physical Server           |Dedicated Host             |AmazonEC2          |%HostUsage%                 |                    |                                 |Yandex Compute Cloud               |Cloud Servers              |SberCloud    |
|Compute      |Container Service|AWS Container Instanses|Graphics Optimized GPU    |GPU Instances              |AmazonEC2          |%EGpuUsage%                 |                    |                                 |Yandex Compute Cloud               |Cloud Servers              |SberCloud    |
|Compute      |Container Service|AWS Container Instanses|Spot Instances            |Spot Instances             |AmazonEC2          |%SpotUsage%                 |                    |                                 |Yandex Compute Cloud               |Cloud Servers              |SberCloud    |
|Compute      |Container Service|AWS Container Instanses|CPU Credits               |T2/T3 CPU Credits          |AmazonEC2          |%CPUCredits%                |                    |                                 |Yandex Compute Cloud               |Cloud Servers              |SberCloud    |
|Compute      |Container Service|AWS Container Instanses|All Upfront               |Reserved Instance          |AmazonEC2          |%Purchase%                  |                    |Sign up charge for subscription:%|Yandex Compute Cloud               |Cloud Servers              |SberCloud    |
|Compute      |Container Service|AWS Container Instanses|Instances Modification    |Savings Plans Exchange     |AmazonEC2          |%ExchangeUsage              |                    |                                 |Yandex Compute Cloud               |Cloud Servers              |SberCloud    |
|Compute      |Container Service|AWS Container Instanses|Compute Optimized         |Heavy Utilization Instances|AmazonEC2          |%HeavyUsage%                |                    |                                 |Yandex Compute Cloud               |Cloud Servers              |SberCloud    |
|Compute      |Container Service|AWS Container Instanses|RI Resale                 |RI Resale Service Fee      |AmazonEC2RIResale2 |%RIResaleServiceFee         |                    |                                 |Yandex Cloud Marketplace           |VK Cloud Marketplace       |SberCloud    |
|Cloud Service|Data Storage     |AWS                    |RI Resale                 |RI Resale                  |AmazonCloudFront   |                            |                    |Tax%                             |Yandex Cloud CDN                   |VK Content Delivery Network|SberDisk CDN |
|Cloud Service|Data Storage     |AWS                    |Request Handling          |Tier 1 Requests            |AmazonCloudFront   |%Requests-Tier1             |                    |                                 |Yandex Cloud CDN                   |VK Content Delivery Network|SberDisk CDN |
|Cloud Service|Data Storage     |AWS                    |Request Handling          |Tier 1 Requests            |AmazonCloudFront   |%Requests-Tier1             |                    |                                 |Yandex Cloud CDN                   |VK Content Delivery Network|SberDisk CDN |
|Cloud Service|Data Storage     |AWS                    |Dynamic Content Delivery  |Tier 2 HTTP Requests       |AmazonCloudFront   |%Requests-Tier2-HTTPS       |                    |                                 |Yandex Cloud CDN                   |VK Content Delivery Network|SberDisk CDN |
|Cloud Service|Data Storage     |AWS                    |Static Content Delivery   |HTTP Requests              |AmazonCloudFront   |%Requests-HTTP%             |                    |                                 |Yandex Cloud CDN                   |VK Content Delivery Network|SberDisk CDN |
|Cloud Service|Data Storage     |AWS                    |Content Delivery          |Invalidation               |AmazonCloudFront   |%Invalidations              |                    |                                 |Yandex Cloud CDN                   |VK Content Delivery Network|SberDisk CDN |
|Cloud Service|Data Storage     |AWS                    |Media Streaming           |Data Transfer              |AmazonCloudFront   |%FMS-Out-Bytes              |                    |                                 |Yandex Cloud CDN                   |VK Content Delivery Network|SberDisk CDN |
|Cloud Service|Data Storage     |AWS                    |Inter-region Data Transfer|Data Transfer              |AmazonCloudFront   |%DataTransfer%              |                    |                                 |Yandex Cloud CDN                   |VK Content Delivery Network|SberDisk CDN |
|Cloud Service|Data Storage     |AWS                    |Custom SSL Certificates   |SSL Certificate Management |AmazonCloudFront   |SSL-Cert-Custom             |                    |                                 |Yandex Cloud CDN                   |VK Content Delivery Network|SberDisk CDN |
|application� |AI Diagnostic    |Enterprise AI Search   |Enterprise Edition        |Enterprise Search          |AmazonKendra       |%KendraEnterpriseEdition    |                    |                                 |YandexGPT API                      |-                          |Sber GigaChat|
|application� |AI Diagnostic    |Enterprise AI Search   |Document Processing       |Document Scanning          |AmazonKendra       |%DocumentsScanned           |                    |                                 |YandexGPT API                      |-                          |Sber GigaChat|
|application� |AI Diagnostic    |Enterprise AI Search   |Connector Sync            |Data Synchronization       |AmazonKendra       |%ConnectorSync              |                    |                                 |YandexGPT API                      |-                          |Sber GigaChat|
|application� |AI&ML Services   |AWS                    |AI Chatbots               |Voice Processing           |AmazonLex          |                            |                    |Tax%                             |Yandex SpeechKit + YandexDataSphere|-                          |Sber GigaChat|
|application� |AI&ML Services   |AWS                    |Request Processing        |Lex Requests               |AmazonLex          |%Req%                       |                    |                                 |Yandex SpeechKit + YandexDataSphere|Cloud Voice                |Sber GigaChat|
|Network DNS  |Network/Delivery |DNS Service            |                          |DNS Queries                |AmazonRoute53      |                            |                    |Tax%                             |Yandex Cloud DNS                   |VK Cloud DNS               |SberDisk DNS |
|Network DNS  |Network/Delivery |DNS Service            |Public DNS Queries        |Health Check Services      |AmazonRoute53      |%Health-Check-Option-AWS    |                    |                                 |Yandex Cloud DNS                   |VK Cloud DNS               |SberDisk DNS |
|Network DNS  |Network/Delivery |DNS Service            |Monitoring                |Health Check Services      |AmazonRoute53      |%Health-Check-AWS           |                    |                                 |Yandex Cloud DNS                   |VK Cloud DNS               |SberDisk DNS |
|Network DNS  |Network/Delivery |DNS Service            |Public DNS Queries        |DNS Queries                |AmazonRoute53      |%DNS-Queries                |                    |                                 |Yandex Cloud DNS                   |VK Cloud DNS               |SberDisk DNS |
|Network DNS  |Network/Delivery |DNS Service            |Public LBR Queries        |LBR Queries                |AmazonRoute53      |%LBR-Queries                |                    |                                 |Yandex Cloud DNS                   |VK Cloud DNS               |SberDisk DNS |
|Network DNS  |Network/Delivery |DNS Service            |DNS Queries               |Internal DNS Queries       |AmazonRoute53      |%Intra-AWS-DNS-Queries      |                    |                                 |Yandex Cloud DNS                   |VK Cloud DNS               |SberDisk DNS |
|Network DNS  |Network/Delivery |DNS Service            |Hosted Zone               |DNS Hosted Zone            |AmazonRoute53      |%HostedZone                 |                    |                                 |Yandex Cloud DNS                   |VK Cloud DNS               |SberDisk DNS |
|Network DNS  |Network/Delivery |DNS Service            |Monitoring                |Health Check Services      |AmazonRoute53      |%Health-Check-Non-AWS       |                    |                                 |Yandex Cloud DNS                   |VK Cloud DNS               |SberDisk DNS |
|Network DNS  |Network/Delivery |DNS Service            |Policy Management         |Traffic Flow Policy        |AmazonRoute53      |%Traffic-Flow-Policy-Records|                    |                                 |Yandex Cloud DNS                   |VK Cloud DNS               |SberDisk DNS |
|Network DNS  |Network/Delivery |DNS Service            |Monitoring                |Health Check Services      |AmazonRoute53      |%Health-Check%              |%Latency%           |                                 |Yandex Cloud DNS                   |VK Cloud DNS               |SberDisk DNS |
|Network DNS  |Network/Delivery |DNS Service            |Monitoring                |Health Check Services      |AmazonRoute53      |%Health-Check-Option-Non-AWS|                    |                                 |Yandex Cloud DNS                   |VK Cloud DNS               |SberDisk DNS |
|Network DNS  |Network/Delivery |DNS Service            |Geolocation Routing       |DNS Geo Queries            |AmazonRoute53      |%Geo-Queries%               |                    |                                 |Yandex Cloud DNS                   |VK Cloud DNS               |SberDisk DNS |
|Network DNS  |Network/Delivery |DNS Service            |Network Interface Usage   |Route 53 Resolver          |AmazonRoute53      |%ResolverNetworkInterface   |                    |                                 |Yandex Cloud DNS                   |VK Cloud DNS               |SberDisk DNS |


---

## ***Описание сервисов Azure*** ## 

__Amazon EC2__ облачная платформа с тысячами экземпляров, поддерживающая разные типы процессоров и предоставляющая гибкие тарифы для различных рабочих нагрузок.

__Compute Savings Plans__ предлагает скидки на вычислительные мощности при условии их использования в течение года или трёх лет.

__Reserved Consumption__ позволяет получить скидку до 22% за бронирование ресурсов на 6 месяцев или год вперёд.

__AmazonEC2RIResale2__ это Reserved Instance Marketplace, где можно купить или продать неиспользуемые экземпляры.

__AmazonCloudFront__ content delivery network для быстрой и безопасной доставки контента, ускорения загрузки сайтов и защиты от DDoS-атак.

__Amazon Kendra__ поисковый сервис, использующий AI для эффективного поиска информации, особенно в специфических областях.

__Amazon Lex__ сервис создания интерфейсов на базе AI, позволяющий разрабатывать и тестировать чат-ботов с использованием распознавания речи.

__Amazon Route53__ DNS-сервис, обеспечивающий маршрутизацию трафика, мониторинг и лёгкую настройку ремаршрутизации.

----
## ***российских аналогов (Yandex Cloud и VK Cloud)*** ##

__Yandex Compute Cloud__  Аналог EC2 с большим выбором процессоров, посекундная тарификация, оплата по использованию CPU/RAM и дисков.

__Cloud Servers__ Предлагает разнообразие ОС, включая российские дистрибутивы, привлекательно для государственных компаний. Посекундный биллинг, различные тарифы.

__Cloud Voice__ Подходит для автораспознавания и синтеза речи, работает стабильно, поддерживает потоковое аудио и звуковые файлы.

__Yandex Cloud Marketplace__ B2C рынок с выбором продуктов от различных вендоров, включая БД, сетевую инфраструктуру и многое другое.

__VK Cloud Marketplace__ Подобный Yandex Marketplace, управляемый и тарифицируемый самим ВК, включает как опенсорс, так и предоставляемые сервисы.

__Yandex Cloud CDN__ Почти идентичен функционалом, с акцентом на рынок Восточной Европы и России, предоставляет аналитику трафика, защиту от DDoS и более доступные цены.

__VK Content Delivery Network__ Аналогичный функционал CDN с более низкой задержкой и ЦОДами на 5 континентах.

__YandexGPT API__ Решение команды Яндекса для бизнеса и приложений, помогает улучшать контент, бесплатен с лимитом запросов, требует подписку для большего количества запросов, может быть дообучен через DataSphere.

__VK Cloud__ Предлагает только Cloud Vision для распознавания текста, объектов на фото и видео, а также для автоматизации.

__Yandex Cloud DNS__ Предоставляет создание доменных зон, оптимизацию запросов, мониторинг и конфигурацию через различные инструменты.

__VK Cloud DNS__ Предоставляет приватный и публичный DNS с простой настройкой.

__SberCloud__ Провайдер услуг и сервисов по моделям IaaS и PaaS (IT-инфраструктура в аренду) для бизнеса и государственных организаций.

__Sber GigaChat__ нейросеть от Сбера, которая умеет отвечать на вопросы, писать код, рисовать изображения по запросу на русском языке.

----
Все готово!


