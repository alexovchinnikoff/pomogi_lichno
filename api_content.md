| Модуль | ID | Приоритет | Название тест‑кейса | Шаги воспроизведения | Ожидаемый результат (ОР) | Статус |
| --- | --- | --- | --- | --- | --- | --- |
| content | API_cont_1 | Критичный | Получить список всего контента для страниц сайта фонда | 1. Отправить запрос GET на эндпоинт `/content/` | 200 OK. Тело ответа: массив объектов с полями `title`, `slug`, `text`. | Passed |
| content | API_cont_2 | Высокий | Получить список всего контента с некорректным методом POST | 1. Отправить запрос POST на эндпоинт `/content/` | 405 Method Not Allowed | Passed |
| content | API_cont_3 | Высокий | Получить список всего контента с некорректным эндпоинтом | 1. Отправить запрос GET на эндпоинт `/contents/` | 404 Not Found | Passed |
| content | API_cont_4 | Критичный | Получить конкретный объект контента (about) | 1. Отправить запрос GET на эндпоинт `/content/about/` | 200 OK. Объект с полями `title`, `slug`, `text`. | Passed |
| content | API_cont_5 | Критичный | Получить конкретный объект контента (footer) | 1. Отправить запрос GET на эндпоинт `/content/footer/` | 200 OK. Объект с полями `title`, `slug`, `text`. | Passed |
| content | API_cont_6 | Критичный | Получить конкретный объект контента (contacts) | 1. Отправить запрос GET на эндпоинт `/content/contacts/` | 200 OK. Объект с полями `title`, `slug`, `text`. | Passed |
| content | API_cont_7 | Критичный | Получить конкретный объект контента (volunteer) | 1. Отправить запрос GET на эндпоинт `/content/volunteer/` | 200 OK. Объект с полями `title`, `slug`, `text`. | Passed |
| content | API_cont_8 | Критичный | Получить конкретный объект контента (reports) | 1. Отправить запрос GET на эндпоинт `/content/reports/` | 200 OK. Объект с полями `title`, `slug`, `text`. | Passed |
| content | API_cont_9 | Высокий | Получить несуществующий объект контента (header) | 1. Отправить запрос GET на эндпоинт `/content/header/` | 400 Bad Request | Passed |
| content | API_cont_10 | Высокий | Получить объект с отрицательным ID | 1. Отправить запрос GET на эндпоинт `/content/-1/` | 400 Bad Request | Passed |
| content | API_cont_11 | Высокий | Получить объект с ID = 0 | 1. Отправить запрос GET на эндпоинт `/content/0/` | 400 Bad Request | Passed |
| content | API_cont_12 | Высокий | Получить объект с дробным ID | 1. Отправить запрос GET на эндпоинт `/content/1.1/` | 400 Bad Request | Passed |
| content | API_cont_13 | Высокий | Получить объект с пробелом в ID | 1. Отправить запрос GET на эндпоинт `/content/1 1/` | 400 Bad Request | Passed |
| content | API_cont_14 | Высокий | Получить объект со спецсимволами в ID | 1. Отправить запрос GET на эндпоинт `/content/!@#$%^&/` | 400 Bad Request | Passed |
| content | API_cont_15 | Высокий | Получить объект с русскими буквами в ID | 1. Отправить запрос GET на эндпоинт `/content/офонде/` | 400 Bad Request | Passed |
| content | API_cont_16 | Высокий | Получить объект с булевым значением ID | 1. Отправить запрос GET на эндпоинт `/content/?slug=true/` | 400 Bad Request | Failed |
| content | API_cont_17 | Высокий | Получить объект с несколькими значениями подряд | 1. Отправить запрос GET на эндпоинт `/content/aboutreports/` | 404 Not Found | Passed |
