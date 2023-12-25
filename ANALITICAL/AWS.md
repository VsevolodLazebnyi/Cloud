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

__Amazon EC2__ представляет собой безопасную платформу для облачных вычислений с низкой задержкой благодаря глобальному присутствию, в которой немного менее тысячи инстансов, поддерживающая все основные архитектуры процессоров (включая ARM) и является единственным облаком на рынке с сетью Ethernet 400 Гбит/с. Основные Selling points - максимальная гибкость, огромное количество тарифных планов в зависимости от рабочей нагрузки, потребностей и бюджетных ограничений (например, Memory Optimized подходит для приложений, требующих использование больших объёмов памяти, например, машинное обучение, запуск Hadoop, Accelerated Computing - для параллельной обработки данных и т.д.). Экземпляр EC2 - это виртуальная машина, которая получает определенный процент оперативной памяти, процессора, дисков и сетевых входов/выходов базового физического хоста. В первой строке биллинга встретился такой тип использования, как %Box Usage% это посекундная(!) оплата за использование инстанса EC2. AMIs, т.е. Amazon Machine Instances изначально спроектированы под увеличивающийся список операционок, в том числе их собственную (Amazon Linux 2), Windows (что редкость в российских аналогах), и огромный спимок дистрибутивов Линукс.

__Compute Savings Plans__ отличный инструмент экономии за счёт того, что пользователь обязуется использовать определённый объём вычислительной мощности в течение одного/трёх лет. Схема такая же, как при оптовых закупках - снижение цены за счёт большого количества покупаемой продукции. Размер скидки может доходить до 72%. Ещё одно преимущество для получателя услуги - неизменность цены на протяжение всего периода использования, т.е. инфляция не увеличит цену. Подробнее об условиях написано в AWS Cost Explorer. Существует несколько планов, включая All upfront (требует полной предоплаты за весь срок), Partial upfront (нужна частичная предоплата) и No upfront (без предоплаты, но с меньшей скидкой).

__Reserved Consumption__ возможность пользователям получить скидку до 22% за заблаговпеменную бронь ресурсов от 6 месяцев до года. Прекрасный способ экономии, суть работы та же, что и в AWS.

__AmazonEC2RIResale2__ относится к Reserved Instance Marketplace - уникальной P2P службой для купли-продажи инстансов. Это позволяет продавцам получить деньги за неиспользованные инстансы, а покупателям приобрести их дешевле. Как посредник, Amazon продает экземпляр (если кто-либо продаёт инстанс с такими параметрами) с самой низкой стоимостью, пока весь заказ покупателя не выполнится, а потом передает право собственности на зарезервированные экземпляры получателю. Прямых аналогов, предлагаемыми Яндексом и ВК, нет. "%RIResaleServiceFee" представляет собой сервисный сбор, взимающийся при продаже зарезервированного экземпляра на маркетплейсе.

__AmazonCloudFront__ является content delivery network, которая, как я уже описывала в прошлой лабораторной, позволяет максимально быстро и безопасно доставить контент сайтов, приложений в любой регион, так как серверы (Points Of Presence) расположены по равномерно по миру. Трафик пользователя направляется через глобальную сеть CDN для ускорения загрузки статического и динамического контента. Пользовательские запросы перенаправляются к ближайшему edge location, где контент кэшируется для быстрой доставки. Если контент не находится на краю сети, он извлекается из исходного местоположения. CloudFront также интегрируется с AWS Shield для защиты от DDoS-атак. За счёт быстрой загрузки сайта он поднимется выше в поисковике, что увеличит охваты. Один из подходящих сценариев использования CDN -раздача мультимедиа. Например, среди клиентов есть SUPERCELL, поэтому можно с низким пингом играть в Brawl Stars даже в Африке.

__Amazon Kendra__ представляет собой поисковый сервис на основе AI, который воспринимает поисковые запросы в виде естественных вопросительных предложений и применяет алгоритмы глубокого обучения для выявления контекста. Она полностью самостоятельна, пользователям не нужны собственные серверы, а также разработка, обучение и применение отдельных ML-моделей. Служба оптимизирована под узкие сферы и хорошо 'понимает' специфическую терминологию, в том числе научную, даже во  всех презентационных материалах позиционируется как enterprise-поисковик. Kendra может подключаться к различным источникам данных для индексации и поиска информации - коннекторам. Они облегчают интеграцию с популярными хранилищами данных, что делает поисковые запросы актуальными. 

__Amazon Lex__ работает на том же движке, что и голосовой помощник Alexa, создаёт интерфейсы. Он использует понятия намерений (intent) для определения действий, которые необходимо выполнить, промптов для запроса данных от пользователя, слотов (slot) для сбора необходимых данных, и обработку (fulfillment) для выполнения намеренных действий. Благодаря этому Lex по сути повторяет пайплайн работы программиста-создателя чат-ботов, не только разрабатывая, подстраиваясь под нужды конкретного бота, но и тестируя, доводя до конечной версии (что пугает меня). Распознавание речи подходит под работу со звуком с частотой дискретизации 8 кГц, то есть с обычным смартфоном.

Прямых аналогов к такому инновационному решению нет, однако __Cloud Voice__ от ВК и __Yandex SpeechKit + YandexDataSphere__ от Яндекса могут частично справиться. Первый подходит для автораспознавания и синтеза речи, имитирующей естесственную. Работает стабильно, ибо у VK есть стабильный и хорошо звучащий голосовой ассистент Маруся. Работает и с потоком аудио, и с отдельными звуковыми файлами, то есть можно использовать и для поддержки, коллцентра, и для озвучки контента. Пара сервисов Яндекса вместе тоже могут приблизиться к закрытию тех же задач, что и Lex: Первый создаёт голосовых ассистентов с реалистичным голосом, распознаванием речи и аналитикой клиентов для автоматизации бизнесов. DataSphere же предоставляет инструменты для всего ML пайплайна: от подготовки данных, виртуального окружения и библиотек до предоставления вычислительных мощностей для обучения моделей. Однако, Amazon Lex работает гораздо более автономно.

__Amazon Route53__ это не просто платформа, которая наибыстрейшим образом преобразует доменные имена в IP-адреса для направления трафика на сайт (проще говоря, DNS-сервис), но и соединяет запросы с инфраструктурой, работающей в AWS, с помощью большого числа типов маршрутизации управляет трафиком, позволяет мониторить, оперативно выявлять сбои и легко настроить ремаршрутизацию. Также, как и остальные сервисы AWS, Route53 безопасна, масштабируема и предоставляет широчайший выбор тарифных планов. Однако, он не поддерживает DNSSEC и не предоставляет опции переадресации для доменов, используемых в локальной сети.

----
## ***российских аналогов (Yandex Cloud и VK Cloud)*** ##

__Yandex Compute Cloud__ также является сервисом облачных вычислений, является точным аналогом EC2, и, в отличие от VK, предоставляет большую вариативность физических процессоров, включая AMD EPYC. Тарификация так же посекундная. Система списывания денег за ВМ такая же, как у AWS и VK - за использование CPU/RAM деньги снимаются только при работающей машине, а за диски - вне зависимости от работы виртуалки.

__Cloud Servers__ Из доступных ОС есть российские дистрибутивы Linux (AlmaLinux, AstraLinux, Red OS, Альт Сервер), а также Ubuntu, Debian, CentOS и пару других, что делает решение привлекательным для государственных компаний. предлагают только процессоры Intel Xeon Gold, так же, как и в AWS есть посекундный биллинг (Pay-as-you-go) для оплаты исключительно того объёма услуг, которую расходуешь. Также есть готовые конфигурации тарифов: basic, standard и advanced

Ниже представлены скрины, отображающие максимальную схожесть по цене решений по виртуализации Yandex Compute Cloud и VK Cloud Servers при схожих конфигурациях.

__Yandex Cloud Marketplace__ вообще сложно отнести к аналогам, ибо это не P2P, а B2C рынок, предоставляющий клиентам выбрать продукты среди разнообразных сторонних вендоров. В отличие от AmazonEC2RIResale2, там присутствуют не только инстансы, но и продукты из таких категорий, как БД, сетевая инфраструктура, VoIP, ОС, удалённые рабочие столы и т.д.

__VK Cloud Marketplace__ суть та же, что и у Яндекса, но маркетплейс меньше по охвату поставщиков. Сам ВК не просто бездействующий посредник, но и подготавливает экземпляр сервиса, управляет и тарифицирует его. В маркетплейс входят как опенсорс сервисы, так и предоставляемые дистрибьютором.

__Yandex Cloud CDN__ предоставляет почти абсолютно аналогичный функционал, только сосредоточен больше на рынке Восточной Европы и России. Всего CDN-ов более 140. Также Яндекс предоставляет инструменты аналитики трафика и запросов. Также, как и в AWS присутствует защита от ддос атак. Цены демократичнее, чем у AWS.

__VK Content Delivery Network__ суть та же, что и в первых двух сервисах. Основной сервер разгружен, а CDN принимвют на себя весь трафик. Производитель заявляет среднюю задержку в 20 мс и более 400 ЦОДов на 5 континентах (Хотя в Южной Америке лишь 1).

__YandexGPT API__ предлагает использовать разработанную командой Яндекса модель для бизнес-нужд, приложений, в общем, продвигается больше как B2B решение, хотя и стало популярным среди обычных пользователей. Он пока находится в бета-версии. Уже неплохо справляется с улучшением контента, лендингов, копирайтом/рерайтом. Бесплатен, но для ликвидации лимита на количество запросов нужно приобрести подписку, также стоимость рассчитывается по числу токенов в запросе, модели (есть YandexGPT Lite и YandexGPT2) и режиму (синхронный/асинхронный). Интересной фишкой является и то, что LLM можно дообучить, отправив JSON с запросами и ответами через DataSphere.

У VK Cloud из отдалённо похожих сервисов есть только __Cloud Vision__ для распознавания текста, документов, объектов на видео и фото. Также служит инструментом для автоматпзации человеческого труда и является B2B решением.
__Yandex Cloud DNS__ так же, как и Route53, не только предоставляет возможность создания доменных зон и оптимизирует запросы, но и даёт возможность для мониторинга и конфигурации через консоль Yandex Cloud, API, CLI и Terraform.

__VK Cloud DNS__ предоставляет приватный и публичный DNS, в остальном функционал скуден, зато настройка очень простая.

----
Все готово!


