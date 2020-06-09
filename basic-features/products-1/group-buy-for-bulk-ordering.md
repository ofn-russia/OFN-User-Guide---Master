# Групповая Покупка - для массового заказа

Функция **Групповая покупка** предназначена для предприятий, которые покупают некоторые входящие запасы в больших количествах и перепродают их небольшими единицами \(например, покупая мешок риса по 25 кг и продавая его покупателям по 1 кг\).

Массовые закупки - обычная практика для групп покупателей, которые, покупая большие объемы, могут получить выгоду от оптовых цен так же, как обычные дистрибьюторы. Таким образом, участники получают доступ к продуктам намного дешевле, чем они могли бы получить от розничных продавцов.

Для таких предприятий решение о том, заказывать ли определенный товар, зависит от того, достаточно ли заказали заказчики в совокупности, чтобы оправдать оптовую покупку. Это может быть связано с величиной скидки или платой за доставку. Функция групповой покупки позволяет центру достичь эффективности массовых закупок.

Когда товар распределен по групповой покупке, он будет отображаться по-разному на витрине магазина \(см. ниже\), с отображением в столбце мин / макс количества:

![](../../.gitbook/assets/group-buy%20%281%29.png)

Клиента просят указать:

* Их **минимальное** количество - это количество товара, которое они в идеале хотят.
* Их **максимальное** количество - это максимальная сумма, которую они готовы купить.

{% hint style="info" %}
По сути, для клиента это способ клиента сказать: 'У вас есть мое разрешение увеличить мой заказ до этого момента, если это означает, что как группа, мы можем достичь большого количества заказа'.
{% endhint %}

[В Пакетном Управлении Заказами](../orders/view-orders.md#bulk-order-management)  вы можете просмотреть общие минимальные и максимальные объемы заказов для товара от всех ваших клиентов. Затем вы можете либо поднять заказы клиента в пределах их допустимого диапазона, чтобы достичь массового количества, либо, если максимальный объем заказа не дотягивает, вы можете удалить все заказы для этого товара.

## Включение Групповой Покупки для товара

На панели администратора перейдите в '**Товары'** в синем горизонтальном меню. Выберите **Изменить** товар, щелкнув значок карандаша и бумаги справа от соответствующего товара:

![](../../.gitbook/assets/productedit.jpg)

Затем выберите **Параметры Групповой Покупки** в меню справа.

![](../../.gitbook/assets/groupbuy.jpg)

Выберите **Да** в **Групповая Покупка?**, чтобы активировать эту функцию для товара.

**Размер Оптовой Единицы** - это кол-во, которое должен достичь коллективный заказ группы.

{% hint style="warning" %}
**Единицы** Размера Оптовой Единицы зависят от единиц, выбранных для розничной продажи товара покупателям.

Если товар продается по:

* **Вес**: единицы измерения в гр \(поэтому, если общий вес должен быть равен 5кг, введите в этом поле '5000'\)
* **Объем**: единицы измерения в литрах \(поэтому, если общий объем должен составлять 10л, введите '10' в это поле\)
* **Предметы**: например продажа букетов цветов, но в общей сложности необходимо купить 100 букетов, а тогда необходимо ввести '100' в этом поле.
{% endhint %}

## Adjusting Orders to make complete Batches

Under Orders-&gt; [bulk order management](../orders/view-orders.md#bulk-order-management) you can view and edit customer orders for Bulk Buy products to make the combined order from all customers reach your required threshold.

1. Select the order cycle or date range of interest.
2. Search for the product \(Fish in the example below\).
3. Make sure the ‘Max’ column is displayed so you can see the upper limit each customers is prepared to purchase.
4. Next, click on the value \('test fish: Fish One' in the example below\) in the **Product : Unit** column, to display the orders total box \(in blue\) for the product in question. 
5. Using the information in the column **Max**, you can increase the quantities ordered to reach the threshold for a complete batch. 
6. Click update to save changes to customer orders.

![](../../.gitbook/assets/bulkorder2.jpg)

**Current Fulfilled Units** divides your total quantity ordered by the group buy unit size. If this figure is greater than 1, it tells you that the existing customer order satisfy or exceed your required group buy unit size. If this figure is less than 1, existing customer orders don’t meet that threshold. As you raise the quantity of customer orders, this figure will raise.

**Max Fulfilled Units** takes the sum or all of the customer’s MAX order quantities and divides this by the Group Buy Unit Size. If the number is over 1, then you know that the total of your MAX orders exceeds the required group buy quantity. If it’s below zero, it means that even the MAX order quantities won’t reach the threshold.

