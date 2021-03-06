# Дипломный проект курса «Библиотека React»

![Обложка](./resources/images/cover.jpg)

Дипломный проект представляет собой интернет-магазин обуви. Задача заключается в создании работающего приложения, всеми основными функциями которого можно пользоваться.

## Содержание

Приложение содержит следующие самостоятельные экраны (страницы):

+ Главная страница;
+ Каталог товаров;
+ Избранное;
+ Страница товара;
+ Оформление заказа.

И встроенные (являющиеся частью самостоятельных) экраны:
+ Товар;
+ Корзина покупок;
+ Поиск;
+ Подписка.

## Переходы между экранами

Навигационным центром приложения является шапка каждого экрана (страницы). Из шапки можно попасть на все основные экраны:

+ в **Каталог товаров**  
Кликнув по любой из ссылок в нижней части шапки;
+ в **Избранное**  
Кликнув по иконке профиля в шапке, затем по ссылке «Избранное»;
+ в **Корзину покупок**  
Кликнув по иконке корзины;
+ на **Главную страницу**  
Кликнув по логотипу.

![Шапка](./resources/images/from-header.jpg)

С большинства экранов можно попасть на экран «Страница товара», кликнув по названию или фотографии товара:

![К товару](./resources/images/to-item.jpg)

Единственным экраном, на который нельзя попасть откуда угодно, является экран «Оформление заказа». Перейти к этому экрану можно только из Корзины покупок, кликнув по кнопке «Оформить заказ»:

![Оформить](./resources/images/ordering.jpg)

## Описание экранов

### Главная страница

Экран «Главная страница» доступен по умолчанию при открытии приложения.

[![Главная страница](./resources/images/desktop-small.jpg)](./resources/main.png) [![Главная страница схема](./resources/images/des-desktop-small.jpg)](./resources/images/des-desktop-full.jpg)

Этот экран содержит, в основном, описания акций и новостей, которые для нас не представляют особого интереса. 

Реализовать на этом экране нужно блок «Новинки»:

![Новинки](./resources/images/featured.png)

В блоке должны быть доступны возможности:
1. **Посмотреть все новинки**.  
Товары листаются с помощью стрелок вправо и влево.
2. **Добавить товар / товары в Избранное**  
Для добавления нужно кликнуть на сердечко в правом верхнем углу активного товара. При добавлении сердечко становится закрашенным.
3. **Убрать товар / товары из Избранного, если он был добавлен ранее**  
Чтобы убрать товар из избранного, нужно повторно кликнуть на сердечко. После этого сердечко снова становится белым.
4. **Перейти на страницу товара**  
Переход происходит по клику.

Получение списка новинок подробно описывается в разделе «Рекомендации по технической реализации» данного описания.

### Каталог товаров

На экран «Каталог товаров» можно попасть с любого самостоятельного экрана, кликнув по одной из ссылок в шапке страницы.

[![Каталог товаров](./resources/images/cat-small.jpg)](./resources/catalog.png) [![Каталог товаров](./resources/images/des-cat-small.jpg)](./resources/images/des-cat-full.jpg)

На экране «Каталог товаров» должны быть отображены все доступные товары в магазине. Товары отображаются постранично, на одной странице **15** товаров. Внизу страницы располагается пагинация.

На странице каталога должна быть доступна фильтрация товаров по следующим критериям:
+ Тип обуви (балетки, босоножки, ботильоны...);
+ Цена (диапазон цен);
+ Цвет;
+ Размер;
+ Размер каблука;
+ Повод (офис, вечеринка, свадьба);
+ Сезон;
+ Бренд;
+ Наличие скидки.

Все фильтры должно быть можно выключить, кликнув по кнопке «**x** Сбросить» внизу перечня фильтров.

Также должна быть доступна сортировка товаров по следующим критериям:
+ По популярности;
+ По размеру;
+ По производителю.

В отношении каждого из товаров доступны возможности, аналогичные таковым на главной странице:
1. **Добавить товар / товары в Избранное**  
Для добавления нужно кликнуть на сердечко в правом верхнем углу активного товара. При добавлении сердечко становится закрашенным.
2. **Убрать товар / товары из Избранного, если он был добавлен ранее**  
Чтобы убрать товар из избранного, нужно повторно кликнуть на сердечко. После этого сердечко снова становится белым.
3. **Перейти на страницу товара**  
Переход происходит по клику.

Получение списка новинок подробно описывается в разделе «Рекомендации по технической реализации» данного описания.

### Избранное

На экран «Избранное» можно попасть с любого самостоятельного экрана, кликнув по иконке профиля в шапке, затем по ссылке «Избранное».

[![Избранное](./resources/images/fav-small.jpg)](./resources/favourites.png) [![Избранное](./resources/images/des-fav-small.jpg)](./resources/images/des-fav-full.jpg)

На этом экране отображаются все товары, добавленные пользователем кликом по сердечку. Товары отображаются постранично, на одной странице **12** товаров. Внизу страницы также располагается пагинация.

Доступна сортировка товаров по следующим критериям:
+ По популярности;
+ По размеру;
+ По производителю.

В отношении каждого из товаров доступны возможности:
1. **Убрать товар / товары из Избранного, если он был добавлен ранее**  
Чтобы убрать товар из избранного, нужно повторно кликнуть на сердечко. После этого товар должен исчезнуть со страницы.
2. **Перейти на страницу товара**  
Переход происходит по клику.

### Страница товара

На экран «Страница товара» можно попасть, кликнув на товар в любом из экранов. 

[![Страница товара](./resources/images/item-small.jpg)](./resources/item.png) [![Страница товара](./resources/images/des-item-small.jpg)](./resources/images/des-item-full.jpg)

Главный блок данного экрана это «Информация о товаре», где отображается подробная информация о товаре, а именно:
1. Фотографии товара в формате галереи.
2. Наименование, Артикул, Производитель, Цвет, Материал, Сезон, Повод.
3. Доступные размеры.
4. Индикатор наличия.

В блоке «Информация о товаре» должны быть доступны следующие возможности:
1. **Добавить товар в Избранное**  
Для добавления нужно кликнуть по кнопке _«В избранное»_ под информацией о товаре. При добавлении сердечко кнопки становится закрашенным, а текст изменяется на _«В избранном»_
2. **Убрать товар из Избранного, если он был добавлен ранее**  
Чтобы убрать товар из избранного, нужно кликнуть по кнопке _«В избранном»_.
3. **Добавить товар в Корзину**  
Для добавления необходимо предварительно выбрать размер и количество товаров. Если размер не выбран, добавление товара в Корзину не происходит.  
Значения параметров по умолчанию: «Размер» — _нет значения_; Количество товаров — _1_.

Кроме информации о выбранном товаре на экране также есть два блока с информацией о других товарах:

1. Блок «Вы смотрели», где выводятся все товары (но не больше 10), страницы которых посетил пользователь во время текущей сессии.
2. Блок «Похожие товары», где выводятся товары, чей _Тип_ и _Цвет_ совпадают с _Типом_ и _Цветом_ текущего товара.

### Оформление заказа

На экран «Оформление заказа» можно попасть только из встроенного экрана «Корзина», кликнув по кнопке «Оформить заказ».

[![Оформление заказа](./resources/images/order-small.jpg)](./resources/order.png) [![Оформление заказа](./resources/images/des-order-small.jpg)](./resources/images/des-order-full.jpg)

На этом экране есть два основных блока:

1. Подробное отображение товаров, добавленных в «Корзину», а именно:
   + Наименование товара;
   + Фотография;
   + Выбранный размер;
   + Производитель;
   + Количество с возможностью его изменить;
   + Цена (изменяется в зависимости от количества).
2. «Форма заказа», в которой есть следующие элементы:
   + Поле для ввода имени покупателя;
   + Поле для ввода телефона;
   + Поле для ввода адреса;
   + Выбор формы оплаты (доступно 3 варианта: Картой онлайн, Картой курьеру, Наличными курьеру)
   + Кнопка подтверждения заказа.

Все поля в Форме заказа являются обязательными для заполнения.

При успешном подтверждении заказа блоки Корзина и Форма заказа сменяются блоком «Заказ принят, спасибо!». В блоке выводятся следующие данные:
1. Итог заказа:
   + Сумма всего заказа;
   + Выбранный способ оплаты;
   + Имя клиента;
   + Адрес доставки;
   + Телефон
2. Уведомление об отправке копии итога на электронную почту;
3. Предложение продолжить покупки (кнопка, нажатие на которую ведет на страницу Каталога товаров).

### Корзина покупок
Корзина покупок доступна на любом экране и реализуется в виде раздвижной панели в шапке сайта. Отображается по клику на значок корзины:

![cart](./resources/images/cart.png)

Если в корзину добавлено от одного до трёх товаров, скролл не отображается.

Если в корзине нет товаров, то отображается уведомление «В корзине пока ничего нет. Не знаете, с чего начать? Посмотрите наши новинки!»:

![cart](./resources/images/cart_empty.jpg)

На панели корзины доступны следующие возможности:
1. **Перейти на страницу товара**  
Переход происходит по клику.
2. **Убрать товар из корзины**  
Для этого нужно кликнуть на крестик справа от цены товара.
3. **Оформить заказ**  
Для этого необходимо кликнуть на кнопку «Оформить заказ». При клике происходит переход на экран «Оформление заказа».

### Поиск
На сайте должен быть реализован поиск по товарам. Поле для ввода поискового запроса доступно всегда в шапке страницы по клику на иконку в форме лупы. 

Страница вывода результатов поиска представляет собой страницу каталога, где выведены только товары, соответствующие запросу. Все функции страницы каталога (фильтры, сортировка, быстрый просмотр товара, добавление в избранное) доступны на этой странице. Изменяется только заголовок и «хлебные крошки»:

![search](./resources/images/search.png)

### Подписка
На сайте должна быть реализована подписка на выгодные предложения. Форма подписки доступна всегда в подвале страницы. Пользователь может выбрать между группами предложений (женские, мужские, общие) и оставить свой адрес электронной почты.

После того, как пользователь подписался на предложения, нужно показать уведомление об успешной подписке — «Подписка оформлена! Спасибо!»:

![subscribe](./resources/images/subscribe.png)


## Рекомендации по технической реализации

### Фильтры

Выбранные пользователем фильтры хранятся в состоянии приложения. При запросе списка товаров используются выбранные фильтры.

### Корзина

При добавлении товара в корзину в `localStorage` проверяется наличие идентификатора корзины, если он доступен, то запрос отправляется вместе в ним. В противном случае запрос отправляется без идентификатора, полученный ответ сохраняется в `localStorage`.

### Избранное

Список идентификаторов избранных товаров хранится в `localStorage`.

## Взаимодействие с сервером по HTTP

Для взаимодействия с серверной частью приложения вам доступно REST API по адресу:

https://neto-api.herokuapp.com/bosa-noga

### Получение списка категорий

` GET /categories` — получить информацию о категориях в JSON-формате.

В ответ приходит либо сообщение об ошибке, либо JSON-массив со списком категорий. Например:
```json
{
    "data": [
        {
            "id": 12,
            "title": "Мужская обувь"
        },
        {
            "id": 13,
            "title": "Женская обувь"
        }
    ],
    "status": "ok"
}
```

Тут:
- `data` — данные по запросу, _объект_;
- `id` — идентификатор категории на сервере, _число_;
- `title` — название категории, _строка_;
- `status` — статус запроса, _строка_;

Поле `status` может быть `'ok'` и `'error'`. Если состояние `'error'`, то показывается ещё текст с ошибкой в поле `'message'`.

### Получение списка товаров

`GET /products` — получить информацию о товарах в JSON-формате.

В ответ приходит либо сообщение об ошибке, либо JSON-массив со списком из 10 товаров, согласно переданному параметру `page`, например:
```json
{
  "data": [
    {
      "id": 20,
      "categoryId": 13,
      "title": "Кроссовки как у Pharrell Williams",
      "images": [
        "https://neto-api.herokuapp.com/bosa-noga/Chanel-x-Adidas-Originals-NMD-Hu_480x480.jpg?v=1512941013",
        "https://neto-api.herokuapp.com/bosa-noga/5113054-1_1.jpg"
      ],
      "brand": "Chanel",
      "price": 12000,
      "oldPrice": 14000
    },
    {
      "id": 47,
      "categoryId": 13,
      "title": "Рыбацкая сетка",
      "images": [
        "https://neto-api.herokuapp.com/bosa-noga/1519322087_KCP277SUR_S900_E02_G.jpg",
        "https://neto-api.herokuapp.com/bosa-noga/1519322087_KCP277SUR_S900_E03_D.jpg"
      ],
      "brand": "Dior",
      "price": 5000
    }
  ],
  "pagination": {
    "goods": 62,
    "pages": 7,
    "limit": 10,
    "offset": 0
  },
  "status": "Ok"
}
```

Тут:
- `data` — объект с данными о товарах, _объект_;
- `id` — идентификатор товара на сервере, _число_;
- `categoryId` — идентификатор категории, которой принедлежит товар, _число_;
- `title` — название товара, _строка_;
- `images` — список URL-адрес главного изображения товара, по которому оно доступно в сети, _массив_;
- `brand` — производитель, _строка_;
- `price` — цена товара в рублях, _число_;
- `oldPrice` — цена товара в рублях без скидки, _число_, необязательное поле (есть только у товаров, которые продаются по скидке);
- `pagination` — данные о пагинации, _объект_;
- `goods` — общее количество соответствующих фильтру товаров, _число_;
- `pages` — число требуемых страниц для отображения всех товаров, _число_;
- `limit` — количество возвращаемых товаров за один запрос, _число_;
- `offset` — отступ задаваемый параметром `page` в параметрах, _число_;


Данный метод поддерживает сортировку и фильтрацию, формат данных при отправке — `GET-параметры`. Необязательные поля для фильтрации и сортировки:

- `page` — номер страницы (отступ от начала списка товаров), _число_;
- `type` — тип обуви (балетки, босоножки, ботильоны…), _строка_;
- `color` — цвет обуви, _строка_;
- `size` — размер обуви, _число_;
- `heelSize` — размер каблука, _число_;
- `reason` — повод (офис, вечеринка, свадьба), _строка_;
- `season` — сезон, _строка_;
- `brand` — бренд, _строка_;
- `discounted` — наличие скидки, _логическое значение_;
- `categoryId` — идентификатор категории, _число_;
- `sortBy` — поле для сортировки, _строка_;

### Получение новинок

`GET /featured` — получить информацию о новинках товаров в JSON-формате.

В ответ приходит либо сообщение об ошибке, либо JSON-массив со списком товаров. Например:
```json
{
  "data": [
    {
      "id": 20,
      "categoryId": 13,
      "title": "Кроссовки как у Pharrell Williams",
      "images": [
        "https://neto-api.herokuapp.com/bosa-noga/Chanel-x-Adidas-Originals-NMD-Hu_480x480.jpg?v=1512941013",
        "https://neto-api.herokuapp.com/bosa-noga/5113054-1_1.jpg"
      ],
      "brand": "Chanel",
      "price": 12000,
      "oldPrice": 14000
    },
    {
      "id": 21,
      "categoryId": 13,
      "title": "Туфли принцессы",
      "images": [
        "https://neto-api.herokuapp.com/bosa-noga/c5e4699d3c9c.jpg",
        "https://neto-api.herokuapp.com/bosa-noga/s800.webp"
      ],
      "brand": "Dolce & Gabbana",
      "price": 3000
    },
  ],
  "status": "ok"
}
```

Структура ответа аналогична таковой при получении списка товаров.

### Получение информации о товаре

`GET /products/${id}` — получить информацию о товаре в JSON-формате. Тут `${id}` — идентификатор товара на сервере.

В ответ приходит либо сообщение об ошибке, либо JSON-объект с данными о товаре. Например:
```json
{
  "data": {
    "id": 25,
    "categoryId": 13,
    "title": "Туфли императрицы",
    "images": [
      "https://neto-api.herokuapp.com/bosa-noga/images5134523.jpg",
      "https://neto-api.herokuapp.com/bosa-noga/dolce-gabbana-red-tufli-3.jpg"
    ],
    "sku": "1000005",
    "brand": "Dolce & Gabbana",
    "color": "Бардо",
    "material": "Ткань",
    "reason": "Высокая мода",
    "season": "Лето",
    "heelSize": 8,
    "price": 15000,
    "sizes": [
      {
        "size": 15,
        "avalible": true
      },
      {
        "size": 18,
        "avalible": false
      }
    ]
  },
    "status": "ok"
}
```

Кроме полей, которые уже были описаны при получении списка товаров, еще некоторые свойства с ключами:
- `images` — URL-адреса изображений товара, по которому они доступны в сети, первое изображение считается главным, _массив строк_;
- `color` — цвет товара, _строка_;
- `material` — материал, из которого произведен товар, _строка_;
- `reason` — повод, по которому предполагается носить товар, _строка_;
- `season` — сезон, для которого подходит товар, _строка_;
- `heelSize` — размер каблука, _число_ сантиметров;
- `sizes` — информация о размерах и наличии их на складе, _массив объектов_.

Свойство `sizes`, которое хранит массив объетов со следующими свойствами:
- `size` — размер, _число_;
- `avalible` — доступность размера на складе, _логическое значение_.

### Создание корзины

`POST /cart/` — создать новую корзину.

Формат данных при отправке `json-объект`. Пример запроса:
```json
{
  "id": 42,
  "size": 14,
  "amount": 12
}
```

Тут:
- `id` — идентификатор товара на сервере, _число_;
- `size` — размер выбранного товара, _число_;
- `amount` — количество единиц выбранного товара, _число_;

Указанный товар будет добавлен в корзину.

В ответ приходит либо объект с описанием ошибки, либо идентификатор новой корзины.

```json
{
    "id": "-LGp7nXm_acnkzaFQU4Y",
    "status": "ok"
}
```

### Получение содержимого корзины

`GET /cart/${cartId}` — получить список товаров в корзине. Тут `${cartId}` — идентификатор корзины.

В ответ приходит либо сообщение об ошибке, либо JSON-объект с данными о товарах в корзине.

```json
{
  "data": {
    "id": "-LGp7nXm_acnkzaFQU4Y",
    "products": [
      {
        "id": 42,
        "size": 14,
        "amount": 12
      }
    ]
  },
  "status": "ok"
}
```

Тут:
- `data` — содержимое корзины, _объект_;
- `id` — идентификатор корзины, _строка_;
- `products` — список объектов товаров, _массив_;
- `id` — идентификатор товара на сервере, _число_;
- `size` — размер товара, _число_;
- `amount` — количество товара в корзине, _число_;

### Добавление, обновление и удаление товаров из корзины

`POST /cart/${cartId}` — изменить состав коризны. Тут `${cartId}` — идентификатор корзины.

Формат данных при отправке `json-объект`. Пример запроса:
```json
{
  "id": 1,
  "size": 13,
  "amount": 1
}
```

Тут:
- `id` — идентификатор товара на сервере, _число_;
- `size` — размер товара, _число_;
- `amount` — количество единиц товара, _число_.

Указанный товар будет добавлен в корзину, либо обновлен, если уже существовал. 

Для удаления одного из размеров у выбранного товара необходимо передать поле `amount` равное нулю.

В ответ приходит либо сообщение об ошибке, либо объект обновленной корзины, аналогичный предыдущему.

### Создание заказа

`POST /order` — создать новый заказ.

Формат данных при отправке `json-объект`. Пример запроса:
```json
{
	"name": "Николай",
	"phone": "8  999  495 53 33",
	"address": "ул. Гоголя, 92",
	"paymentType": "onlineCard",
	"cart": "-LGp7nXm_acnkzaFQU4Y"
}
```

Тут:
- `name` — имя заказчика, _строка_;
- `phone` — телефон заказчика, _строка_;
- `address` — адрес заказчика, _стркоа_;
- `paymentType` — способ оплаты, _строка, одно из_:
  - `onlineCard` — картой онлайн, _стркоа_;
  - `offlineCard` — картой при получении _стркоа_;
  - `offlineCash` — наличными при получении; _стркоа_;
- `cart` — идентификатор корзины, _строка_;

В ответ приходит либо сообщение об ошибке, либо JSON-объект с данными о товарах в корзине.

```json
{
  "data": {
    "id": "-LGp7wgmnIez0ZiJtPF3",
    "info": {
      "name": "Николай",
      "phone": "8  999  495 53 33",
      "address": "ул. Гоголя, 92",
      "paymentType": "onlineCard",
      "cart": "-LGp7nXm_acnkzaFQU4Y"
    }
  },
  "status": "ok"
}
```

Тут:
- `data` — содержимое заказа, _объект_;
- `id` — идентификатор созданного заказа, _строка_;
- `info` — список объектов товаров, _массив_;

После оформления заказа корзина удаляется