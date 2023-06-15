# Отчёты к запросам
## 1. Получение списка активностей (GET)
1. URL: "https://fakerestapi.azurewebsites.net/api/v1/Activities"
2. Ожидаемый результат: массив с активностями выдаётся
3. Заголовки запроса: 
    - Host - calculated when request is sent
    - User-Agent - PostmanRuntime/7.32.2
    - Accept - * /*
    - Accept-Encoding - gzip, deflate, br
    - Connection - keep-alive
4. Тело запроса: -
5. Заголовки ответа: 
    - Content-Type - application/json; charset=utf-8; v=1.0
    - Date - Wed, 31 May 2023 09:23:28 GMT
    - Server - Kestrel
    - Transfer - chunked
    - api-supported-versions - 1.0
6. Тело ответа: 
    ```{
        "id": 1,
        "title": "Activity 1",
        "dueDate": "2023-05-31T10:23:28.9182816+00:00",
        "completed": false
    },
    {
        "id": 2,
        "title": "Activity 2",
        "dueDate": "2023-05-31T11:23:28.9182841+00:00",
        "completed": true
    },
    {
        "id": 3,
        "title": "Activity 3",
        "dueDate": "2023-05-31T12:23:28.9182844+00:00",
        "completed": false
    },```

## 2. Добавление активности (POST - вариант1)
1. URL: "https://fakerestapi.azurewebsites.net/api/v1/Activities"
2. Ожидаемый результат: добавляется активность
3. Заголовки запроса: 
    - Content-Type - application/json
    - Content-Length - calculated when request is sent
    - Host - calculated when request is sent
    - User-Agent - PostmanRuntime/7.32.2
    - Accept - * /*
    - Accept-Encoding - gzip, deflate, br
    - Connection - keep-alive
4. Тело запроса: 
    ```{

    "id": 2,

    "title": "Новая активность",

     "dueDate": "2023-05-30T05:18:02.847Z",

    "completed": true

    }```
5. Заголовки ответа: 
    - Content-Type - application/json; charset=utf-8; v=1.0
    - Date - Wed, 31 May 2023 09:45:25 GMT
    - Server - Kestrel
    - Transfer-Encoding - chunked
    - api-supported-versions - 1.0
6. Тело ответа:
    ```{
    "id": 2,
    "title": "Новая активность",
    "dueDate": "2023-05-30T05:18:02.847Z",
    "completed": true
    }```

## 3. Добавление активности (POST - вариант2)
1. URL: https://fakerestapi.azurewebsites.net/api/v1/Activities
2. Ожидаемый результат: ошибка 400
3. Заголовки запроса: 
    - Content-Type - application/json
    - Content-Length - calculated when request is sent
    - Host - calculated when request is sent
    - User-Agent - PostmanRuntime/7.32.2
    - Accept - * /*
    - Accept-Encoding - gzip, deflate, br
    - Connection - keep-alive
4. Тело запроса: 
    ```{

    "id": 30,

    "title": "string",

    "dueDate": "2023-05-30T05:18:02.847Z",

    "completed": null

    }```
5. Заголовки ответа: 
    - Content-Type - application/json; charset=utf-8; v=1.0
    - Date - Wed, 31 May 2023 09:45:25 GMT
    - Server - Kestrel
    - Transfer-Encoding - chunked
6. Тело ответа:
    ```{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-8b122650964f844fb9dad8a8a0edcc4f-56576d85856b3b4e-00",
    "errors": {
        "$.completed": [
            "The JSON value could not be converted to System.Boolean. Path: $.completed | LineNumber: 8 | BytePositionInLine: 18."
        ]
    }```

## 4. Добавление активности (POST - вариант3)
1. URL: https://fakerestapi.azurewebsites.net/api/v1/Activities
2. Ожидаемый результат: добавление активности
3. Заголовки запроса: 
    - Content-Type - application/json
    - Content-Length - calculated when request is sent
    - Host - calculated when request is sent
    - User-Agent - PostmanRuntime/7.32.2
    - Accept - * /*
    - Accept-Encoding - gzip, deflate, br
    - Connection - keep-alive
4. Тело запроса: 
    ```{

    "id": 0,

    "title": "null",

    "dueDate": "0001-01-01T00:00:00",

    "completed": false

    }```
5. Заголовки ответа: 
    - Content-Type - application/json; charset=utf-8; v=1.0
    - Date - Wed, 31 May 2023 09:45:25 GMT
    - Server - Kestrel
    - Transfer-Encoding - chunked
    - api-supported-versions - 1.0
6. Тело ответа:
    ```{
    "id": 0,
    "title": "null",
    "dueDate": "0001-01-01T00:00:00",
    "completed": false
    }```

## 5. Добавление активности (POST - вариант4)
1. URL: https://fakerestapi.azurewebsites.net/api/v1/Activities
2. Ожидаемый результат: добавление активности
3. Заголовки запроса: 
    - Content-Type - application/json
    - Content-Length - calculated when request is sent
    - Host - calculated when request is sent
    - User-Agent - PostmanRuntime/7.32.2
    - Accept - * /*
    - Accept-Encoding - gzip, deflate, br
    - Connection - keep-alive
4. Тело запроса: 
    ```{

    "id": 0,

    "title": "0",

    "dueDate": "2023-05-30T05:25:23.478Z",

    "completed": true

    }```
5. Заголовки ответа: 
    - Content-Type - application/json; charset=utf-8; v=1.0
    - Date - Wed, 31 May 2023 09:45:25 GMT
    - Server - Kestrel
    - Transfer-Encoding - chunked
    - api-supported-versions - 1.0
6. Тело ответа:
    ```{
    "id": 0,
    "title": "0",
    "dueDate": "2023-05-30T05:25:23.478Z",
    "completed": true
    }```

## 6. Получение списка активностей по Id (GET - вариант1)
1. URL: https://fakerestapi.azurewebsites.net/api/v1/Activities/2
2. Ожидаемый результат: получение списка активности по Id
3. Заголовки запроса: 
    - Host - calculated when request is sent
    - User-Agent - PostmanRuntime/7.32.2
    - Accept - * /*
    - Accept-Encoding - gzip, deflate, br
    - Connection - keep-alive
4. Тело запроса: -
5. Заголовки ответа: 
    - Content-Type - application/json; charset=utf-8; v=1.0
    - Date - Wed, 31 May 2023 10:08:12 GMT
    - Server - Kestrel
    - Transfer-Encoding - chunked
    - api-supported-versions - 1.0
6. Тело ответа:
    ```{
    "id": 2,
    "title": "Activity 2",
    "dueDate": "2023-05-31T12:08:13.2896411+00:00",
    "completed": true
    }```

## 7. Получение списка активностей по Id (GET - вариант2)
1. URL: https://fakerestapi.azurewebsites.net/api/v1/Activities/31
2. Ожидаемый результат: ошибка 404
3. Заголовки запроса: 
    - Host - calculated when request is sent
    - User-Agent - PostmanRuntime/7.32.2
    - Accept - * /*
    - Accept-Encoding - gzip, deflate, br
    - Connection - keep-alive
4. Тело запроса: -
5. Заголовки ответа: 
    - Content-Type - application/json; charset=utf-8; v=1.0
    - Date - Wed, 31 May 2023 10:08:12 GMT
    - Server - Kestrel
    - Transfer-Encoding - chunked
    - api-supported-versions - 1.0
6. Тело ответа:
    ```{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
    "title": "Not Found",
    "status": 404,
    "traceId": "00-c0b9a04438818445b774fcca9675a624-aaef7a7164b60640-00"
    }```

## 8. Обновление активности (PUT - вариант1)
1. URL: https://fakerestapi.azurewebsites.net/api/v1/Activities/1
2. Ожидаемый результат: обновление активности
3. Заголовки запроса: 
    - Content-Type - application/json
    - Content-Length - calculated when request is sent
    - Host - calculated when request is sent
    - User-Agent - PostmanRuntime/7.32.2
    - Accept - * /*
    - Accept-Encoding - gzip, deflate, br
    - Connection - keep-alive
4. Тело запроса: 
    ```{

    "id": 1,

     "title": "Обновление активности",

    "dueDate": "2023-05-30T05:27:58.598Z",

    "completed": true

    }```
5. Заголовки ответа: 
    - Content-Type - application/json; charset=utf-8; v=1.0
    - Date - Wed, 31 May 2023 10:14:48 GMT
    - Server - Kestrel
    - Transfer-Encoding - chunked
    - api-supported-versions - 1.0
6. Тело ответа:
    ```{
    "id": 1,
    "title": "Обновление активности",
    "dueDate": "2023-05-30T05:27:58.598Z",
    "completed": true
    }```

## 9. Обновление активности (PUT - вариант2)
1. URL: https://fakerestapi.azurewebsites.net/api/v1/Activities/30
2. Ожидаемый результат: обновление активности
3. Заголовки запроса: 
    - Content-Type - application/json
    - Content-Length - calculated when request is sent
    - Host - calculated when request is sent
    - User-Agent - PostmanRuntime/7.32.2
    - Accept - * /*
    - Accept-Encoding - gzip, deflate, br 
    - Connection - keep-alive
4. Тело запроса: 
    ```{

    "title": "string",

    "dueDate": "2023-05-30T05:27:58.598Z",

    "completed": true

    }```
5. Заголовки ответа: 
    - Content-Type - application/json; charset=utf-8; v=1.0
    - Date - Wed, 31 May 2023 10:14:48 GMT
    - Server - Kestrel
    - Transfer-Encoding - chunked
    - api-supported-versions - 1.0
6. Тело ответа:
    ```{
    "id": 0,
    "title": "string",
    "dueDate": "2023-05-30T05:27:58.598Z",
    "completed": true
    }```

## 10. Обновление активности (PUT - вариант3)
1. URL: https://fakerestapi.azurewebsites.net/api/v1/Activities/2
2. Ожидаемый результат: обновление активности
3. Заголовки запроса: 
    - Content-Type - application/json
    - Content-Length - calculated when request is sent
    - Host - calculated when request is sent
    - User-Agent - PostmanRuntime/7.32.2
    - Accept - * /*
    - Accept-Encoding - gzip, deflate, br 
    - Connection - keep-alive
4. Тело запроса: 
    ```{

    "id": 0,

    "title": "null",

    "dueDate": "0001-01-01T00:00:00",

    "completed": false

    }```
5. Заголовки ответа: 
    - Content-Type - application/json; charset=utf-8; v=1.0
    - Date - Wed, 31 May 2023 10:14:48 GMT
    - Server - Kestrel
    - Transfer-Encoding - chunked
    - api-supported-versions - 1.0
6. Тело ответа:
    ```{
    "id": 0,
    "title": "null",
    "dueDate": "0001-01-01T00:00:00",
    "completed": false
    }```

## 11. Обновление активности (PUT - вариант4)
1. URL: https://fakerestapi.azurewebsites.net/api/v1/Activities/30
2. Ожидаемый результат: ошибка 400
3. Заголовки запроса: 
    - Content-Type - application/json
    - Content-Length - calculated when request is sent
    - Host - calculated when request is sent
    - User-Agent - PostmanRuntime/7.32.2
    - Accept - * /*
    - Accept-Encoding - gzip, deflate, br 
    - Connection - keep-alive
4. Тело запроса: 
    ```{

    "id": string,

    "title": "string",

    "dueDate": "dueDate": "2023-05-29T11:33:46.682Z",

    "completed": true

    }```
5. Заголовки ответа: 
    - Content-Type - application/json; charset=utf-8; v=1.0
    - Date - Wed, 31 May 2023 10:14:48 GMT
    - Server - Kestrel
    - Transfer-Encoding - chunked
6. Тело ответа:
    ```{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-6709066ce525d747872d52f622f06da1-1a964ea6096b604b-00",
    "errors": {
        "$.id": [
            "'s' is an invalid start of a value. Path: $.id | LineNumber: 2 | BytePositionInLine: 7."
        ]
    }```

## 12. Удаление активности (DELETE)
1. URL: https://fakerestapi.azurewebsites.net/api/v1/Activities/2
2. Ожидаемый результат: удаление активности
3. Заголовки запроса: 
    - Host - calculated when request is sent
    - User-Agent - PostmanRuntime/7.32.2
    - Accept - * /*
    - Accept-Encoding - gzip, deflate, br
    - Connection - keep-alive
4. Тело запроса: -
5. Заголовки ответа: 
    - Content-Type - 0
    - Date - Wed, 31 May 2023 10:26:45 GMT
    - Server - Kestrel
    - api-supported-versions - 1.0
6. Тело ответа: -

## 13. Получение списка авторов (GET)
1. URL: "https://fakerestapi.azurewebsites.net/api/v1/Authors"
2. Ожидаемый результат: получение списка авторов
3. Заголовки запроса: 
    - Host - calculated when request is sent
    - User-Agent - PostmanRuntime/7.32.2
    - Accept - * /*
    - Accept-Encoding - gzip, deflate, br
    - Connection - keep-alive
4. Тело запроса: -
5. Заголовки ответа: 
    - Content-Type - application/json; charset=utf-8; v=1.0
    - Date - Wed, 31 May 2023 10:29:41 GMT
    - Server - Kestrel
    - Transfer-Encoding - chunked
    - api-supported-versions - 1.0
6. Тело ответа: 
    ```[
    {
        "id": 1,
        "idBook": 1,
        "firstName": "First Name 1",
        "lastName": "Last Name 1"
    },
    {
        "id": 2,
        "idBook": 1,
        "firstName": "First Name 2",
        "lastName": "Last Name 2"
    },
    {
        "id": 3,
        "idBook": 1,
        "firstName": "First Name 3",
        "lastName": "Last Name 3"
    },```

## 14. Добавление автора (POST - вариант1)
1. URL: "https://fakerestapi.azurewebsites.net/api/v1/Autors"
2. Ожидаемый результат: добавляется автор
3. Заголовки запроса: 
    - Content-Type - application/json
    - Content-Length - calculated when request is sent
    - Host - calculated when request is sent
    - User-Agent - PostmanRuntime/7.32.2
    - Accept - * /*
    - Accept-Encoding - gzip, deflate, br
    - Connection - keep-alive
4. Тело запроса: 
    ```{

    "id": 588,

    "idBook": 201,

    "firstName": "Александр",

    "lastName": "Иванов"

    }```
5. Заголовки ответа: 
    - Content-Type - 0
    - Date - Wed, 31 May 2023 10:32:22 GMT
    - Server - Kestrel
    - Transfer-Encoding - chunked
    - api-supported-versions - 1.0
6. Тело ответа:
    ```{

    "id": 588,

    "idBook": 201,

    "firstName": "Александр",

    "lastName": "Иванов"

    }```

## 15. Добавление автора (POST - вариант2)
1. URL: "https://fakerestapi.azurewebsites.net/api/v1/Autors"
2. Ожидаемый результат: добавляется автор
3. Заголовки запроса: 
    - Content-Type - application/json
    - Content-Length - calculated when request is sent
    - Host - calculated when request is sent
    - User-Agent - PostmanRuntime/7.32.2
    - Accept - * /*
    - Accept-Encoding - gzip, deflate, br
    - Connection - keep-alive
4. Тело запроса: 
    ```{

    "firstName": "string",

    "lastName": "string"

    }```
5. Заголовки ответа: 
    - Content-Type - 0
    - Date - Wed, 31 May 2023 10:32:22 GMT
    - Server - Kestrel
    - Transfer-Encoding - chunked
    - api-supported-versions - 1.0
6. Тело ответа:
    ```{

    "firstName": "string",

    "lastName": "string"

    }```

## 16. Добавление автора (POST - вариант3)
1. URL: "https://fakerestapi.azurewebsites.net/api/v1/Autors"
2. Ожидаемый результат: добавляется автор
3. Заголовки запроса: 
    - Content-Type - application/json
    - Content-Length - calculated when request is sent
    - Host - calculated when request is sent
    - User-Agent - PostmanRuntime/7.32.2
    - Accept - * /*
    - Accept-Encoding - gzip, deflate, br
    - Connection - keep-alive
4. Тело запроса: 
    ```{

    "firstName": "null",

    "lastName": "null"

    }```
5. Заголовки ответа: 
    - Content-Type - 0
    - Date - Wed, 31 May 2023 10:32:22 GMT
    - Server - Kestrel
    - Transfer-Encoding - chunked
    - api-supported-versions - 1.0
6. Тело ответа:
    ```{

    "firstName": "null",

    "lastName": "null"

    }```

## 17. Добавление автора (POST - вариант4)
1. URL: "https://fakerestapi.azurewebsites.net/api/v1/Autors"
2. Ожидаемый результат: ошибка 400
3. Заголовки запроса: 
    - Content-Type - application/json
    - Content-Length - calculated when request is sent
    - Host - calculated when request is sent
    - User-Agent - PostmanRuntime/7.32.2
    - Accept - * /*
    - Accept-Encoding - gzip, deflate, br
    - Connection - keep-alive
4. Тело запроса: 
    ```{

    "id": string,

    "idBook": 0,

    "firstName": "string",

    "lastName": "string"

    }```
5. Заголовки ответа: 
    - Content-Type - 0
    - Date - Wed, 31 May 2023 10:32:22 GMT
    - Server - Kestrel
    - Transfer-Encoding - chunked
6. Тело ответа:
    ```{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-8b122650964f844fb9dad8a8a0edcc4f-56576d85856b3b4e-00",
    "errors": {
        "$.completed": [
            "The JSON value could not be converted to System.Boolean. Path: $.completed | LineNumber: 8 | BytePositionInLine: 18."
        ]
    }```

## 18. Получение списка авторов по Id книги (GET - вариант1)
1. URL: https://fakerestapi.azurewebsites.net/api/v1/Authors/books/5
2. Ожидаемый результат: получение списка авторов по Id книги
3. Заголовки запроса: 
    - Host - calculated when request is sent
    - User-Agent - PostmanRuntime/7.32.2
    - Accept - * /*
    - Accept-Encoding - gzip, deflate, br
    - Connection - keep-alive
4. Тело запроса: -
5. Заголовки ответа: 
    - Content-Type - 0 
    - Date - Wed, 31 May 2023 10:48:05 GMT
    - Server - Kestrel
    - Transfer-Encoding - chunked
    - api-supported-versions - 1.0
6. Тело ответа:
    ```{
    "id": 12,
    "idBook": 5,
     "firstName": "First Name 12",
     "lastName": "Last Name 12"
    },
    {
    "id": 13,
    "idBook": 5,
    "firstName": "First Name 13",
    "lastName": "Last Name 13"
    }```

## 19. Получение списка авторов по Id книги (GET - вариант2)
1. URL: https://fakerestapi.azurewebsites.net/api/v1/Authors/books/201
2. Ожидаемый результат: получение списка авторов по Id книги
3. Заголовки запроса: 
    - Host - calculated when request is sent
    - User-Agent - PostmanRuntime/7.32.2
    - Accept - * /*
    - Accept-Encoding - gzip, deflate, br
    - Connection - keep-alive
4. Тело запроса: -
5. Заголовки ответа: 
    - Content-Type - 0
    - Date - Wed, 31 May 2023 10:48:05 GMT
    - Server - Kestrel
    - Transfer-Encoding - chunked
    - api-supported-versions - 1.0
6. Тело ответа:
    ```[]```

## 20. Получение списка авторов по Id (GET - вариант1)
1. URL: https://fakerestapi.azurewebsites.net/api/v1/Authors/599
2. Ожидаемый результат: получение списка авторов по Id
3. Заголовки запроса: 
    - Host - calculated when request is sent
    - User-Agent - PostmanRuntime/7.32.2
    - Accept - * /*
    - Accept-Encoding - gzip, deflate, br
    - Connection - keep-alive
4. Тело запроса: -
5. Заголовки ответа: 
    - Content-Type - 0
    - Date - Wed, 31 May 2023 10:48:05 GMT
    - Server - Kestrel
    - Transfer-Encoding - chunked
    - api-supported-versions - 1.0
6. Тело ответа:
    ```{
    "id": 599,
    "idBook": 198,
    "firstName": "First Name 599",
    "lastName": "Last Name 599"
    }```

## 21. Получение списка авторов по Id (GET - вариант2)
1. URL: https://fakerestapi.azurewebsites.net/api/v1/Authors/606
2. Ожидаемый результат: ошибка 404
3. Заголовки запроса: 
    - Host - calculated when request is sent
    - User-Agent - PostmanRuntime/7.32.2
    - Accept - * /*
    - Accept-Encoding - gzip, deflate, br
    - Connection - keep-alive
4. Тело запроса: -
5. Заголовки ответа: 
    - Content-Type - 0
    - Date - Wed, 31 May 2023 10:48:05 GMT
    - Server - Kestrel
    - Transfer-Encoding - chunked
    - api-supported-versions - 1.0
6. Тело ответа:
    ```{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
    "title": "Not Found",
    "status": 404,
    "traceId": "00-d205b363cdf935459bd64fd949d95823-bd0624cb337a6448-00"
    }```

## 22. Обновление автора (PUT - вариант1)
1. URL: https://fakerestapi.azurewebsites.net/api/v1/Authors/3
2. Ожидаемый результат: обновление автора
3. Заголовки запроса: 
    - Content-Type - application/json
    - Content-Length - calculated when request is sent
    - Host - calculated when request is sent
    - User-Agent - PostmanRuntime/7.32.2
    - Accept - * /*
    - Accept-Encoding - gzip, deflate, br
    - Connection - keep-alive
4. Тело запроса: 
    ```{

    "id": 4,

    "idBook": 4,

    "firstName": "Имя Автора",

    "lastName": "Фамилия Автора"

    }```
5. Заголовки ответа: 
    - Content-Type - application/json; charset=utf-8; v=1.0
    - Date - Wed, 31 May 2023 10:58:29 GMT
    - Server - Kestrel
    - Transfer-Encoding - chunked
    - api-supported-versions - 1.0 
6. Тело ответа:
    ```{
    "id": 4,
    "idBook": 4,
    "firstName": "Имя Автора",
    "lastName": "Фамилия Автора"
    }```

## 23. Обновление автора (PUT - вариант2)
1. URL: https://fakerestapi.azurewebsites.net/api/v1/Authors/20
2. Ожидаемый результат: ошибка 400
3. Заголовки запроса: 
    - Content-Type - application/json
    - Content-Length - calculated when request is sent
    - Host - calculated when request is sent
    - User-Agent - PostmanRuntime/7.32.2
    - Accept - * /*
    - Accept-Encoding - gzip, deflate, br
    - Connection - keep-alive
4. Тело запроса: 
    ```{

    "id": 1,

    "idBook": 1,

    "firstName": "string",

    }```
5. Заголовки ответа: 
    - Content-Type - application/json; charset=utf-8; v=1.0
    - Date - Wed, 31 May 2023 10:58:29 GMT
    - Server - Kestrel
    - Transfer-Encoding - chunked
6. Тело ответа:
    ```{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-74a2ee7192f7754eb990b76e775418c2-e30a8e5f5ff6f341-00",
    "errors": {
        "$": [
            "The JSON object contains a trailing comma at the end which is not supported in this mode. Change the reader options. Path: $ | LineNumber: 8 | BytePositionInLine: 0."
        ]
    }```

## 24. Обновление автора (PUT - вариант3)
1. URL: https://fakerestapi.azurewebsites.net/api/v1/Authors/50
2. Ожидаемый результат: ошибка 400
3. Заголовки запроса: 
    - Content-Type - application/json
    - Content-Length - calculated when request is sent
    - Host - calculated when request is sent
    - User-Agent - PostmanRuntime/7.32.2
    - Accept - * /*
    - Accept-Encoding - gzip, deflate, br
    - Connection - keep-alive
4. Тело запроса: 
    ```{

    "id": ,

    "idBook": ,

    "firstName": " ",

    "lastName": " "

    }```
5. Заголовки ответа: 
    - Content-Type - application/json; charset=utf-8; v=1.0
    - Date - Wed, 31 May 2023 10:58:29 GMT
    - Server - Kestrel
    - Transfer-Encoding - chunked
6. Тело ответа:
    ```{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-117cb78bdae9fd4b83eb4ea312ac2870-35ea173892920f4a-00",
    "errors": {
        "$.id": [
            "',' is an invalid start of a value. Path: $.id | LineNumber: 2 | BytePositionInLine: 7."
        ]
    }```

## 25. Обновление автора (PUT - вариант4)
1. URL: https://fakerestapi.azurewebsites.net/api/v1/Authors/50
2. Ожидаемый результат: обновление автора
3. Заголовки запроса: 
    - Content-Type - application/json
    - Content-Length - calculated when request is sent
    - Host - calculated when request is sent
    - User-Agent - PostmanRuntime/7.32.2
    - Accept - * /*
    - Accept-Encoding - gzip, deflate, br
    - Connection - keep-alive
4. Тело запроса: 
    ```{

    "id": 0,

    "idBook": 0,

    "firstName": "null",

    "lastName": "0"

    }```
5. Заголовки ответа: 
    - Content-Type
    - Date
    - Server
    - Transfer-Encoding
    - api-supported-versions
6. Тело ответа:
    ```{
    "id": 0,
    "idBook": 0,
    "firstName": "null",
    "lastName": "0"
    }```

## 26. Удаление автора (DELETE)
1. URL: https://fakerestapi.azurewebsites.net/api/v1/Authors/700
2. Ожидаемый результат: удаление автора
3. Заголовки запроса: 
    - Host - calculated when request is sent
    - User-Agent - PostmanRuntime/7.32.2
    - Accept - * /*
    - Accept-Encoding - gzip, deflate, br
    - Connection - keep-alive
4. Тело запроса: -
5. Заголовки ответа: 
    - Content-Type - 0
    - Date - Wed, 31 May 2023 14:38:40 GMT
    - Server - Kestrel
    - api-supported-versions - 1.0
6. Тело ответа: -

## 27. Получение списка книг (GET)
1. URL: https://fakerestapi.azurewebsites.net/api/v1/Books
2. Ожидаемый результат: получение списка книг
3. Заголовки запроса: 
    - Host - calculated when request is sent
    - User-Agent - PostmanRuntime/7.32.2
    - Accept - * /*
    - Accept-Encoding - gzip, deflate, br
    - Connection - keep-alive
4. Тело запроса: -
5. Заголовки ответа: 
    - Content-Type - application/json; charset=utf-8; v=1.0
    - Date - Wed, 31 May 2023 11:09:30 GMT
    - Server - Kestrel
    - Transfer-Encoding - chunked
    - api-supported-versions - 1.0
6. Тело ответа: 
    ```[
    {
        "id": 1,
        "title": "Book 1",
        "description": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
        "pageCount": 100,
        "excerpt": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
        "publishDate": "2023-05-30T11:09:30.316329+00:00"
    },
    {
        "id": 2,
        "title": "Book 2",
        "description": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
        "pageCount": 200,
        "excerpt": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
        "publishDate": "2023-05-29T11:09:30.3163697+00:00"
    },```

## 28. Добавление книги (POST - вариант1)
1. URL: https://fakerestapi.azurewebsites.net/api/v1/Books
2. Ожидаемый результат: добавляется книга
3. Заголовки запроса: 
    - Content-Type - application/json
    - Content-Length - calculated when request is sent
    - Host - calculated when request is sent
    - User-Agent - PostmanRuntime/7.32.2
    - Accept - * /*
    - Accept-Encoding - gzip, deflate, br
    - Connection - keep-alive
4. Тело запроса: 
    ```{

    "id": 201,

    "title": "Заголовок",

    "description": "Описание",

    "pageCount": 10,

    "excerpt": "Эксперт",

    "publishDate": "2023-05-30T05:45:02.71Z"

    }```
5. Заголовки ответа: 
    - Content-Type - application/json; charset=utf-8; v=1.0
    - Date - Wed, 31 May 2023 11:11:35 GMT
    - Server - Kestrel
    - Transfer-Encoding - chunked
    - api-supported-versions - 1.0
6. Тело ответа:
    ```{
    "id": 201,
    "title": "Заголовок",
    "description": "Описание",
    "pageCount": 10,
    "excerpt": "Эксперт",
    "publishDate": "2023-05-30T05:45:02.71Z"
    }```

## 29. Добавление книги (POST - вариант2)
1. URL: https://fakerestapi.azurewebsites.net/api/v1/Books
2. Ожидаемый результат: ошибка 400
3. Заголовки запроса: 
    - Content-Type - application/json
    - Content-Length - calculated when request is sent
    - Host - calculated when request is sent
    - User-Agent - PostmanRuntime/7.32.2
    - Accept - * /*
    - Accept-Encoding - gzip, deflate, br
    - Connection - keep-alive
4. Тело запроса: 
    ```{

    "id": 201,

    "title": "Заголовок",

    "description": "Описание",

    "pageCount": 10,

    "excerpt": "Эксперт",

    "publishDate": "2023-05-30T05"

    }```
5. Заголовки ответа: 
    - Content-Type - application/json; charset=utf-8; v=1.0
    - Date - Wed, 31 May 2023 11:11:35 GMT
    - Server - Kestrel
    - Transfer-Encoding - chunked
6. Тело ответа:
    ```{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-5f7e84b34b585742beaa3e88ecd1f956-3ceda2ebaa199c43-00",
    "errors": {
        "$.publishDate": [
            "The JSON value could not be converted to System.DateTime. Path: $.publishDate | LineNumber: 12 | BytePositionInLine: 31."
        ]
    }```

## 30. Добавление книги (POST - вариант3)
1. URL: https://fakerestapi.azurewebsites.net/api/v1/Books
2. Ожидаемый результат: добавление книги
3. Заголовки запроса: 
    - Content-Type - application/json
    - Content-Length - calculated when request is sent
    - Host - calculated when request is sent
    - User-Agent - PostmanRuntime/7.32.2
    - Accept - * /*
    - Accept-Encoding - gzip, deflate, br
    - Connection - keep-alive
4. Тело запроса: 
    ```{

    "id": 0,

    "title": "null",

    "description": "null",

    "pageCount": 0,

    "excerpt": "null",

    "publishDate": "0001-01-01T00:00:00"

    }```
5. Заголовки ответа: 
    - Content-Type - application/json; charset=utf-8; v=1.0
    - Date - Wed, 31 May 2023 11:11:35 GMT
    - Server - Kestrel
    - Transfer-Encoding - chunked
    - api-supported-versions - 1.0
6. Тело ответа:
    ```{
    "id": 0,
    "title": "null",
    "description": "null",
    "pageCount": 0,
    "excerpt": "null",
    "publishDate": "0001-01-01T00:00:00"
    }```

## 31. Добавление книги (POST - вариант4)
1. URL: https://fakerestapi.azurewebsites.net/api/v1/Books
2. Ожидаемый результат: добавление книги
3. Заголовки запроса: 
    - Content-Type- application/json
    - Content-Length - calculated when request is sent
    - Host - calculated when request is sent
    - User-Agent - PostmanRuntime/7.32.2
    - Accept - * /*
    - Accept-Encoding - gzip, deflate, br
    - Connection - keep-alive
4. Тело запроса: 
    ```{

    "id": -1,

    "title": "string",

    "description": "string",

    "pageCount": -1,

    "excerpt": "string",

    "publishDate": "2023-05-30T05:51:25.399Z"

    }```
5. Заголовки ответа: 
    - Content-Type - application/json; charset=utf-8; v=1.0
    - Date - Wed, 31 May 2023 11:11:35 GMT
    - Server - Kestrel
    - Transfer-Encoding - chunked
    - api-supported-versions - 1.0
6. Тело ответа:
    ```{
    "id": -1,
    "title": "string",
    "description": "string",
    "pageCount": -1,
    "excerpt": "string",
    "publishDate": "2023-05-30T05:51:25.399Z"
    }```

## 32. Получение списка книг по Id (GET - вариант1)
1. URL: https://fakerestapi.azurewebsites.net/api/v1/Books/200
2. Ожидаемый результат: получение списка книг по Id
3. Заголовки запроса: 
    - Host - calculated when request is sent
    - User-Agent - PostmanRuntime/7.32.2
    - Accept - * /*
    - Accept-Encoding - gzip, deflate, br
    - Connection - keep-alive
4. Тело запроса: -
5. Заголовки ответа: 
    - Content-Type - application/json; charset=utf-8; v=1.0
    - Date - Wed, 31 May 2023 11:11:35 GMT
    - Server - Kestrel
    - Transfer-Encoding - chunked
    - api-supported-versions - 1.0
6. Тело ответа:
    ```{
    "id": 200,
    "title": "Book 200",
    "description": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
    "pageCount": 20000,
    "excerpt": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
    "publishDate": "2022-11-12T11:21:08.448829+00:00"
    }```

## 33. Получение списка книг по Id (GET - вариант2)
1. URL: https://fakerestapi.azurewebsites.net/api/v1/Books/201
2. Ожидаемый результат: ошибка 404
3. Заголовки запроса: 
    - Host - calculated when request is sent
    - User-Agent - PostmanRuntime/7.32.2
    - Accept - * /*
    - Accept-Encoding - gzip, deflate, br
    - Connection - keep-alive
4. Тело запроса: -
5. Заголовки ответа: 
    - Content-Type - application/json; charset=utf-8; v=1.0
    - Date - Wed, 31 May 2023 11:11:35 GMT
    - Server - Kestrel
    - Transfer-Encoding - chunked
6. Тело ответа:
    ```{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
    "title": "Not Found",
    "status": 404,
    "traceId": "00-ebdc56029c1a4d40ad48c6edd02d9b32-375e44e687aa0f45-00"
}   ```

## 34. Обновление книги (PUT - вариант1)
1. URL: https://fakerestapi.azurewebsites.net/api/v1/Books/200
2. Ожидаемый результат: обновление книги
3. Заголовки запроса: 
    - Content-Type - application/json
    - Content-Length - calculated when request is sent
    - Host - calculated when request is sent
    - User-Agent - PostmanRuntime/7.32.2
    - Accept - * /*
    - Accept-Encoding - gzip, deflate, br
    - Connection - keep-alive
4. Тело запроса: 
    ```{

    "id": 200,

    "title": "string",

    "description": "string",

    "pageCount": 10,

    "excerpt": "string",

    "publishDate": "2023-05-30T05:52:40.003Z"

    }```
5. Заголовки ответа: 
    - Content-Type - application/json; charset=utf-8; v=1.0
    - Date - Wed, 31 May 2023 11:24:39 GMT
    - Server - Kestrel
    - Transfer-Encoding - chunked
    - api-supported-versions - 1.0
6. Тело ответа: 
    ```{
    "id": 200,
    "title": "string",
    "description": "string",
    "pageCount": 10,
    "excerpt": "string",
    "publishDate": "2023-05-30T05:52:40.003Z"
    }```

## 35. Обновление книги (PUT - вариант2)
1. URL: https://fakerestapi.azurewebsites.net/api/v1/Books/200
2. Ожидаемый результат: ошибка 400
3. Заголовки запроса: 
    - Content-Type - application/json
    - Content-Length - calculated when request is sent
    - Host - calculated when request is sent
    - User-Agent - PostmanRuntime/7.32.2
    - Accept - * /*
    - Accept-Encoding - gzip, deflate, br
    - Connection - keep-alive
4. Тело запроса: 
    ```{

    "id": 0,

    "title": "string",

    "description": "string",

    "pageCount": 0,

    "excerpt": "string",

    }```
5. Заголовки ответа: 
    - Content-Type - application/json; charset=utf-8; v=1.0
    - Date - Wed, 31 May 2023 11:24:39 GMT
    - Server - Kestrel
    - Transfer-Encoding - chunked
6. Тело ответа: 
    ```{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-528263de76659d4cbf9191722ed7d277-6f02452c32a1e848-00",
    "errors": {
        "$": [
            "The JSON object contains a trailing comma at the end which is not supported in this mode. Change the reader options. Path: $ | LineNumber: 12 | BytePositionInLine: 0."
        ]
    }```

## 36. Обновление книги (PUT - вариант3)
1. URL: https://fakerestapi.azurewebsites.net/api/v1/Books/200
2. Ожидаемый результат: обновление книги
3. Заголовки запроса: 
    - Content-Type - application/json
    - Content-Length - calculated when request is sent
    - Host - calculated when request is sent
    - User-Agent - PostmanRuntime/7.32.2
    - Accept - * /*
    - Accept-Encoding - gzip, deflate, br
    - Connection - keep-alive
4. Тело запроса: 
    ```{

    "id": 0,

    "title": "null",

    "description": "null",

    "pageCount": 0,

    "excerpt": "null",

    "publishDate": "0001-01-01T00:00:00"

    }```
5. Заголовки ответа: 
    - Content-Type - application/json; charset=utf-8; v=1.0
    - Date - Wed, 31 May 2023 11:24:39 GMT
    - Server - Kestrel
    - Transfer-Encoding - chunked
    - api-supported-versions - 1.0
6. Тело ответа: 
    ```{
    "id": 0,
    "title": "null",
    "description": "null",
    "pageCount": 0,
    "excerpt": "null",
    "publishDate": "0001-01-01T00:00:00"
    }```

## 37. Обновление книги (PUT - вариант4)
1. URL: https://fakerestapi.azurewebsites.net/api/v1/Books/200
2. Ожидаемый результат: обновление книги
3. Заголовки запроса: 
    - Content-Type - application/json
    - Content-Length - calculated when request is sent
    - Host - calculated when request is sent
    - User-Agent - PostmanRuntime/7.32.2
    - Accept - * /*
    - Accept-Encoding - gzip, deflate, br
    - Connection - keep-alive
4. Тело запроса: 
    ```{

    "id": 0,

    "title": "null",

    "description": "null",

    "pageCount": 0,

    "excerpt": "0",

    "publishDate": "2023-05-30T05:55:48.663Z"

    }```
5. Заголовки ответа: 
    - Content-Type - application/json; charset=utf-8; v=1.0
    - Date - Wed, 31 May 2023 11:24:39 GMT
    - Server - Kestrel
    - Transfer-Encoding - chunked
    - api-supported-versions - 1.0
6. Тело ответа: 
    ```{
    "id": 0,
    "title": "null",
    "description": "null",
    "pageCount": 0,
    "excerpt": "0",
    "publishDate": "2023-05-30T05:55:48.663Z"
    }```

## 38. Удаление книги (DELETE)
1. URL: https://fakerestapi.azurewebsites.net/api/v1/Activities/201
2. Ожидаемый результат: удаление книги
3. Заголовки запроса: 
    - Host - calculated when request is sent
    - User-Agent - PostmanRuntime/7.32.2
    - Accept - * /*
    - Accept-Encoding - gzip, deflate, br
    - Connection - keep-alive
4. Тело запроса: -
5. Заголовки ответа: 
    - Content-Type - application/json; charset=utf-8; v=1.0
    - Date - Wed, 31 May 2023 15:11:45 GMT
    - Server - Kestrel
    - api-supported-versions - 1.0
6. Тело ответа: -

## 39. Получение списка фотографий обложки (GET)
1. URL: https://fakerestapi.azurewebsites.net/api/v1/Books
2. Ожидаемый результат: получение списка фотографий обложки
3. Заголовки запроса: 
    - Host - calculated when request is sent
    - User-Agent - PostmanRuntime/7.32.2
    - Accept - * /*
    - Accept-Encoding - gzip, deflate, br
    - Connection - keep-alive
4. Тело запроса: -
5. Заголовки ответа: 
    - Content-Type - application/json; charset=utf-8; v=1.0
    - Date - Wed, 31 May 2023 11:35:36 GMT
    - Server - Kestrel
    - Transfer-Encoding - chunked
    - api-supported-versions - 1.0
6. Тело ответа: 
    ```[
    {
        "id": 1,
        "idBook": 1,
        "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"
    },
    {
        "id": 2,
        "idBook": 2,
        "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 2&w=250&h=350"
    },
    {
        "id": 3,
        "idBook": 3,
        "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 3&w=250&h=350"
    },```

## 40. Добавление фотографии обложки (POST - вариант1)
1. URL: https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos
2. Ожидаемый результат: добавляется фотография обложки
3. Заголовки запроса: 
    - Content-Type - application/json
    - Content-Length - calculated when request is sent
    - Host - calculated when request is sent
    - User-Agent - PostmanRuntime/7.32.2
    - Accept - * /*
    - Accept-Encoding - gzip, deflate, br
    - Connection - keep-alive
4. Тело запроса: 
    ```{

    "id": 201,

    "idBook": 201,

    "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 200&w=250&h=400"

    }```
5. Заголовки ответа: 
    - Content-Type - application/json; charset=utf-8; v=1.0
    - Date - Wed, 31 May 2023 11:37:13 GMT
    - Server - Kestrel
    - Transfer-Encoding - chunked
    - api-supported-versions - 1.0 
6. Тело ответа:
    ```{
    "id": 201,
    "idBook": 201,
    "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 200&w=250&h=400"
    }```

## 41. Добавление фотографии обложки (POST - вариант2)
1. URL: https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos
2. Ожидаемый результат: ошибка 400
3. Заголовки запроса: 
    - Content-Type - application/json
    - Content-Length - calculated when request is sent
    - Host - calculated when request is sent
    - User-Agent - PostmanRuntime/7.32.2
    - Accept - * /*
    - Accept-Encoding - gzip, deflate, br
    - Connection - keep-alive
4. Тело запроса: 
    ```{

    "id": 3,

    "idBook": 3,

    }```
5. Заголовки ответа: 
    - Content-Type - application/json; charset=utf-8; v=1.0
    - Date - Wed, 31 May 2023 11:37:13 GMT
    - Server - Kestrel
    - Transfer-Encoding - chunked
6. Тело ответа:
    ```{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-4592549b028fa6438848af26f0d6f390-b8fa27f4aeb73846-00",
    "errors": {
        "$": [
            "The JSON object contains a trailing comma at the end which is not supported in this mode. Change the reader options. Path: $ | LineNumber: 6 | BytePositionInLine: 0."
        ]
    }```

## 42. Добавление фотографии обложки (POST - вариант3)
1. URL: https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos
2. Ожидаемый результат: добавляется фотография обложки
3. Заголовки запроса: 
    - Content-Type - application/json
    - Content-Length - calculated when request is sent
    - Host - calculated when request is sent
    - User-Agent - PostmanRuntime/7.32.2
    - Accept - * /*
    - Accept-Encoding - gzip, deflate, br
    - Connection - keep-alive
4. Тело запроса: 
    ```{

    "id": 0,

    "idBook": 0,

    "url": "null"

    }```
5. Заголовки ответа: 
    - Content-Type - application/json; charset=utf-8; v=1.0
    - Date - Wed, 31 May 2023 11:37:13 GMT
    - Server - Kestrel
    - Transfer-Encoding - chunked
    - api-supported-versions - 1.0
6. Тело ответа:
    ```{
    "id": 0,
    "idBook": 0,
    "url": "null"
    }```

## 43. Добавление фотографии обложки (POST - вариант4)
1. URL: https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos
2. Ожидаемый результат: добавляется фотография обложки
3. Заголовки запроса: 
    - Content-Type - application/json
    - Content-Length - calculated when request is sent
    - Host - calculated when request is sent
    - User-Agent - PostmanRuntime/7.32.2
    - Accept - * /*
    - Accept-Encoding - gzip, deflate, br
    - Connection - keep-alive
4. Тело запроса: 
    ```{

    "id": 0,

    "idBook": 0,

    "url": "0"

    }```
5. Заголовки ответа: 
    - Content-Type - application/json; charset=utf-8; v=1.0
    - Date - Wed, 31 May 2023 11:37:13 GMT
    - Server - Kestrel
    - Transfer-Encoding - chunked
    - api-supported-versions - 1.0
6. Тело ответа: 
    ```{

    "id": 0,

    "idBook": 0,

    "url": "0"

    }```

## 44. Получение списка фотографий обложки по Id книги (GET - вариант1)
1. URL: https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/books/covers/200
2. Ожидаемый результат: получение списка фотографий обложки по Id книги
3. Заголовки запроса: 
    - Host - calculated when request is sent
    - User-Agent - PostmanRuntime/7.32.2
    - Accept - * /*
    - Accept-Encoding - gzip, deflate, br
    - Connection - keep-alive
4. Тело запроса: -
5. Заголовки ответа: 
    - Content-Type - application/json; charset=utf-8; v=1.0
    - Date - Wed, 31 May 2023 11:47:36 GMT
    - Server - Kestrel
    - Transfer-Encoding - chunked
    - api-supported-versions - 1.0 
6. Тело ответа:
    ```[
    {
        "id": 200,
        "idBook": 200,
        "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 200&w=250&h=350"
    }
    ]```

## 45. Получение списка фотографий обложки по Id книги (GET - вариант2)
1. URL: https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/books/covers/201
2. Ожидаемый результат: получение списка фотографий обложки по Id книги
3. Заголовки запроса: 
    - Host - calculated when request is sent
    - User-Agent - PostmanRuntime/7.32.2
    - Accept - * /*
    - Accept-Encoding - gzip, deflate, br
    - Connection - keep-alive
4. Тело запроса: -
5. Заголовки ответа: 
    - Content-Type - application/json; charset=utf-8; v=1.0
    - Date - Wed, 31 May 2023 11:47:36 GMT
    - Server - Kestrel
    - Transfer-Encoding - chunked
    - api-supported-versions - 1.0
6. Тело ответа:
    ```[]```

## 46. Получение списка фотографий обложки по Id (GET - вариант1)
1. URL: https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/200
2. Ожидаемый результат: получение списка фотографий обложки по Id
3. Заголовки запроса: 
    - Host - calculated when request is sent
    - User-Agent - PostmanRuntime/7.32.2
    - Accept - * /*
    - Accept-Encoding - gzip, deflate, br
    - Connection - keep-alive
4. Тело запроса: -
5. Заголовки ответа: 
    - Content-Type - application/json; charset=utf-8; v=1.0
    - Date - Wed, 31 May 2023 11:47:36 GMT
    - Server - Kestrel
    - Transfer-Encoding - chunked
    - api-supported-versions - 1.0
6. Тело ответа:
    ```{
    "id": 200,
    "idBook": 200,
    "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 200&w=250&h=350"
    }```

## 47. Получение списка фотографий обложки по Id (GET - вариант2)
1. URL: https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/201
2. Ожидаемый результат: ошибка 404
3. Заголовки запроса: 
    - Host - calculated when request is sent
    - User-Agent - PostmanRuntime/7.32.2
    - Accept - * /*
    - Accept-Encoding - gzip, deflate, br
    - Connection - keep-alive
4. Тело запроса: -
5. Заголовки ответа: 
    - Content-Type - application/json; charset=utf-8; v=1.0
    - Date - Wed, 31 May 2023 11:47:36 GMT
    - Server - Kestrel
    - Transfer-Encoding - chunked
6. Тело ответа:
    ```{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
  "title": "Not Found",
  "status": 404,
  "traceId": "00-200f79011a657347abbbac98e58c5c03-e60c8438b02bc945-00"
    }```

## 48. Обновление фотографии обложки (PUT - вариант1)
1. URL: https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/201
2. Ожидаемый результат: обновление фотографии обложки
3. Заголовки запроса: 
    - Content-Type - application/json
    - Content-Length - calculated when request is sent
    - Host - calculated when request is sent
    - User-Agent - PostmanRuntime/7.32.2
    - Accept - * /*
    - Accept-Encoding - gzip, deflate, br
    - Connection - keep-alive
4. Тело запроса: 
    ```{

    "id": 2,

    "idBook": 2,

    "url": "string"

    }```
5. Заголовки ответа: 
    - Content-Type - application/json; charset=utf-8; v=1.0
    - Date - Wed, 31 May 2023 11:51:36 GMT
    - Server - Kestrel
    - Transfer-Encoding - chunked
    - api-supported-versions - 1.0
6. Тело ответа: 
    ```{
    "id": 2,
    "idBook": 2,
    "url": "string"
    }```

## 49. Обновление фотографии обложки (PUT - вариант2)
1. URL: https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/10
2. Ожидаемый результат: обновление фотографии обложки
3. Заголовки запроса: 
    - Content-Type - application/json
    - Content-Length - calculated when request is sent
    - Host - calculated when request is sent
    - User-Agent - PostmanRuntime/7.32.2
    - Accept - * /*
    - Accept-Encoding - gzip, deflate, br
    - Connection - keep-alive
4. Тело запроса: 
    ```{

     "idBook": 0,

    "url": "string"

    }```
5. Заголовки ответа: 
    - Content-Type - application/json; charset=utf-8; v=1.0
    - Date - Wed, 31 May 2023 11:51:36 GMT
    - Server - Kestrel
    - Transfer-Encoding - chunked
    - api-supported-versions - 1.0
6. Тело ответа: 
    ```{
    "id": 0,
    "idBook": 0,
    "url": "string"
    }```

## 50. Обновление фотографии обложки (PUT - вариант3)
1. URL: https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/10
2. Ожидаемый результат: обновление фотографии обложки
3. Заголовки запроса: 
    - Content-Type - application/json
    - Content-Length - calculated when request is sent
    - Host - calculated when request is sent
    - User-Agent - PostmanRuntime/7.32.2
    - Accept - * /*
    - Accept-Encoding - gzip, deflate, br
    - Connection - keep-alive
4. Тело запроса: 
    ```{

    "id": 0,

    "idBook": 0,

    "url": "null"

    }```
5. Заголовки ответа: 
    - Content-Type - application/json; charset=utf-8; v=1.0
    - Date - Wed, 31 May 2023 11:51:36 GMT
    - Server - Kestrel
    - Transfer-Encoding - chunked
    - api-supported-versions - 1.0
6. Тело ответа: 
    ```{
    "id": 0,
    "idBook": 0,
    "url": "null"
    }```

## 51. Обновление фотографии обложки (PUT - вариант4)
1. URL: https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/200
2. Ожидаемый результат: ошибка 400
3. Заголовки запроса: 
    - Content-Type - application/json
    - Content-Length - calculated when request is sent
    - Host - calculated when request is sent
    - User-Agent - PostmanRuntime/7.32.2
    - Accept - * /*
    - Accept-Encoding - gzip, deflate, br
    - Connection - keep-alive
4. Тело запроса: 
    ```{

    "id": 0,

    "idBook": string,

    "url": "null"

    }```
5. Заголовки ответа: 
    - Content-Type - application/json; charset=utf-8; v=1.0
    - Date - Wed, 31 May 2023 11:51:36 GMT
    - Server - Kestrel
    - Transfer-Encoding - chunked
6. Тело ответа: 
    ```{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-5996207a58fb3f4c8c5358963944ac23-63af08d4651cb14b-00",
    "errors": {
        "$.idBook": [
            "'s' is an invalid start of a value. Path: $.idBook | LineNumber: 4 | BytePositionInLine: 11."
        ]
    }```

## 52. Удаление фотографии обложки (DELETE)
1. URL: https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/201
2. Ожидаемый результат: удаление книги
3. Заголовки запроса: 
    - Host - calculated when request is sent
    - User-Agent - PostmanRuntime/7.32.2
    - Accept - * /*
    - Accept-Encoding - gzip, deflate, br
    - Connection - keep-alive
4. Тело запроса: -
5. Заголовки ответа: 
    - Content-Type - application/json; charset=utf-8; v=1.0
    - Date - Wed, 31 May 2023 11:59:30 GMT
    - Server - Kestrel
    - api-supported-versions - 1.0
6. Тело ответа: -

## 53. Получение списка пользователей (GET)
1. URL: https://fakerestapi.azurewebsites.net/api/v1/Users
2. Ожидаемый результат: получение списка пользователей
3. Заголовки запроса: 
    - Host - calculated when request is sent
    - User-Agent - PostmanRuntime/7.32.2
    - Accept - * /*
    - Accept-Encoding - gzip, deflate, br
    - Connection - keep-alive
4. Тело запроса: -
5. Заголовки ответа: 
    - Content-Type - application/json; charset=utf-8; v=1.0
    - Date - Wed, 31 May 2023 12:01:54 GMT
    - Server - Kestrel
    - Transfer-Encoding - chunked
    - api-supported-versions - 1.0
6. Тело ответа: 
    ```[
    {
        "id": 1,
        "userName": "User 1",
        "password": "Password1"
    },
    {
        "id": 2,
        "userName": "User 2",
        "password": "Password2"
    },
    {
        "id": 3,
        "userName": "User 3",
        "password": "Password3"
    },```

## 54. Добавление пользователя (POST - вариант1)
1. URL: https://fakerestapi.azurewebsites.net/api/v1/Users
2. Ожидаемый результат: добавляется пользователь
3. Заголовки запроса: 
    - Content-Type - application/json
    - Content-Length - calculated when request is sent
    - Host - calculated when request is sent
    - User-Agent - PostmanRuntime/7.32.2
    - Accept - * /*
    - Accept-Encoding - gzip, deflate, br
    - Connection - keep-alive
4. Тело запроса: 
    ```{

    "id": 11,

    "userName": "Имя",

    "password": "Пароль"

    }```
5. Заголовки ответа: 
    - Content-Type - application/json; charset=utf-8; v=1.0
    - Date - Wed, 31 May 2023 12:04:24 GMT
    - Server - Kestrel
    - Transfer-Encoding - chunked
    - api-supported-versions - 1.0
6. Тело ответа:
    ```{
    "id": 11,
    "userName": "Имя",
    "password": "Пароль"
    }```

## 55. Добавление пользователя (POST - вариант2)
1. URL: https://fakerestapi.azurewebsites.net/api/v1/Users
2. Ожидаемый результат: добавляется пользователь
3. Заголовки запроса: 
    - Content-Type - application/json
    - Content-Length - calculated when request is sent
    - Host - calculated when request is sent
    - User-Agent - PostmanRuntime/7.32.2
    - Accept - * /*
    - Accept-Encoding - gzip, deflate, br
    - Connection - keep-alive
4. Тело запроса: 
    ```{

    "userName": "Имя",

     "password": "Пароль"

    }```
5. Заголовки ответа: 
    - Content-Type - application/json; charset=utf-8; v=1.0
    - Date - Wed, 31 May 2023 12:04:24 GMT
    - Server - Kestrel
    - Transfer-Encoding - chunked
    - api-supported-versions - 1.0
6. Тело ответа:
    ```{
    "id": 0,
    "userName": "Имя",
    "password": "Пароль"
    }```

## 56. Добавление пользователя (POST - вариант3)
1. URL: https://fakerestapi.azurewebsites.net/api/v1/Users
2. Ожидаемый результат: добавляется пользователь
3. Заголовки запроса: 
    - Content-Type - application/json
    - Content-Length - calculated when request is sent
    - Host - calculated when request is sent
    - User-Agent - PostmanRuntime/7.32.2
    - Accept - * /*
    - Accept-Encoding - gzip, deflate, br
    - Connection - keep-alive
4. Тело запроса: 
    ```{

    "id": 0,

     "userName": "null",

     "password": "null"

    }```
5. Заголовки ответа: 
    - Content-Type - application/json; charset=utf-8; v=1.0
    - Date - Wed, 31 May 2023 12:04:24 GMT
    - Server - Kestrel
    - Transfer-Encoding - chunked
    - api-supported-versions - 1.0 
6. Тело ответа:
    ```{
    "id": 0,
    "userName": "null",
    "password": "null"
    }```

## 57. Добавление пользователя (POST - вариант4)
1. URL: https://fakerestapi.azurewebsites.net/api/v1/Users
2. Ожидаемый результат: ошибка 400
3. Заголовки запроса: 
    - Content-Type - application/json
    - Content-Length - calculated when request is sent
    - Host - calculated when request is sent
    - User-Agent - PostmanRuntime/7.32.2
    - Accept - * /*
    - Accept-Encoding - gzip, deflate, br
    - Connection - keep-alive
4. Тело запроса: 
    ```{

    "id": string,

    "userName": "string",

    "password": "string"

    }```
5. Заголовки ответа: 
    - Content-Type - application/json; charset=utf-8; v=1.0
    - Date - Wed, 31 May 2023 12:04:24 GMT
    - Server - Kestrel
    - Transfer-Encoding - chunked
6. Тело ответа:
    ```{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-d5c622a18925af43b8f5106656a3b1c9-5227deb8213de641-00",
    "errors": {
        "$.id": [
            "'s' is an invalid start of a value. Path: $.id | LineNumber: 2 | BytePositionInLine: 7."
        ]
    }```

## 58. Получение списка пользователей по Id (GET - вариант1)
1. URL: https://fakerestapi.azurewebsites.net/api/v1/Users/10
2. Ожидаемый результат: получение списка пользователей по Id
3. Заголовки запроса: 
    - Host - calculated when request is sent
    - User-Agent - PostmanRuntime/7.32.2
    - Accept - * /*
    - Accept-Encoding - gzip, deflate, br
    - Connection - keep-alive
4. Тело запроса: -
5. Заголовки ответа: 
    - Content-Type - application/json; charset=utf-8; v=1.0
    - Date - Wed, 31 May 2023 12:18:34 GMT
    - Server - Kestrel
    - Transfer-Encoding - chunked
    - api-supported-versions - 1.0
6. Тело ответа:
    ```{
    "id": 10,
    "userName": "User 10",
    "password": "Password10"
    }```

## 59. Получение списка пользователей по Id (GET - вариант2)
1. URL: https://fakerestapi.azurewebsites.net/api/v1/Users/11
2. Ожидаемый результат: ошибка 404
3. Заголовки запроса: 
    - Host - calculated when request is sent
    - User-Agent - PostmanRuntime/7.32.2
    - Accept - * /*
    - Accept-Encoding - gzip, deflate, br
    - Connection - keep-alive
4. Тело запроса: -
5. Заголовки ответа: 
    - Content-Type - application/json; charset=utf-8; v=1.0
    - Date - Wed, 31 May 2023 12:18:34 GMT
    - Server - Kestrel
    - Transfer-Encoding - chunked
6. Тело ответа:
    ```{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
    "title": "Not Found",
    "status": 404,
    "traceId": "00-e70db5ffb6931d42bd7c10f4b1f30a53-73a64f0d0ccb8d4b-00"
    }```

## 60. Обновление пользователя (PUT - вариант1)
1. URL: https://fakerestapi.azurewebsites.net/api/v1/Users/10
2. Ожидаемый результат: обновление пользователя
3. Заголовки запроса: 
    - Content-Type - application/json
    - Content-Length - calculated when request is sent
    - Host - calculated when request is sent
    - User-Agent - PostmanRuntime/7.32.2
    - Accept - * /*
    - Accept-Encoding - gzip, deflate, br
    - Connection - keep-alive
4. Тело запроса: 
    ```{

    "id": 10,

    "userName": "string",

     "password": "string"

    }```
5. Заголовки ответа: 
    - Content-Type - application/json; charset=utf-8; v=1.0
    - Date - Wed, 31 May 2023 12:24:56 GMT
    - Server - Kestrel
    - Transfer-Encoding - chunked
    - api-supported-versions - 1.0
6. Тело ответа: 
    ```{
    "id": 10,
    "userName": "string",
    "password": "string"
    }```

## 61. Обновление пользователя (PUT - вариант2)
1. URL: https://fakerestapi.azurewebsites.net/api/v1/Users/10
2. Ожидаемый результат: обновление пользователя
3. Заголовки запроса: 
    - Content-Type - application/json
    - Content-Length - calculated when request is sent
    - Host - calculated when request is sent
    - User-Agent - PostmanRuntime/7.32.2
    - Accept - * /*
    - Accept-Encoding - gzip, deflate, br
    - Connection - keep-alive
4. Тело запроса: 
    ```{

    "userName": "string",

    "password": "string"

    }```
5. Заголовки ответа: 
    - Content-Type - application/json; charset=utf-8; v=1.0
    - Date - Wed, 31 May 2023 12:24:56 GMT
    - Server - Kestrel
    - Transfer-Encoding - chunked
    - api-supported-versions - 1.0
6. Тело ответа:
    ```{
    "id": 0,
    "userName": "string",
    "password": "string"
    }```

## 62. Обновление книги (PUT - вариант3)
1. URL: https://fakerestapi.azurewebsites.net/api/v1/Users/10
2. Ожидаемый результат: обновление пользователя
3. Заголовки запроса: 
    - Content-Type - application/json
    - Content-Length - calculated when request is sent
    - Host - calculated when request is sent
    - User-Agent - PostmanRuntime/7.32.2
    - Accept - * /*
    - Accept-Encoding - gzip, deflate, br
    - Connection - keep-alive
4. Тело запроса: 
    ```{

    "id": 0,

    "userName": "null",

     "password": "null"

    }```
5. Заголовки ответа: 
    - Content-Type - application/json; charset=utf-8; v=1.0
    - Date - Wed, 31 May 2023 12:24:56 GMT
    - Server - Kestrel
    - Transfer-Encoding - chunked
    - api-supported-versions - 1.0
6. Тело ответа:
    ```{
    "id": 0,
    "userName": "null",
    "password": "null"
    }```

## 63. Обновление пользователя (PUT - вариант4)
1. URL: https://fakerestapi.azurewebsites.net/api/v1/Users/10
2. Ожидаемый результат: ошибка 400
3. Заголовки запроса: 
    - Content-Type - application/json
    - Content-Length - calculated when request is sent
    - Host - calculated when request is sent
    - User-Agent - PostmanRuntime/7.32.2
    - Accept - * /*
    - Accept-Encoding - gzip, deflate, br
    - Connection - keep-alive
4. Тело запроса: 
    ```{

    "id": string,

    "userName": "0",

    "password": "0"

    }```
5. Заголовки ответа: 
    - Content-Type - application/json; charset=utf-8; v=1.0
    - Date - Wed, 31 May 2023 12:24:56 GMT
    - Server - Kestrel
    - Transfer-Encoding - chunked
6. Тело ответа:
    ```{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-a77be3e9ff0bd04ca1496798853cb451-8c20a110ba5d4846-00",
    "errors": {
        "$.id": [
            "'s' is an invalid start of a value. Path: $.id | LineNumber: 2 | BytePositionInLine: 7."
        ]
    }```

## 64. Удаление пользователя (DELETE)
1. URL: https://fakerestapi.azurewebsites.net/api/v1/Users/10
2. Ожидаемый результат: удаление книги
3. Заголовки запроса: 
    - Host - calculated when request is sent
    - User-Agent - PostmanRuntime/7.32.2
    - Accept - * /*
    - Accept-Encoding - gzip, deflate, br
    - Connection - keep-alive
4. Тело запроса: -
5. Заголовки ответа: 
    - Content-Type - application/json; charset=utf-8; v=1.0
    - Date - Wed, 31 May 2023 12:34:03 GMT
    - Server - Kestrel
    - api-supported-versions - 1.0
6. Тело ответа: -
