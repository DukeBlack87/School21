# **Архитектура**

## **Уровни веб-приложения**

## Существует четыре общих уровня веб-приложений

- Уровень представления (PL)
- Уровень обслуживания данных (DSL)
- Уровень бизнес-логики (BLL)
- Уровень доступа к данным (DAL)

## ***Уровень представления***

PL отображает пользовательский интерфейс и упрощает взаимодействие с пользователем. Уровень представления имеет компоненты пользовательского интерфейса, которые визуализируют и показывают данные для пользователей. Также существуют компоненты пользовательского процесса, которые задают взаимодействие с пользователем. PL предоставляет всю необходимую информацию клиентской стороне. Основная цель уровня представления - получить входные данные, обработать запросы пользователей, отправить их в службу данных и показать результаты.

## ***Уровень службы данных***

DSL передает данные, обработанные уровнем бизнес-логики, на уровень представления. Этот уровень гарантирует безопасность данных, изолируя бизнес-логику со стороны клиента.

## ***Слой бизнес-логики***

BLL несет ответственность за надлежащий обмен данными. Этот уровень определяет логику бизнес-операций и правил. Вход на сайт - это пример уровня бизнес-логики.

## ***Уровень доступа к данным***

DAL предлагает упрощенный доступ к данным, хранящимся в постоянных хранилищах, таких как двоичные файлы и файлы XML. Уровень доступа к данным также управляет операциями CRUD - создание, чтение, обновление, удаление.

## **Монолитная архитектура**

Монолитная архитектура означает, что приложение — большой связанный модуль, все компоненты которого спроектированы для совместной работы, используя общую память и ресурсы.

Обычно все функции содержатся в единой кодовой базе, написанной на одном языке программирования и технологическом стеке. Например, если вы создаете интернет-магазин для продажи футболок, у вас может быть одно приложение, которое обрабатывает оформление заказа, платежи, отвечает за управление запасами и за обновление заказов.

Монолитные приложения — это не всегда плохо. Для простых приложений они могут быть идеальными.

Монолиты подходят для некоторых приложений, но для более сложных систем вы можете пойти дальше и разбить их на микросервисы.

## **Микросервисная архитектура**

Микросервисная архитектура означает, что приложение состоит из маленьких независимых приложений, использующих собственные ресурсы и развивающихся независимо друг от друга, которые потенциально могут быть размещены на разных машинах.

Микросервисы — это архитектурный шаблон, который упорядочивает приложение как набор слабосвязанных мелкомодульных сервисов, взаимодействующих через облегченные протоколы. Это отличается от монолита, который представляет собой приложение, написанное на одном языке и работающее вместе как одна единица кода.

## **Различия между монолитом и микросервисами**

Традиционная монолитная архитектура веб-приложения состоит из трех частей - базы данных, клиентской и серверной сторон. Это означает, что внутренняя и внешняя логика, как и другие фоновые задачи, генерируются в одной кодовой базе. Чтобы изменить или обновить компонент приложения, разработчики программного обеспечения должны переписать все приложение.

Что касается микросервисов, этот подход позволяет разработчикам создавать веб-приложение из набора небольших сервисов. Разработчики создают и развертывают каждый компонент отдельно.

Архитектура микросервисов выгодна для больших и сложных проектов, поскольку каждый сервис может быть изменен без ущерба для других блоков. Поэтому, если вам нужно обновить логику оплаты, вам не придется на время останавливать работу сайта.

Известные проекты: Netflix, Uber, Spotify, PayPal.

## **Почему не все приложения построены на микросервисной архитектуре?**

В традиционном монолитном сервисе каждый экземпляр микросервиса представлен в виде модуля системы. Связь между ними осуществляется в памяти, а задержка близка к нулю. Внедрение микросервисов означает, что коммуникация между службами переходит от транзакций в памяти к сетевым инструкциям.

Есть множество проверенных решений этой проблемы, но все они имеют свою цену — задержку. Переход от транзакций, которые выполняются в памяти, к сетевой связи, увеличивает единицу задержки с наносекунд (нс) до микросекунд (мс).

Представьте, что три разных сервиса общатся друг с другом по сети. Если каждый вызов службы занимает 100 мс (а так нередкое бывает под нагрузкой), 300 мс придется тратить только на ожидание ответа сети.

Некоторые приложения по своей природе тесно интегрированы с компонентами и сервисами. Дополнительный уровень связи, который увеличивает задержку, может привести к катастрофическим результатам — например, в приложениях, которые обрабатывают данные в реальном времени. Представьте, что вы решили увеличить задержку связи диспетчеру в аэропорту или хирургу во время операции — это почти то же самое.

- ***Дополнительная сложность.*** Да, сложность решения не может быть определена количественно и сравнивать ее можно только в относительном выражении. Хотя изначально микросервисы предназначены для того, чтобы упростить архитектуру приложения за счет разделения монолита на части, микросервисная архитектура сложна в развертывании и обслуживании.

- ***Стоимость развертывания.*** Микросервисы — это распределенные системы с молекулярной структурой, а распределение имеет свою цену. Если монолит можно развернуть на одной виртуальной машине или в контейнере, то каждой службе в микросервисной структуре (по крайней мере, в идеальном мире) требуется отдельная виртуальная машина или контейнер. Их объем меньше, чем у монолита, но, скорее всего, они обойдутся дороже даже без учета стоимости обслуживания.

- ***Команда DevOps.*** Без команды DevOps поддерживать и контролировать микросервисы не получится, а найм таких специалистов может и помочь, и навредить компании. С одной стороны, DevOps — это широко распространенное и проверенное операционное решение. Но если компания небольшая, найм таких специалистов скорее принесет убытки, чем сделает организацию более прогрессивной.

- ***Высокая связанность компонентов.*** Некоторые части сервиса тесно связаны друг с другом. Попытка разделить их только для того, чтобы «вписаться» в архитектуру, может закончиться катастрофой. Отсутствие опыта. Отсутствие опыта имеет решающее значение при решении любых проблем — в том числе вопросов, связанных с сервисно-ориентированной архитектурой. Когда дело доходит до микросервисов, ущерб приумножается: если вы разворачиваете сервисы в неправильном порядке или происходит сбой, при котором один из зависимых сервисов выходит из строя, менять что-то может быть слишком поздно.

- ***Сквозное тестирование.*** Традиционное монолитное приложение позволяет запускать тесты почти мгновенно. Наличие нескольких сервисов с взаимозависимостью приведет к задержке тестирования без жизнеспособной оркестрации. Хаотические контракты на данные. Разработка и хранение контрактов на данные внутри команды сильно отличается от обмена ими между командами. При работе с микросервисами ваша команда может не находиться в одном регионе, не говоря уже об использовании одного и того же языка программирования. Выработка контрактов с данными для особых нужд будет стоить вам времени и места.

- ***Устаревшая база кода.*** Давайте будем честны — большинство из нас каждый день работает с устаревшей базой кода. Быстро развитие технологий двигает нас вперед, но в то же время они еще больше изолируют нас от legacy-кода. Вы уверены, что только что разработанный фреймворк на RabbitMQ, будет хорошо работать с устаревшим приложением на IBM AIX?

- ***Проблемы при отладке.*** Каждая служба будет иметь собственный набор файлов журнала для анализа. Чем больше сервисов, тем больше файлов.

**Монолитная** архитектура идеальна для небольших приложений благодаря быстрой разработке, простоте тестирования и отладки, а также низкой стоимости.

Использование **микросервисов** дает множество преимуществ. Они позволяют создавать более модульные и удобные в сопровождении приложения с меньшим риском поломки при внесении изменений. Они также предоставляют вашей команде больше гибкости во взаимодействии над проектом, облегчая им продуктивную работу на всех уровнях опыта — от младших разработчиков до тех, кто работает с этими типами систем в течение многих лет.

### **Нет никакой идеальной архитектуры. Как и c языком программирования, мы всегда выбираем архитектуру в зависимости от задачи.**

## **Особенности тестирования монолитных и микросервисных веб-приложений**

Монолит вы тестируете один сервис независимо от каких-либо зависимостей. Обычно все очевидно.
По сравнению с программным обеспечением на основе микросервисов тестирование монолитного приложения значительно проще. Нам осталось только запустить наше приложение, убедиться и протестировать его подключение к базовой базе данных. Каждая служба в приложении на основе микрослужб должна сначала запускаться и тестироваться отдельно. После того как все сервисы запущены, необходимо еще раз протестировать приложение в целом.
