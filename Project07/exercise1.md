## Алгоритмы балансировки нагрузок

Рано или поздно веб-приложения перерастают среду одного сервера. Компаниям требуется увеличить или их доступность, или масштабируемость, или и то, и другое. Чтобы сделать это, они развёртывают своё приложение на нескольких серверах и ставят перед ним балансировщик нагрузок для распределения входящих запросов. Чтобы справляться с нагрузками, большим компаниям могут потребоваться тысячи серверов, на которых запущено веб-приложение.

Начнём сначала: с одного балансировщика нагрузок, отправляющего запросы одному серверу. Запросы отправляются с частотой 1 запрос в секунду (request per second, RPS), и каждый запрос постепенно уменьшается в размере, пока сервер обрабатывает его.

Для многих веб-сайтов такая система вполне работает. Современные серверы мощны и способны обрабатывать множество запросов. Но что будет, если они перестанут справляться?

Мы видим, что при частоте 3 RPS — часть запросов отбрасывается. Если запрос поступает на сервер, пока обрабатывается другой запрос, то сервер его отбросит. Это приводит к тому, что у пользователя отображается ошибка, и такую ситуацию нужно избегать. Чтобы устранить проблему, можно добавить к нашему балансировщику нагрузок ещё один сервер.

Отбрасываемых запросов больше нет! Наш балансировщик нагрузок в этом случае отправляет по очереди запрос каждому серверу; это называется балансировкой нагрузок циклическим перебором (**round robin**). Это одна из самых простых разновидностей балансировки нагрузок, которая хорошо работает, когда серверы имеют одинаковую мощность, а запросы одинаково затратны.

Можно улучшить round robin так, чтобы он лучше справлялся с колебаниями. Существует алгоритм, называющийся **weighted round robin** (взвешенный цикличный перебор); он заключается в том, что люди присваивают каждому серверу вес, определяющий, сколько запросов ему отправлять.

В этой симуляции мы используем в качестве веса каждого сервера его известное значение мощности, и отдаём более мощным серверам больше запросов при их циклическом обходе.

Хотя это позволяет лучше справляться с колебаниями мощности серверов, чем стандартный round robin, нам всё равно нужно решить вопрос колебаний запросов. На практике ручное указание весов быстро оказывается неэффективным. Сложно свести производительность сервера к одному числу, и для этого потребуется тщательное тестирование нагрузок с реальными рабочими нагрузками. Это делают редко, поэтому другой вариант weighted round robin вычисляет веса динамически при помощи вспомогательной метрики: задержки.

Логично, что если один сервер обрабатывает запросы в три раза быстрее, чем другой сервер, то, вероятно, он в три раза быстрее и должен получать в три раза больше запросов.

Добавим к каждому серверу текст, отображающий среднюю задержку трёх последних обработанных запросов. Затем мы решаем, отправить ли 1, 2 или 3 запроса каждому серверу, на основании относительного различия в задержках. Результат очень схож с исходной симуляцией weighted round robin,
но отсутствует необходимость заранее указывать вес каждого сервера. Этот алгоритм также сможет адаптироваться к изменениям производительности сервера со временем. Это называется **dynamic weighted round robin**.

Балансировкой нагрузок по принципу **least connections** (наименьшего количества соединений).

Так как балансировщик нагрузок находится между сервером и пользователем, он может точно отслеживать, сколько ожидающих запросов есть у каждого сервера. То есть при поступлении нового запроса и необходимости выбора, куда его отправить, он знает, у каких из серверов меньше всего работы, и отдаёт приоритет им.

Этот алгоритм работает чрезвычайно хорошо вне зависимости от степени колебаний. Он избавляет от неопределённости, обеспечивая точное понимание того, чем занят каждый из серверов. Он обладает и ещё одним преимуществом: простотой реализации. Поэтому такой алгоритм является стандартным методом балансировки HTTP-нагрузки в балансировщиках нагрузок AWS. Он также используется как опция в nginx, и с ним стоит поэкспериментировать, если вы никогда не меняли стандартный метод.

Хотя этот алгоритм имеет хороший баланс между простотой и производительностью, у него нет иммунитета к отбрасыванию запросов. Однако можно заметить, что это единственный случай, когда алгоритм отбрасывает запросы только в случае полного отсутствия места в очередях. Он обеспечивает использование всех доступных ресурсов, поэтому для большинства нагрузок может стать отличным выбором по умолчанию.

| Алгоритм | Описание |
| ------ | ------ |
| ROUND ROBIN (ПО-КРУГОВОЙ) | Последовательно распределяет запросы на первый доступный сервер и по завершении перемещает этот сервер в конец очереди. Алгоритм Round Robin используется для пулов равных серверов, но он не учитывает нагрузку, уже имеющуюся на сервере. |
| LEAST CONNECTIONS (НАИМЕНЬШЕЕ КОЛИЧЕСТВО ПОДКЛЮЧЕНИЙ) | Алгоритм наименьшего количества подключений предполагает отправку нового запроса наименее загруженному серверу. Метод наименьшего соединения используется, когда в пуле серверов много неравномерно распределенных постоянных соединений. |
| LEAST RESPONSE TIME (НАИМЕНЬШЕЕ ВРЕМЯ ОТКЛИКА) | Балансировка нагрузки с наименьшим временем отклика распределяет запросы на сервер с наименьшим количеством активных подключений и с самым быстрым средним временем отклика на запрос мониторинга работоспособности. Скорость отклика показывает, насколько загружен сервер. |
| HASH (ХЕШ) | Алгоритм хеширования определяет, куда распределять запросы, на основе назначенного ключа, такого как IP-адрес клиента, номер порта или URL-адрес запроса. Метод Hash используется для приложений, которые полагаются на сохраненную информацию о пользователях, например, тележки на веб-сайтах интернет магазинов. |
| CUSTOM LOAD (ПОЛЬЗОВАТЕЛЬСКАЯ НАГРУЗКА) | Алгоритм Custom Load направляет запросы к отдельным серверам через SNMP (Simple Network Management Protocol). Администратор определяет нагрузку на сервер, которую балансировщик нагрузки должен учитывать при маршрутизации запроса (например, использование ЦП и памяти, а также время ответа). |

