# API для приложения

API для взаимодействия с Фронтендом приложения "Межгалактическая аналитика"

## Доступные ручки

-   **GET /report**

    -   Генерирует CSV отчет с заданными параметрами.
    -   Параметры запроса:
        -   `size` (number, обязателен): Размер отчета в ГБ
        -   `withErrors` (string, по умолчанию "off"): Включать ли ошибки в отчет
        -   `maxSpend` (string, по умолчанию "1000"): Максимальная сумма расходов
    -   Ответ: CSV файл с отчетом или объект с ошибкой

-   **POST /aggregate**
    -   Агрегирует данные, полученные в виде файла (multipart/form-data).
    -   Параметры запроса:
        -   `rows` (number, обязателен): Количество строк для промежуточного агрегирования
    -   Тело запроса: multipart/form-data с файлом
    -   Ответ: JSON-стрим с результатами агрегации или объект с ошибкой

---

## Документация API (Swagger)

Интерактивная документация доступна по адресу: [http://localhost:3000/swagger](http://localhost:3000/swagger)

В ней можно посмотреть описание ручек, параметры и протестировать запросы прямо из браузера.

