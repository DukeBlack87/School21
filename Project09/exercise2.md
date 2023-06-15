# Этапы тестирования веб приложений, применимые к тестированию мобильных приложений

## Функциональное тестирование

В данном пункте важно убедиться, что продукт соответствует нужной функциональной спецификации, упомянутой в документации по разработке.

**Что проверяем?**

1. Установка/удаление/накатка версий
2. Запуск приложения (отображение Splash Screen)
3. Работоспособность основного функционала приложения
    - Авторизация (по номеру телефона/через соц. сети/e-mail)
    - Регистрация (по номеру телефона/через соц. сети/e-mail)
    - Онбординг новых пользователей
    - Валидация обязательных полей
    - Навигация между разделами приложения
    - Редактирование данных в профиле пользователя
    - Проверка оплаты
    - Тестирование фильтров
    - Бонусы
4. Корректное отображение ошибок
5. Работа с файлами (отправка/получение/просмотр)
6. Тестирование тайм-аутов
7. Тестирование заглушек (не соединения с интернетом/нет, например, товаров и т.д)
8. Тестирование pop-up, алертов
9. Тестирование WebView
10. Скролл/свайп элементов
11. Тестирование PUSH уведомлений
12. Сворачивание/разворачивание приложения
13. Разные типы подключений (сотовая связь/Wi-Fi)
14. Ориентация экрана (альбомная/портретная)
15. Темная/светлая темы
16. Реклама в приложении
17. Шаринг контента в соц. сети
18. Работа приложения в фоне
19. Пагинация страниц
20. Политики конфиденциальности и прочие ссылки на документы

## Тестирование совместимости

Тестирование совместимости используется, чтобы убедиться, что ваше приложение совместимо с другими версиями ОС, различными оболочками и сторонними сервисами, а также аппаратным обеспечением устройства.

**Что проверяем?**

1. Корректное отображение гео
2. Информации об операциях (чеки и т.д.)
3. Различные способы оплаты (Google Pay, Apple Pay)
4. Тестирование датчиков (освещенности, температуры устройства, гироскоп и т.д.)
5. Тестирование прерываний (входящий звонок/смс/push/будильник/режим «Не беспокоить» и т.д.)
6. Подключение внешних устройств (карта памяти/наушники и т.д.)

## Тестирование безопасности

Данная проверка нацелена на поиск недостатков и пробелов с точки зрения безопасности приложения.

**Что проверяем?**

1. Тестирование разрешений (доступ к камере/микрофону/галерее/и т.д.)
2. Данные пользователя (пароли) не передаются в открытом виде
3. В полях, с вводом пароля и подтверждением пароля, данные скрываются астерисками

## Тестирование удобства использования

Тестирование удобства использования помогает удостовериться в простоте и эффективности использования продукта пользователем, с целью достижения поставленных целей. Иными словами, это не что иное, как тестирование дружелюбности приложения для пользователя.

**Что проверяем?**

1. Корректное отображение элементов на устройствах с различными разрешениями экранов
2. Все шрифты соответствуют требованиям
3. Все тексты правильно выровнены
4. Все сообщения об ошибках верные, без орфографических и грамматических ошибок
5. Корректные заголовки экранов
6. В поисковых строках присутствуют плейсхолдеры
7. Неактивные элементы отображаются серым
8. Ссылки на документы ведут на соответствующий раздел на сайте
9. Анимация между переходами
10. Корректный возврат на предыдущий экран
11. Поддерживаются основные жесты при работе с сенсорными экранами (swipe back и т.д.)
12. Пиксель-перфект

## Тестирование производительности

Если пользователь устанавливает приложение, и оно не отображается достаточно быстро (например, в течение трех секунд), оно может быть удалено в пользу другого приложения. Аспекты потребления времени и ресурсов являются важными факторами успеха для приложения, и для измерения этих аспектов проводится тестирование производительности.

**Что проверяем?**

1. Время загрузки приложения
2. Обработка запросов
3. Кэширование данных
4. Потребление ресурсов приложением (например расход заряда батареи)