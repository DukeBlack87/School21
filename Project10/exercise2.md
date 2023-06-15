# Что такое Local Storage и Session Storage?

***Local Storage*** и ***Session Storage*** - это возможности браузера сохранять информацию на стороне клиента. Обе эти технологии позволяют программистам хранить данные в браузере пользователя без необходимости отправлять их на сервер. ***Локальное хранилище (Local Storage)*** и ***сессионное хранилище (Session Storage)*** - две различные спецификации, которые используются в браузере для хранения данных. ***Local storage*** и ***session storage*** используются в ***JavaScript*** для хранения локальных данных, таких как настройки пользователя, история просмотра и т.д. Обе технологии очень полезны для создания приложений, которые могут работать в автономном режиме или для хранения настроек пользователя на длительное время.

## В чём заключается их различие?

1. ***Область применения:*** *localStorage* - это хранилище данных, общее для всех страниц в рамках одного домена. Данные, которые сохраняются в *localStorage*, будут доступны на ***всех*** страницах на этом домене.  *sessionStorage* же является хранилищем, которое ограничено текущей *"сессией"* - все данные будут доступны только в ***текущей*** вкладке браузера, пока пользователь не закроет эту вкладку.

2. ***Время жизни данных:*** В *localStorage* данные хранятся ***навсегда***, пока их явно не удалить. В *sessionStorage* данные же существуют только в течение ***текущей сессии*** - в текущей вкладке браузера. Если пользователь закроет вкладку или браузер, данные из *sessionStorage* автоматически удалены.

# Какие существуют основные методы взаимодействия с localStorage и sessionStorage через консоль в браузере?

Существует несколько методов взаимодействия с ***localStorage*** и ***sessionStorage*** через консоль в браузере.

1. Для ***записи*** значения в localStorage и sessionStorage можно использовать следующие методы:

***localStorage.setItem('ключ', 'значение');*** или *localStorage.setItem('key', 'value')*

***sessionStorage.setItem('ключ', 'значение');*** или *sessionStorage.setItem('key', 'value')*

2. Для ***получения*** значения из localStorage и sessionStorage можно использовать следующие методы:

***localStorage.getItem('ключ');*** или *localStorage.getItem('key')*

***sessionStorage.getItem('ключ');*** или *sessionStorage.getItem('key')* 

3. Для ***удаления*** значения из localStorage и sessionStorage можно использовать следующие методы:

***localStorage.removeItem('ключ');*** или *localStorage.removeItem('key')*

***sessionStorage.removeItem('ключ');*** или *sessionStorage.removeItem('key')*

4. Для ***очистки*** значения в localStorage и sessionStorage можно использовать следующие методы:

***localStorage.clear();***

***sessionStorage.clear();***

Кроме того, есть возможность использовать методы консоли браузера для ***добавления/изменения/удаления*** значений в localStorage и sessionStorage. Для этого нужно использовать команду ***console.log('ключ', 'значение')*** для записи значения и команду ***console.clear()*** для очистки консоли.  Например:

*console.log('имя', 'Алексей');*

*console.log('возраст', 25);*

*localStorage.setItem('имя', 'Алексей');*

*localStorage.setItem('возраст', 25);*

*console.log(localStorage.getItem('имя'));*

*console.log(localStorage.getItem('возраст'));*

*localStorage.removeItem('имя');*

*localStorage.clear();*

Например, чтобы ***сохранить*** значение "John" в LocalStorage под ключом "name", нужно в консоли браузера ввести команду ***localStorage.setItem('name', 'John')***. А чтобы ***получить*** это значение обратно, нужно ввести команду ***localStorage.getItem('name')***. Если нужно ***удалить*** значение из хранилища, вводим команду ***localStorage.removeItem('name')***. Чтобы ***очистить*** LocalStorage полностью, вводим команду ***localStorage.clear()***. Для SessionStorage принцип действия аналогичен.

# Что такое IndexedDB?

***IndexedDB*** - это встроенная база данных в браузере, которая позволяет хранить большие объемы структурированных данных и проводить поиск по ним с помощью ***индексов***. Она работает в рамках JavaScript и предоставляет хорошо оптимизированный интерфейс для доступа к данным. ***IndexedDB*** можно использовать для хранения сведений, таких как ***история пользовательских запросов*** или ***информация, введенная пользователем в форме***. Она также может использоваться для создания ***веб-приложений***, которые могут работать в автономном режиме.

*Пример использования IndexedDB может выглядеть следующим образом:* 

веб-приложение, позволяющее пользователю сохранять и просматривать свою коллекцию картинок. Для каждой картинки сохраняются такие данные, как название, описание и файл с картинкой. IndexedDB может использоваться для хранения и индексации этих данных, что позволит пользователям быстро находить нужные им картинки.

## Чем отличается IndexedDB от localStorage и sessionStorage?

***IndexedDB***, ***Local Storage*** и ***Session Storage*** - это три примера технологий хранения данных в браузере, используемых веб-разработчиками. Они все предлагают возможность хранения данных на ***локальном*** компьютере пользователя, но имеют некоторые отличия в использовании и в функциональности.

1. ***Механизм хранения:***
   - *IndexedDB* - это объектная база данных, которая позволяет хранить в браузере данные в структурированном формате. В IndexedDB данные хранятся в БД и их можно обрабатывать как в реляционной базе данных.
   - *localStorage* - это механизм хранения данных в строковом формате в пределах одного домена.
   - *sessionStorage* - это тоже механизм хранения данных на клиенте, но данные хранятся относительно текущей сессии и удаляются после закрытия окна/вкладки.

2. ***Емкость:*** 
   - *IndexedDB* может хранить гораздо больше данных по сравнению с localStorage и sessionStorage.
   - *localStorage* ограничено до 5-10 МБ на домен.
   - *sessionStorage* ограничено до размера сессии.

3. ***Скорость и производительность:***
   - *IndexedDB* может обрабатывать не только текстовые данные, но и бинарные, изображения, музыку и т.д. 
   - *localStorage* и *sessionStorage* медленнее, поскольку данные хранятся в строковом формате.

4. ***Управление данными:***
   - В *IndexedDB* можно использовать запросы и индексирование данных, что позволяет оптимизировать поиск и запросы.
   - *localStorage* и *sessionStorage* предоставляют API только для чтения/записи данных, без возможности индексирования.

В целом, ***IndexedDB*** может быть более сложным в использовании, однако он может быть полезен для проектов, которым необходимы функции хранения больших объемов данных в браузере. ***localStorage*** и ***sessionStorage*** могут использоваться для простых задач, где нужно хранить небольшие объемы данных на клиенте.

# Как можно просмотреть содержимое всех веб-хранилищ в браузере?

Чтобы просмотреть содержимое всех веб-хранилищ в браузере, необходимо выполнить несколько простых шагов (если используется ***Google Chrome***):

1. Открыть браузер ***Google Chrome***
2. Открыть страницу, на которой нужно просмотреть хранилище.
3. Нажать клавишу F12.
4. В DevTools выбрать вкладку "Application", а затем "Storage".
5. Теперь можно увидеть список всех хранилищ для данного сайта.

Также существуют расширения для браузеров, такие как ***Cookies***, которые позволяют быстро просматривать и управлять содержимым веб-хранилищ.