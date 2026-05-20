# Задание: Создание тестового класса SerializeDeserializeTests

## Цель
Создать тестовый класс для проверки API сериализации/десериализации при создании аккаунта.

## Описание задачи
Реализуйте тестовый класс `SerializeDeserializeTests` с тестовым методом, который проверяет создание нового аккаунта через API.

##
В начале теста используем mock

```dtd
@Rule
public WireMockRule wireMockRule = new WireMockRule(9876);
```

## Данные для теста
- **Эндпоинт**: `POST /customer/101/accounts`
- **Базовый URL**: `http://localhost:9876`
- **Объект Account**: с типом "savings"
- **Ожидаемый статус**: 201 Created

## Структура ответа API:
```
Request method: POST
Request URI: http://localhost:9876/customer/101/accounts
Headers: Accept=*/*
         Content-Type=text/plain; charset=ISO-8859-1
Body: {"id":1001,"type":"savings","balance":"0"}

Response:
HTTP/1.1 201 Created
Content-Type: application/json
{
    "result": "OK"
}
```
