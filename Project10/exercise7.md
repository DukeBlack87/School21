# Нагрузка, стресс и отказоустойчивость

## нагрузочное тестирование

Его еще называют Load Testing. Главная задача нагрузочного тестирования заключается в проверке работоспособности системы, варьируя постепенный рост нагрузки от минимальной до пиковой. Максимально допустимый показатель указывается в настройках.

Суть нагрузочного тестирования состоит в замере соотношения отклика ресурса и скорости обработки запросов от пользователей, т.е. как быстро открывается вкладка, скорость проведения расчетов. При таком тестировании определяется потребление ресурсов сервера, а сама проверка начинается с плавного увеличения нагрузки.

Цель нагрузочного тестирования – определение, насколько приложение или сайт выполняют свои задачи в нормальных условиях и при повышенном количестве запросов. Стоит отметить, что нагрузочное тестирование создает ожидаемую нагрузку от пользователей.

Теперь рассмотрим такой тест на примере среднего интернет-магазина. При проектировании ресурса мы ожидаем, что наша площадка должна выдерживать одновременную нагрузку, как минимум, от 4 тыс. пользователей. Максимально идеальный вариант отклика сайта в таком случае должен не превышать 3 секунд.

Нагрузочное тестирование создает вышеупомянутую нагрузку и одновременно определяется время отклика. Если оно выше ожидаемого, тогда у сервера при росте посещаемости проблемы, и ваш интернет-магазин будет тормозить.

### Основные отличия нагрузочного тестирования

- помогает определить надежность работы сайта или приложения;
- помогает понять работу сайта или приложения под нагрузкой;
- главный параметр для проверки — время ответа сервера;
- измеряется производительность системы в зависимости от различного количества пользователей;
- нагрузочное тестирование — часть стрессового тестирования;
- проходит по точно заданным требованиям, основанным на определенном количестве пользователей, времени ответа, пропускной способности, некоторых параметрах по проверке состояния сервера/приложения.

## Стресс-тестирование

Стресс и нагрузочное тестирование несколько похожи. Но в отличие от второго, в первом нагрузка эмулируется на протяжении длительного промежутка времени, например, на 2-3 часа.

Цель стресс-тестирования заключается в определении «стрессоустойчивости» сервера. В идеале он должен работать при любой нагрузке, хоть медленно, но работать. Даже, если одновременно ваш интернет-магазин посещают, скажем, 10 тыс., интернет-магазин не должен «падать».

Еще одна схожесть с нагрузочным тестированием состоит в том, что нагрузка эмулируется, плавно начиная от минимального и заканчивая максимальным значением. При достижении определенного показателя нагрузка останавливается и измеряется скорость реакции сервера. Цель стресс теста — убедится, что несмотря на медленную работу за пределами допустимой нагрузки сервер не падает, хоть и работает медленно.

На каждом тарифе хостинга ресурсы не бесконечные и по мере роста нагрузки наступит момент, при котором сервер будет в не состоянии обработать N-ое количество запросов. Итог – при попытке зайти на сайт вылетит соответствующая ошибка.

И вот, когда потребление ресурсов превысит их количество, сервер перестанет работать, и тестировщики получают данные об объеме пропускной способности, т.е. сколько сайт одновременно может принять пользователей.

### Основные отличия стресс-тестирования

- Основные характеристики стресс-тестирования:
- определяем стабильность работы;
- основная цель — определить предел прочности сервера;
- целевой параметр для проверки — пропускная способность;
- стресс тест — комплексный тест, включающий нагрузочное тестирование;
- стрессовое тестирование — это тестирование на чрезмерную нагрузку, включая неожиданное большое количество пользователей.

## Тестирование отказоустойчивости

Тестирование отказоустойчивости (failover testing): Тестирование при помощи эмуляции отказов системы или реально вызываемых отказов в управляемом окружении. После вызванного отказа проверяется механизм отказоустойчивости с целью удостовериться, что данные не потеряны или не испорчены, и достигнут оговоренный уровень обслуживания (например, доступности функций или время отклика).

Тестирование на отказ и восстановление (Failover and Recovery testing, Disaster Recovery Testing) - подвид тестирования производительности, проверяет тестируемый продукт с точки зрения способности противостоять и успешно восстанавливаться после возможных сбоев, возникших в связи с ошибками ПО, отказами оборудования или проблемами связи/сети. Failover - проверка систем восстановления (или дублирующих основной функционал систем), которые, в случае возникновения сбоев, обеспечат сохранность и целостность данных тестируемого продукта. Методика подобного тестирования заключается в симулировании различных условий сбоя, последующем изучении и оценке реакции защитных систем. В процессе подобных проверок выясняется, была ли достигнута требуемая степень восстановления системы после возникновения сбоя. В отличие от тестирования надежности (Reliability Testing), которое проводится, чтобы найти отказ в конкретной точке, где он происходит, Recovery Testing проводится для проверки того, насколько хорошо система восстанавливается после сбоя или аварии.

### Основные отличия тестирования отказоустойчивости

- Проблемы с сетью;
- Сбой питания;
- Внешний сервер недоступен (External server not reachable);
- Сервер не отвечает (Server not responding);
- Отсутствует файл dll;
- Перегрузка базы данных;
- Остановленные сервисы/службы;
- Физические условия;
- Внешнее устройство не отвечает;
- Потеря сигнала беспроводной сети;

## Различия нагрузочного, стресс теста и отказоустойчивости

- **Нагрузочное тестирование** – увеличение нагрузки до пикового значения, при котором система начнет тормозит. Касательно стрессовой проверки, то тестирование заключается в постоянной перегрузке ресурса до тех пор, пока сервер полностью «не ляжет».

- **Stress Testing** или как его называют «стрессовый тест» показывает скорость отклика вашего ресурса, когда оказываемая нагрузка значительно превышает норму, указанную в требованиях к проекту.

    Обязательно ли проводить стресс тест? Если вы допускаете расширение пользовательской базы, тогда тестирование стрессоустойчивости необходимо. Оно покажет поведение сайта при резком увеличении посещаемости. Крайне важно, чтобы ресурс все равно работал, даже если нагрузка будет значительно больше, чем устойчивость сервера. Иначе потерю клиентов не избежать. Поэтому при покупке тарифа у хостинга учитывайте рост посещаемости.

- **Тестирования отказоустойчивости.** После вызванного отказа проверяется механизм отказоустойчивости с целью удостовериться, что данные не потеряны или не испорчены, и достигнут оговоренный уровень обслуживания

## Примеры выполнения видов тестирования (в контексте проверки базы данных большого веб-приложения)

### Нагрузочное тестирование

Проверка, как одновременное выполнение множества транзакций влияет на производительность БД.

Время ответа при выполнении транзакций многочисленными удаленными пользователями
Время, затрачиваемое на выполнение отдельных интересующих запросов к БД

**Примеры:**

- Многократное выполнение самых частых транзакций, для оценки общей производительности БД
- Передача и прием больших файлов
- Параллельный запуск многих других приложений на одном сервере

### Стресс тестирование

Направлено на поиск «точки отказа» системы. С этой целью систему подвергают стрессу большим количеством одновременных запросов. Устойчивость подсистемы баз данных требует тщательного планирования, включая определение «точки отказа».

В основном для стресс-тестирования применяются инструменты LoadRunner и конечно JMeter.

**Пример:**

- Имеем например CRM-приложение автоматизации продаж, которое может выдержать максимально 50000 одновременных пользователей. А если увеличить нагрузку до 51000, параллельно выполняя транзакции обновления или добавления записей в БД? После каждой транзакции приложение должно синхронизироваться с БД. Если все прошло без проблем, нагрузка увеличивается до 52000, и т.п.

### Тестирование отказоустойчивости.

Проверка восстановления базы данных после возможного сбоя: работает ли БД и приложение корректно, восстановились ли данные, есть ли методология восстановления.

**Примеры:**

- Также проверяют, выполняются ли критически важные процедуры во время и после сбоя.
- Ищут ошибки в программах резервного копирования и восстановления
- Проверяют последовательность и правильность процедур восстановления
- Возможность восстановления критически важных данных после масштабного сбоя

## Инструменты для проведения нагрузочного тестирования баз данных

### Apache JMeter

Apache JMeter – на настоящий момент один из самых популярных инструментов с открытым исходным кодом для нагрузочного тестирования. Инструмент разрабатывается с 2003 года и за прошедшие десятилетия оброс богатой функциональностью и достаточно давно успел себя зарекомендовать, как прекрасную альтернативу платным аналогам для большинства решаемых задач.

Инструмент кроссплатформенный, так как разработан на Java. Доступна как работа из GUI, так и запуски в консольном режиме.

Apache JMeter поддерживает работу с различными сетевыми протоколами разных уровней HTTP, HTTPS, FTP, LDAP, SOAP, TCP, почтовых протоколов и shell-скриптов. Он, как java-based инструмент, предоставляет возможности по работе с JDBC, Message-oriented middleware (MOM) через JMS и Java Objects.

Если вам этого недостаточно и нужно решение какой-либо специфической задачи, то JMeter можно расширить, написав к нему своё расширение или используя существующие, доступные в менеджере плагинов. Например, можно из JMeter запускать даже .Net-код, используя jni4net, или проводить тестирование с помощью графического citrix-ica протокола.

Для высоких нагрузок запуска одного инстанса JMeter может и не хватить, но эта проблема решаема тюнингом конфигурационных файлов инструмента или использованием распределенного запуска.

JMeter действительно очень популярен в отрасли, об этом говорит тот факт, что некоторые инструменты из нашего списка используют JMeter в качестве своего движка.

### Яндекс.Танк

Не секрет, что в компании Яндекс имеется своя экосистема различных инструментов для абсолютно разных задач. Некоторые говорят, что если есть возможность написать свой инструмент, то Яндекс обязательно это сделает (иногда без оглядки на уже имеющиеся решения).  Не обошла стороной эта тема и инструменты для нагрузочного тестирования.

После своего создания в 2006 году, Танк прошёл длинный путь своего развития и сейчас позволяет использовать разные типы генераторов нагрузки. Если нужно протестировать http-сервис на высокую нагрузку, то используется Phantom (C++). Интеграция Танка с JMeter в свою очередь позволяет реализовать сценарный тип тестирования со всеми протоколами, которые поддерживаются JMeter.

Кроме того, можно использовать BFG-Python-генератор и написанный на Go Pandora.

Сам Танк реализован на Python и может использоваться только в Unix-системах.

### Gatling

Gatling – это ещё один популярный инструмент для проведения нагрузочного тестирования с открытым исходным кодом. Он написан на языке Scala с использованием технологий Netty и Akka.

Если Вы – разработчик, знакомый со Scala и Вам нужно провести нагрузочное тестирование, то Gatling – идеально вам подойдёт.

Скрипты на gatling пишутся в привычной среде разработки, и поддерживают инструменты автоматизации сборки sbt и maven. Также реализована возможность встраивания в процессы непрерывной интеграции с помощью Jenkins.

Удобство gatling для разработчика также состоит в том, что по завершении тестирования отчёт создаётся автоматически, его остаётся только проанализировать.

Что касается поддержки протоколов, то согласно официальной документации поддерживаются HTTP(s)/1, websocket, JMS, MQTT. Протокол HTTP 2.0 имеет ограниченную поддержку.

## Способы оптимизации баз данных

### Оптимизация запросов

В большинстве случаев проблемы с производительностью вызваны низкой производительностью SQL-запросов. При попытке оптимизировать эти запросы вы столкнетесь со многими дилеммами, например, использовать ли IN или EXISTS, писать ли подзапрос или объединение. Хотя вы можете платить хорошие деньги за консультационные услуги, вы также можете ускорить запросы SQL с помощью оптимизаторов запросов, которые ускорят запрос и объяснят рекомендации, чтобы вы могли учиться на будущее.

### Создать оптимальные индексы

При правильной индексации можно оптимизировать продолжительность выполнения запроса и повысить общую производительность базы данных. Индексы достигают этого, внедряя структуру данных, которая помогает поддерживать порядок и облегчает поиск информации; в основном, индексирование ускоряет процесс поиска данных и делает его более эффективным, тем самым экономя ваше время (и вашу систему) и усилия.

### Приобрести более мощный процессор

Чем лучше ваш процессор, тем быстрее и эффективнее будет ваша база данных. Поэтому, если ваша база данных работает не так, вы должны рассмотреть возможность обновления процессорного модуля более высокого класса; чем мощнее ваш процессор, тем меньше нагрузка при работе с несколькими приложениями и запросами. Кроме того, при оценке производительности ЦП важно отслеживать все аспекты производительности ЦП, в том числе время готовности ЦП (которое может рассказать вам о случаях, когда ваша система пыталась использовать ЦП, но не смогла, поскольку все ресурсы ЦП были слишком заняты или иным образом заняты).

### Выделите больше памяти

Подобно тому, как недостаточно мощный процессор может повлиять на эффективность базы данных, так же как и нехватка памяти. В конце концов, когда в базе данных недостаточно памяти для выполнения запрашиваемой работы, производительность базы данных по понятным причинам пойдет на спад. По сути, наличие большего объема памяти поможет повысить эффективность системы и общую производительность. Хороший способ проверить, нужно ли вам больше памяти, — посмотреть, сколько ошибок в вашей системе имеет страница; Если количество сбоев велико (например, в тысячах), это означает, что вашим хостам не хватает (или, возможно, полностью не хватает) доступного пространства памяти. Следовательно,

Кроме того, вы можете рассмотреть вопрос об увеличении объема памяти, используемой MySQL. Мы рекомендуем разрешить ему выделять 70% общей памяти (при условии, что база данных является единственным приложением на этом сервере). Вы можете изменить объем памяти, выделенной для базы данных, используя ключ innodb_buffer_pool_size в файле конфигурации MySQL, my.cnf.

### Дефрагментация данных

Если у вас проблемы с медленной базой данных, другим возможным решением является дефрагментация данных. Когда в базу данных записывается много записей и время идет, записи фрагментируются во внутренних файлах данных MySQL и на самом диске. Дефрагментация диска позволит сгруппировать соответствующие данные, поэтому операции, связанные с вводом/выводом, будут выполняться быстрее, что напрямую повлияет на общую производительность запросов и базы данных. Кроме того, на некотором связанном примечании также важно иметь достаточно дискового пространства вообще, работая с базой данных; если вы действительно хотите оптимизировать производительность базы данных, обязательно используйте дефрагментацию диска, сохраняя при этом достаточно свободного дискового пространства для вашей базы данных.

### Типы дисков

Для извлечения результатов даже одного запроса могут потребоваться миллионы операций ввода-вывода с диска, в зависимости от объема данных, к которым запрос должен получить доступ для обработки, и в зависимости от объема данных, возвращаемых из запроса. Таким образом, тип дисков на вашем сервере может сильно повлиять на производительность ваших SQL запросов. Работа с SSD-дисками может значительно повысить общую производительность базы данных и, в частности, производительность SQL-запросов.

### Версия базы данных

Другим важным фактором производительности базы данных является версия MySQL, которую вы в настоящее время развертываете. Обновление последней версии базы данных может существенно повлиять на общую производительность базы данных. Возможно, что один запрос может работать лучше в старых версиях MySQL, чем в новых, но если посмотреть на общую производительность, новые версии, как правило, работают лучше.