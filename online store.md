**Plan**
front <---> back <---> (PostgreSQL)

**technologies:**
- boot 
- web
- security
- thymeleaf
- data jpa + postgresql
- additional:
-- flyway
-- lombbok

**features:** 
- Аутентификация и регистрация пользователей
- Защита веб-приложения
- Просмотр товаров
- Добавление товаров в корзину
- Формирование заказов
- Оплата (PayPal)
- Фильтрация/сортировка товаров
- Управление корзиной
- Валидация вводимых данных
- Оповщения по e-mail
- Навигация

Entities:
1.Product
-- id
-- title
-- price
-- categories
-- sales (optional)
2.User
-- id
-- username
-- email
-- password
-- role
-- address
-- archive
3.Role
-- USER
-- GUEST
-- ADMIN
-- MANAGER
4.Order
-- id
-- created date
--  last change date
-- completed date
-- addressOrder
-- user
-- status (NEW, CANCEL, PAID, CLOSED, RETURNED)
-- details ( product. price, amount, comment)
5.Category
-- id
-- tittle
6.Bucket
-- id
-- user
-- details (product, amount) /product list
