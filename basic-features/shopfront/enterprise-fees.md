# Сборы Предприятия

Сборы Предприятия полезны для производителей и центров, которые работают вместе: это позволяет распределять расходы, связанные с администрированием, упаковкой, транспортировкой, продажами и сбором средств, между различными сторонами.

Например, центр может выбрать добавление корпоративного сбора в размере 10% ко всем товарам, которые они продают, чтобы покрыть свои административные расходы \(хранение товаров до распределения, зарплаты людей, которые управляют продажами и координируют их ...\)

Для производителей, продающих свои собственные товары напрямую, эти затраты уже присутствуют в стоимости товара, поэтому необходмости в применении Сборов Предприятия нет.

Одним из многих преимуществ для клиентов ОСП является прозрачность цен. Покупатели могут видеть процент от цены товара, назначенной администратору, упаковке и т.д. Эта информация отображается при нажатии на круговую диаграмму рядом с ценой товара на витрине магазина:

![&#x421;&#x431;&#x43E;&#x440; &#x41F;&#x440;&#x435;&#x434;&#x43F;&#x440;&#x438;&#x44F;&#x442;&#x438;&#x44F; &#x432; &#x432;&#x438;&#x442;&#x440;&#x438;&#x43D;&#x435; &#x43C;&#x430;&#x433;&#x430;&#x437;&#x438;&#x43D;&#x430;](../../.gitbook/assets/enterprsie-fee-in-shopfront.png)

Прежде чем двигаться дальше, вы можете взглянуть на быструю демонстрацию настройки вашего первого сбора предприятия:

![](../../.gitbook/assets/enterprisefeefirst.gif)

## Настройка Сборов Предприятия

* Перейдите на страницу Сборы Предприятия, нажав на **Предприятия** в синем горизонтальном меню, а затем нажмите **Настройки** рядом с вашим предприятием. Страница **Сборы Предприятия** находится в меню слева.
* Нажмите **Создать сейчас** \(или **Управление Сборами Предприятия**, если вы уже настроили и хотите изменить\). Вы будете перенаправлены на такую страницу:

![](../../.gitbook/assets/enterprisefeecreate.jpg)

**Предприятие**: в первом столбце выберите предприятие, к которому применяется сбор.

**Тип Сбора**: выберите услугу, к которой применяется данный сбор. Возможные варианты: Оплата Упаковки, Транспортный Сбор, Административный Сбор, Сбор с Продаж или Сбор на Пожертвования.

**Название**: выберите имя для этого сбора.

**Налоговая Категория**: выберите соответствующую налоговую ставку. В большинстве случаев ставка НДС для сбора с предприятия будет унаследована от товара. Если сбор предприятия связан с услугой, добавленной к товару, этот сбор может облагаться НДС, а сам товар - нет. В этом случае выберите 'Нулевая ставка', 'Полная ставка' и 'Пониженная ставка' НДС, применяемого к Cборам Предприятия.

**Калькулятор:** сбор может быть рассчитан несколькими способами. Выберите калькулятор, который лучше всего подходит.

Нажмите Обновить, чтобы создать сбор предприятия.

{% hint style="info" %}
Вы сможете указывать только тарифы или значения \(в столбце 'значения калькулятора' после создания Cбора Предприятия\).
{% endhint %}

![](../../.gitbook/assets/enterprisefee2.jpg)

## Калькуляторы Сбора

![](../../.gitbook/assets/enterprisefee3.jpg)

**Flat Percent** – This fee is charged as a percentage of the total amount charged in the order.

**Weight \(per kg\)** – this fee is applied to products on a per kg basis. The fee will _only be applied to products which are priced at a per kg rate_, not products listed as items \(e.g. A product listed as ‘1 bunch of parsley’ will not have an associated enterprise fee with this option.\)

**Flat Rate \(per order\)** – This fee is applied as standard fee to all orders, regardless of the size of the order.

**Flexible Rate** – This fee calculator is especially useful if you'd like to encourage customers to place large orders: the enterprise can be reduced or zero when the threshold number of items has been reached.

* ‘First Item Cost’: The fee charged for the first item in the order.
* ‘Additional Item Cost’: The fee charged for items beyond the first item.
* ‘Max Items’: The maximum number of items on which the fee will be applied. Items purchased beyond this amount will be not be charged the fee.

![](../../.gitbook/assets/enterprisefeeflex.jpg)

> For Example: if the 'First Item Cost' is set to £0.20, 'Additional Item Cost' is £0.10 and 'Max Items' is 3 then a customer who purchases 5 items will be charged £0.40 in enterprise fees \(£0.20 for the first item, £0.10 for items two and three, and £0.00 for items four and five\).

**Flat Rate \(per item\):** This fee is a constant fee, applied to products listed as ‘items’. \(It is not applied to products sold by weight or volume. Hence there will be no associated enterprise fee charged to a customer who, for example, buys rice by kg.\)

**Price Sack:** This is a flexible enterprise fee method charged by _total monetary sale_, rather than number of items purchased \(Flexible Rate above\)

* ‘Minimum Amount’: Monetary value of the threshold between Normal Enterprise fee and Discounted Enterprise fee. 
* 'Normal Amount': Payment Method fee applied to sales below the threshold stated in 'Minimum Amount'.
* ‘Discount Amount’: Payment Method fee applied to sales above the threshold stated in 'Minimum Amount'.

![](../../.gitbook/assets/enterprisefeepc.jpg)

{% hint style="warning" %}
Now that you've created your Enterprise Fee remember that **it will not apply in your shop unless it's added to an order cycle**. See the order cycle pages for [producers](order-cycle/order-cycles-for-producers.md) or [hubs ](order-cycle/order-cycles-for-hubs.md)for more details.
{% endhint %}

