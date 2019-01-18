# php01
Реализует простейший магазин на LAMP-стеке

В файле https://github.com/elias2k17/php01/blob/master/laptopsheaven_shop.sql.gz находится структура БД и данные

Что сделано:
+ админка сайта - редактирование, добавление товара в архив, добавление нового товара
+ каталог товаров и страница с характеристиками товаров
+ регистрация нового пользователя
+ интерфейс разработан под две группы пользователей - admin и customer.
+ реализовано разделение ролей - группа admin имеет право доступа к админке сайта/доступ ко всем заказам и изменение статуса заказа. Customer только для работы с корзиной и заказами
+ реализована работа с корзиной - просмотр, добавление товара в корзину
+ реализована работа с заказами - администратор может просматривать все заказы, менять статус заказов. Пользователь видит статусы только своих заказов.

Что еще можно было бы допилить:
- управление пользователями
- шаблон страницы error.php, редиректить на эту страницу в случае всех фатальных ошибок или отсуствия прав доступа
- добавить кнопки +/- в корзину, чтобы можно было по-штучно уменьшать/увеличивать кол-во товара в корзине
- корзину хранить временно в сессии, а не в БД (сейчас корзина хранится в БД и сохраняется между сессиями, если не была очищена пользователем)
- добавить виртуальные ID для товаров/заказов, чтобы убрать возможность перебора заказов по номеру
- реализовать функционал ограничения доступа к чужим заказам - каждый юзер может только посмотреть свои заказы (добавить логику в контроллер order.php)
- в списке заказов выводить дату модификации заказа и завести поле "комментарий к заказу", чтобы администратор мог оставлять комментарии к заказу, а пользователь их видел
