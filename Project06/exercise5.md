# Swagger

## 1. GET /api/v1/Activities

- HTTP-метод: **GET**
- Полный URL запроса: "https://fakerestapi.azurewebsites.net/api/v1/Activities"
- Заголовки запроса: **-H  "accept: text/plain; v=1.0"**
- Тело запроса (при наличии):
- Статус-код ответа: **200**
- Тело ответа (при наличии): **[
  {
    "id": 1,
    "title": "Activity 1",
    "dueDate": "2023-05-22T13:26:08.7428527+00:00",
    "completed": false
  }, ]**

## 2. POST /api/v1/Activities

- HTTP-метод: **POST**
- Полный URL запроса: "https://fakerestapi.azurewebsites.net/api/v1/Activities"
- Заголовки запроса: **-H  "accept: text/plain; v=1.0" -H  "Content-Type: application/json; v=1.0"**
- Тело запроса (при наличии): **{
  "id": 0,
  "title": "string",
  "dueDate": "2023-05-22T13:11:15.854Z",
  "completed": true
}**
- Статус-код ответа: **200**
- Тело ответа (при наличии): **{
  "id": 0,
  "title": "string",
  "dueDate": "2023-05-22T13:11:15.854Z",
  "completed": true
}**

## 3. GET ​/api​/v1​/Activities​/10

- HTTP-метод: **GET**
- Полный URL запроса: "https://fakerestapi.azurewebsites.net/api/v1/Activities/10"
- Заголовки запроса: **-H  "accept: text/plain; v=1.0"**
- Тело запроса (при наличии):
- Статус-код ответа: **200**
- Тело ответа (при наличии): **{
  "id": 10,
  "title": "Activity 10",
  "dueDate": "2023-05-23T00:31:41.1116049+00:00",
  "completed": true
}**

## 4. GET ​/api​/v1​/Activities​/500

- HTTP-метод: **GET**
- Полный URL запроса: "https://fakerestapi.azurewebsites.net/api/v1/Activities/500"
- Заголовки запроса: **-H  "accept: text/plain; v=1.0"**
- Тело запроса (при наличии):
- Статус-код ответа: **404**
- Тело ответа (при наличии): **{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
  "title": "Not Found",
  "status": 404,
  "traceId": "00-666f9b0be289c348910c81f4297052f1-4b62af9242399548-00"
}**

## 5. PUT ​/api​/v1​/Activities​/550

- HTTP-метод: **PUT**
- Полный URL запроса: "https://fakerestapi.azurewebsites.net/api/v1/Activities/550"
- Заголовки запроса: **-H  "accept: text/plain; v=1.0" -H  "Content-Type: application/json; v=1.0"**
- Тело запроса (при наличии): **{
  "id": 0,
  "title": "string",
  "dueDate": "2023-05-22T14:39:19.785Z",
  "completed": true
}**
- Статус-код ответа: **200**
- Тело ответа (при наличии): **{
  "id": 0,
  "title": "string",
  "dueDate": "2023-05-22T14:39:19.785Z",
  "completed": true
}**

## 6. PUT ​/api​/v1​/Activities​/8877877878778787

- HTTP-метод: **PUT**
- Полный URL запроса: "https://fakerestapi.azurewebsites.net/api/v1/Activities/8877877878778787"
- Заголовки запроса: **-H  "accept: text/plain; v=1.0" -H  "Content-Type: application/json; v=1.0"**
- Тело запроса (при наличии): **{
  "id": 0,
  "title": "string",
  "dueDate": "2023-05-22T14:39:19.785Z",
  "completed": true
}**
- Статус-код ответа: **400**
- Тело ответа (при наличии): **{
  "id": 0,
  "title": "string",
  "dueDate": "2023-05-22T14:39:19.785Z",
  "completed": true
}**

## 7. DELETE ​/api​/v1​/Activities​/120

- HTTP-метод: **DELETE**
- Полный URL запроса: "https://fakerestapi.azurewebsites.net/api/v1/Activities/120"
- Заголовки запроса: **-H  "accept: */*"**
- Тело запроса (при наличии):
- Статус-код ответа: **200**
- Тело ответа (при наличии):

## 8. DELETE ​/api​/v1​/Activities​/898989889989

- HTTP-метод: **DELETE**
- Полный URL запроса: "https://fakerestapi.azurewebsites.net/api/v1/Activities/898989889989"
- Заголовки запроса: **-H  "accept: */*"**
- Тело запроса (при наличии):
- Статус-код ответа: **400**
- Тело ответа (при наличии): **{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-00607dbd23c484498b55095a3b21b9ff-1ee2d7c41bc7d049-00",
  "errors": {
    "id": [
      "The value '898989889989' is not valid."
    ]
  }
}**

## 9. GET /api/v1/Authors

- HTTP-метод: **GET**
- Полный URL запроса: "https://fakerestapi.azurewebsites.net/api/v1/Authors"
- Заголовки запроса: **-H  "accept: text/plain; v=1.0"**
- Тело запроса (при наличии):
- Статус-код ответа: **200**
- Тело ответа (при наличии): **[
  {
    "id": 1,
    "idBook": 1,
    "firstName": "First Name 1",
    "lastName": "Last Name 1"
  }, ]**

## 10. POST /api/v1/Authors

- HTTP-метод: **POST**
- Полный URL запроса: "https://fakerestapi.azurewebsites.net/api/v1/Authors"
- Заголовки запроса: **-H  "accept: text/plain; v=1.0" -H  "Content-Type: application/json; v=1.0"**
- Тело запроса (при наличии): **{
  "id": 0,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}**
- Статус-код ответа: **200**
- Тело ответа (при наличии): **{
  "id": 0,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}**

## 11. GET /api/v1/Authors/authors/books/12

- HTTP-метод: **GET**
- Полный URL запроса: "https://fakerestapi.azurewebsites.net/api/v1/Authors/authors/books/12"
- Заголовки запроса: **-H  "accept: text/plain; v=1.0"**
- Тело запроса (при наличии):
- Статус-код ответа: **200**
- Тело ответа (при наличии): **[
  {
    "id": 35,
    "idBook": 12,
    "firstName": "First Name 35",
    "lastName": "Last Name 35"
  }, ]**

## 12. GET /api/v1/Authors/authors/books/419684684168

- HTTP-метод: **GET**
- Полный URL запроса: "https://fakerestapi.azurewebsites.net/api/v1/Authors/authors/books/419684684168"
- Заголовки запроса: **-H  "accept: text/plain; v=1.0"**
- Тело запроса (при наличии):
- Статус-код ответа: **400**
- Тело ответа (при наличии): **{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-eb8e7d49944de54aa94fd6e19f6d514d-972ffe273c49604a-00",
  "errors": {
    "idBook": [
      "The value '419684684168' is not valid."
    ]
  }
}**

## 13. GET /api/v1/Authors/9

- HTTP-метод: **GET**
- Полный URL запроса: "https://fakerestapi.azurewebsites.net/api/v1/Authors/9"
- Заголовки запроса: **-H  "accept: text/plain; v=1.0"**
- Тело запроса (при наличии):
- Статус-код ответа: **200**
- Тело ответа (при наличии): **{
  "id": 9,
  "idBook": 4,
  "firstName": "First Name 9",
  "lastName": "Last Name 9"
}**

## 14. GET /api/v1/Authors/650

- HTTP-метод: **GET**
- Полный URL запроса: "https://fakerestapi.azurewebsites.net/api/v1/Authors/650"
- Заголовки запроса: **-H  "accept: text/plain; v=1.0"**
- Тело запроса (при наличии):
- Статус-код ответа: **404**
- Тело ответа (при наличии): **{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
  "title": "Not Found",
  "status": 404,
  "traceId": "00-0c8b7ec30d27f24787f97452dcb24131-09aed6130ecdf440-00"
}**

## 15. PUT​ /api/v1/Authors/33

- HTTP-метод: **PUT**
- Полный URL запроса: "https://fakerestapi.azurewebsites.net/api/v1/Authors/33"
- Заголовки запроса: **-H  "accept: text/plain; v=1.0" -H  "Content-Type: application/json; v=1.0"**
- Тело запроса (при наличии): **{
  "id": 0,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}**
- Статус-код ответа: **200**
- Тело ответа (при наличии): **{
  "id": 0,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}**

## 16. PUT /api/v1/Authors/9998985496

- HTTP-метод: **PUT**
- Полный URL запроса: "https://fakerestapi.azurewebsites.net/api/v1/Authors/9998985496"
- Заголовки запроса: **-H  "accept: text/plain; v=1.0" -H  "Content-Type: application/json; v=1.0"**
- Тело запроса (при наличии): **{
  "id": 0,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}**
- Статус-код ответа: **400**
- Тело ответа (при наличии): **{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-252314f003183a4e9dbfb5370ed8a397-293ad12af7d7134a-00",
  "errors": {
    "id": [
      "The value '9998985496' is not valid."
    ]
  }
}**

## 17. DELETE /api/v1/Authors/14

- HTTP-метод: **DELETE**
- Полный URL запроса: "https://fakerestapi.azurewebsites.net/api/v1/Authors/14"
- Заголовки запроса: **-H  "accept: */*"**
- Тело запроса (при наличии):
- Статус-код ответа: **200**
- Тело ответа (при наличии):

## 18. DELETE /api/v1/Authors/14000000000

- HTTP-метод: **DELETE**
- Полный URL запроса: "https://fakerestapi.azurewebsites.net/api/v1/Authors/14000000000"
- Заголовки запроса: **-H  "accept: */*"**
- Тело запроса (при наличии):
- Статус-код ответа: **400**
- Тело ответа (при наличии): **{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-f79b3f925105c749b07994c23d81d3a8-e391f46bb73cf645-00",
  "errors": {
    "id": [
      "The value '14000000000' is not valid."
    ]
  }
}**

## 19. GET /api/v1/Books

- HTTP-метод: **GET**
- Полный URL запроса: "https://fakerestapi.azurewebsites.net/api/v1/Books"
- Заголовки запроса: **-H  "accept: text/plain; v=1.0"**
- Тело запроса (при наличии):
- Статус-код ответа: **200**
- Тело ответа (при наличии): **[
  {
    "id": 1,
    "title": "Book 1",
    "description": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
    "pageCount": 100,
    "excerpt": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
    "publishDate": "2023-05-21T19:11:58.1358681+00:00"
  }, ]**

## 20. POST /api/v1/Books

- HTTP-метод: **POST**
- Полный URL запроса: "https://fakerestapi.azurewebsites.net/api/v1/Authors"
- Заголовки запроса: **-H  "accept: */*" -H  "Content-Type: application/json; v=1.0"**
- Тело запроса (при наличии): **{
  "id": 0,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-05-22T19:15:17.458Z"
}**
- Статус-код ответа: **200**
- Тело ответа (при наличии): **{
  "id": 0,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-05-22T19:15:17.458Z"
}**

## 21. GET /api/v1/Books/21

- HTTP-метод: **GET**
- Полный URL запроса: "https://fakerestapi.azurewebsites.net/api/v1/Books/21"
- Заголовки запроса: **-H  "accept: text/plain; v=1.0"**
- Тело запроса (при наличии):
- Статус-код ответа: **200**
- Тело ответа (при наличии): **{
  "id": 21,
  "title": "Book 21",
  "description": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
  "pageCount": 2100,
  "excerpt": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
  "publishDate": "2023-05-01T19:19:42.490665+00:00"
}**

## 22. GET /api/v1/Books/300

- HTTP-метод: **GET**
- Полный URL запроса: "https://fakerestapi.azurewebsites.net/api/v1/Books/300"
- Заголовки запроса: **-H  "accept: text/plain; v=1.0"**
- Тело запроса (при наличии):
- Статус-код ответа: **404**
- Тело ответа (при наличии): **{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
  "title": "Not Found",
  "status": 404,
  "traceId": "00-28b2dc1b82945147b482249392ad74db-e490a185879dfd4b-00"
}**

## 23. PUT /api/v1/Books/16

- HTTP-метод: **PUT**
- Полный URL запроса: "https://fakerestapi.azurewebsites.net/api/v1/Books/16"
- Заголовки запроса: **-H  "accept: */*" -H  "Content-Type: application/json; v=1.0"**
- Тело запроса (при наличии): **{
  "id": 0,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-05-22T19:22:44.310Z"
}**
- Статус-код ответа: **200**
- Тело ответа (при наличии): **{
  "id": 0,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-05-22T19:22:44.31Z"
}**

## 24. PUT /api/v1/Books/10501150414

- HTTP-метод: **PUT**
- Полный URL запроса: "https://fakerestapi.azurewebsites.net/api/v1/Books/10501150414"
- Заголовки запроса: **-H  "accept: */*" -H  "Content-Type: application/json; v=1.0"**
- Тело запроса (при наличии): **{
  "id": 0,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-05-22T19:22:44.310Z"
}**
- Статус-код ответа: **400**
- Тело ответа (при наличии): **{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-b9a3de5863e5c249a39f976f442a4722-cbebba6566bfd34a-00",
  "errors": {
    "id": [
      "The value '10501150414' is not valid."
    ]
  }
}**

## 25. DELETE /api/v1/Books/14

- HTTP-метод: **DELETE**
- Полный URL запроса: "https://fakerestapi.azurewebsites.net/api/v1/Books/14"
- Заголовки запроса: **-H  "accept: */*"**
- Тело запроса (при наличии):
- Статус-код ответа: **200**
- Тело ответа (при наличии):

## 26. DELETE /api/v1/Books/96847646464

- HTTP-метод: **DELETE**
- Полный URL запроса: "https://fakerestapi.azurewebsites.net/api/v1/Books/96847646464"
- Заголовки запроса: **-H  "accept: */*"**
- Тело запроса (при наличии):
- Статус-код ответа: **400**
- Тело ответа (при наличии): **{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-e84d1dea21e43249ab1e9f0400316648-348c9de248d47c4a-00",
  "errors": {
    "id": [
      "The value '96847646464' is not valid."
    ]
  }
}**

## 27. GET /api/v1/CoverPhotos

- HTTP-метод: **GET**
- Полный URL запроса: "https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos"
- Заголовки запроса: **-H  "accept: text/plain; v=1.0"**
- Тело запроса (при наличии):
- Статус-код ответа: **200**
- Тело ответа (при наличии): **[
  {
    "id": 1,
    "idBook": 1,
    "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"
  }, ]**

## 28. POST /api/v1/CoverPhotos

- HTTP-метод: **POST**
- Полный URL запроса: "https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos"
- Заголовки запроса: **-H  "accept: text/plain; v=1.0" -H  "Content-Type: application/json; v=1.0"**
- Тело запроса (при наличии): **{
  "id": 0,
  "idBook": 0,
  "url": "string"
}**
- Статус-код ответа: **200**
- Тело ответа (при наличии): **{
  "id": 0,
  "idBook": 0,
  "url": "string"
}**

## 29. GET /api/v1/CoverPhotos/books/covers/2

- HTTP-метод: **GET**
- Полный URL запроса: "https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/books/covers/2"
- Заголовки запроса: **-H  "accept: text/plain; v=1.0"**
- Тело запроса (при наличии):
- Статус-код ответа: **200**
- Тело ответа (при наличии): **[
  {
    "id": 2,
    "idBook": 2,
    "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 2&w=250&h=350"
  }
]**

## 30. GET /api/v1/CoverPhotos/books/covers/4040104046

- HTTP-метод: **GET**
- Полный URL запроса: "https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/books/covers/4040104046"
- Заголовки запроса: **-H  "accept: text/plain; v=1.0"**
- Тело запроса (при наличии):
- Статус-код ответа: **400**
- Тело ответа (при наличии): **{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-5a785d1fb910bb4aa9df8ec08f9e428b-80b75fe5d13e0c4c-00",
  "errors": {
    "idBook": [
      "The value '4040104046' is not valid."
    ]
  }
}**

## 31. GET ​/api​/v1​/CoverPhotos​/18

- HTTP-метод: **GET**
- Полный URL запроса: "https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/18"
- Заголовки запроса: **-H  "accept: text/plain; v=1.0"**
- Тело запроса (при наличии):
- Статус-код ответа: **200**
- Тело ответа (при наличии): **{
  "id": 18,
  "idBook": 18,
  "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 18&w=250&h=350"
}**

## 32. GET ​/api​/v1​/CoverPhotos​/404

- HTTP-метод: **GET**
- Полный URL запроса: "https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/404"
- Заголовки запроса: **-H  "accept: text/plain; v=1.0"**
- Тело запроса (при наличии):
- Статус-код ответа: **404**
- Тело ответа (при наличии): **{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
  "title": "Not Found",
  "status": 404,
  "traceId": "00-1841fc671fc62646b35fc53279b99ba7-80eec76ee1fc114f-00"
}**

## 33. PUT /api/v1/CoverPhotos/11

- HTTP-метод: **PUT**
- Полный URL запроса: "https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/11"
- Заголовки запроса: **-H  "accept: text/plain; v=1.0" -H  "Content-Type: application/json; v=1.0"**
- Тело запроса (при наличии): **{
  "id": 0,
  "idBook": 0,
  "url": "string"
}**
- Статус-код ответа: **200**
- Тело ответа (при наличии): **{
  "id": 0,
  "idBook": 0,
  "url": "string"
}**

## 34. PUT /api/v1/CoverPhotos/80885465254

- HTTP-метод: **PUT**
- Полный URL запроса: "https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/80885465254"
- Заголовки запроса: **-H  "accept: text/plain; v=1.0" -H  "Content-Type: application/json; v=1.0"**
- Тело запроса (при наличии): **{
  "id": 0,
  "idBook": 0,
  "url": "string"
}**
- Статус-код ответа: **400**
- Тело ответа (при наличии): **{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-61f28d3dc7aace4face18d01323de262-8b13211222f05540-00",
  "errors": {
    "id": [
      "The value '80885465254' is not valid."
    ]
  }
}**

## 35. DELETE /api/v1/CoverPhotos/7

- HTTP-метод: **DELETE**
- Полный URL запроса: "https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/7"
- Заголовки запроса: **-H  "accept: */*"**
- Тело запроса (при наличии):
- Статус-код ответа: **200**
- Тело ответа (при наличии):

## 36. DELETE /api/v1/CoverPhotos/9899955251

- HTTP-метод: **DELETE**
- Полный URL запроса: "https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/9899955251"
- Заголовки запроса: **-H  "accept: */*"**
- Тело запроса (при наличии):
- Статус-код ответа: **400**
- Тело ответа (при наличии): **{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-32e348efe8717f4c89ea09c7d58c1840-eed877d171be8140-00",
  "errors": {
    "id": [
      "The value '9899955251' is not valid."
    ]
  }
}**

## 37. GET /api/v1/Users

- HTTP-метод: **GET**
- Полный URL запроса: "https://fakerestapi.azurewebsites.net/api/v1/Users"
- Заголовки запроса: **-H  "accept: text/plain; v=1.0"**
- Тело запроса (при наличии):
- Статус-код ответа: **200**
- Тело ответа (при наличии): **[
  {
    "id": 1,
    "userName": "User 1",
    "password": "Password1"
  }, ]**

## 38. POST /api/v1/Users

- HTTP-метод: **POST**
- Полный URL запроса: "https://fakerestapi.azurewebsites.net/api/v1/Users"
- Заголовки запроса: **-H  "accept: */*" -H  "Content-Type: application/json; v=1.0"**
- Тело запроса (при наличии): **{
  "id": 0,
  "userName": "string",
  "password": "string"
}**
- Статус-код ответа: **200**
- Тело ответа (при наличии): **{
  "id": 0,
  "userName": "string",
  "password": "string"
}**

## 39. GET /api/v1/Users/5

- HTTP-метод: **GET**
- Полный URL запроса: "https://fakerestapi.azurewebsites.net/api/v1/Users/5"
- Заголовки запроса: **-H  "accept: */*"**
- Тело запроса (при наличии):
- Статус-код ответа: **200**
- Тело ответа (при наличии): **{
  "id": 5,
  "userName": "User 5",
  "password": "Password5"
}**

## 40. GET /api/v1/Users/87

- HTTP-метод: **GET**
- Полный URL запроса: "https://fakerestapi.azurewebsites.net/api/v1/Users/87"
- Заголовки запроса: **-H  "accept: */*"**
- Тело запроса (при наличии):
- Статус-код ответа: **404**
- Тело ответа (при наличии): **{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
  "title": "Not Found",
  "status": 404,
  "traceId": "00-175eec5c1a4af8489b3f49a8252d4bd4-97c00430ed03fa43-00"
}**

## 41. PUT /api/v1/Users/03

- HTTP-метод: **PUT**
- Полный URL запроса: "https://fakerestapi.azurewebsites.net/api/v1/Users/03"
- Заголовки запроса: **-H  "accept: */*" -H  "Content-Type: application/json; v=1.0"**
- Тело запроса (при наличии): **{
  "id": 0,
  "userName": "string",
  "password": "string"
}**
- Статус-код ответа: **200**
- Тело ответа (при наличии): **{
  "id": 0,
  "userName": "string",
  "password": "string"
}**

## 42. PUT /api/v1/Users/87878778755

- HTTP-метод: **PUT**
- Полный URL запроса: "https://fakerestapi.azurewebsites.net/api/v1/Users/87878778755"
- Заголовки запроса: **-H  "accept: */*" -H  "Content-Type: application/json; v=1.0"**
- Тело запроса (при наличии): **{
  "id": 0,
  "userName": "string",
  "password": "string"
}**
- Статус-код ответа: **400**
- Тело ответа (при наличии): **{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-0183ba064aa3894e93d9e902822aa9ef-1527ab9b67b5fe4f-00",
  "errors": {
    "id": [
      "The value '87878778755' is not valid."
    ]
  }
}**

## 43. DELETE /api/v1/Users/8

- HTTP-метод: **DELETE**
- Полный URL запроса: "https://fakerestapi.azurewebsites.net/api/v1/Users/8"
- Заголовки запроса: **-H  "accept: */*"**
- Тело запроса (при наличии):
- Статус-код ответа: **200**
- Тело ответа (при наличии):

## 44. DELETE /api/v1/Users/6941464194

- HTTP-метод: **DELETE**
- Полный URL запроса: "https://fakerestapi.azurewebsites.net/api/v1/Users/6941464194"
- Заголовки запроса: **-H  "accept: */*"**
- Тело запроса (при наличии):
- Статус-код ответа: **400**
- Тело ответа (при наличии): **{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-21a7c8c9a6704945bb276c4ddbc44549-f93dde072abf5a47-00",
  "errors": {
    "id": [
      "The value '6941464194' is not valid."
    ]
  }
}**
