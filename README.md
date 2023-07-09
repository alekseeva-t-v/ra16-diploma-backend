# Дипломный проект курса «React» (бэкенд)

Сервер для клиентской части приложения для учебного проекта курса [React для JS-разработчиков](https://netology.ru/programs/react)

## **Основные запросы**

* URL - http://localhost:7777.

* Хиты продаж — GET http://localhost:7777/api/top-sales. В ответ приходит JSON, содержащий данные о хитах продаж.

* Категории каталога — GET http://localhost:7777/api/categories. В ответ приходит массив категорий без элемента «Все».

* Элементы каталога — GET http://localhost:7777/api/items для варианта «Все». При другой выбранной категории запрос вида GET http://localhost:7777/api/items?categoryId=X. Возвращается массив элементов, соответствующих запросу.

* Загрузить ещё — при запросе элементов каталога загружаются следующие 6. При нажатии на «Загрузить ещё» загружаются ещё 6: GET http://localhost:7777/api/items?offset=6, где offset определяет, сколько элементов пропустить.

* Поиск — при заполнении этого поля отправляется запрос вида: GET http://localhost:7777/api/items?q=текст_в_строке_поиска.

* Полная информация о товаре -  запрос GET http://localhost:7777/api/items/:id, где id — это ID товара

* Блок оформления заказа позволяет оформить заказ — POST http://localhost:7777/api/order.

В теле — JSON:

```Java Script
{
  "owner": {
    "phone": "+7xxxxxxxxxxx",
    "address": "Moscow City",
  },
  "items": [
    {
      "id": 1,
      "price": 34000,
      "count": 1
    }
  ]
}
```

## **Запуск проекта**
`npm start` — запускает сервер

