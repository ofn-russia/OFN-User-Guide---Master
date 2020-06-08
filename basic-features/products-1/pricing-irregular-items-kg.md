# Цены на Мясо и другие 'готовые' товары с неизвестным весом

Здесь мы называем продукты 'не регулярными, если они продаются по весу/объему, но точное количество неизвестно до момента сбора/распределения.

Например куски мяса, ломтики сыра, крупные овощи.

Существует ряд различных инструментов, доступных на платформе ОСП, чтобы помочь управлять и организовать такие продажи.

## Первый Вариант: Установить средний вес/цену и возвращать

Вы можете назначить среднюю цену продукта, а затем возвращать или взимать с клиента дополнительную плату, если фактический вес отклоняется от среднего значения.

Когда вы знаете точный вес продуктов \(т.е. когда вы готовите заказы для получения клиентами\), войдите в "Пакетное Управление Заказами" \(Заказы -&gt; Пакетное Управление Заказами\) и добавьте столбец Вес/Объем в таблицу.

![](../../.gitbook/assets/bom1.jpg)

Затем вы можете изменить вес, указанный для каждого покупателя для данного заказа и данного товара. Цена автоматически будет пересчитана в соответствии с введенным количеством.

{% hint style="info" %}
Не забудьте повторно отправить клиенту электронное письмо с подтверждением заказа, чтобы уведомить их о разнице в цене и любых денежных средствах, которые они могут впоследствии выплатить.
{% endhint %}

## Второй Вариант: Показать ценовые диапазоны

Та же логика, что и в первом варианте, но вместо того, чтобы первоначально отображать среднюю цену, указывается диапазон цен. Это решение имеет то преимущество, что четко указывает покупателю, что окончательная цена может быть изменена.

[Варианты](product-variants.md) также могут быть использованы для создания различных диапазонов.

> **Пример 1** \(один товар и один вариант\):   
> Продукт = курица \(от 8 до 12кг с ценой в зависимости от веса, 100руб. / кг\)
>
> **Пример 2** \(два варианта для одного товара\):  
> Продукт = курица \(100руб. / кг\)  
> Вариант 1 = маленькая курица \(от 8 до 12 кг, цена в соответствии с фактическим весом\)  
> Вариант 2 = Крупная курица \(от 13 до 20 кг, цена зависит от фактического веса\) ...

## Третий Вариант: Создание вариантов с фиксированными ценами

Несколько более простая версия Второго Варианта заключается в создании вариантов для ваших продуктов на основе диапазонов веса, но с фиксированной ценой для всех элементов, попадающих в этот диапазон.  
Например, если тыква с орехами стоит 100руб / кг, вы можете перечислить варианты со следующими фиксированными ценами:

* Маленький \(0.7 - 0.9 кг\)           80руб
* Средний \(0.9 - 1.1 кг\)      100руб
* Большой \(1.1 - 1.3 кг\)           120руб
* Очень Большой \(1.3 - 1.5 кг\) 140руб

## Четвёртый Вариант: Создание вариантов с известным весом

Например, если вы заранее знаете вес всей своей рыбы, вы можете использовать функциональность варианта, чтобы напрямую отобразить точную цену для каждого товара. Пример:

![](../../.gitbook/assets/bom2.jpg)

## Редактирование Заказов

Производителям мяса может быть сложно заранее узнать о наличии продуктов или соответствующим образом подготовить их упаковку. \(До того, как забить, вес курицы или бараньей ноги, возможно неизвестен.\)

Это не проблема, так как заказы могут быть изменены \(путем добавления, изменения или удаления товаров\) при необходимости. Для получения дополнительной информации см. [Заказы](../orders/).

## Reimbursing or Charging customers the difference: How does it work?

If a customer _**pays for their goods on their collection**_ or delivery, then the hub manager will have been able to modify the order before payment according to the actual weight and the products actually delivered. Hence in this instance there will be no need to reimburse or re-bill customer.

If an order is _**paid online before delivery**_, then you must refund or invoice for the the difference between monies already received and that owing for the precise products to be delivered. Click here to see [how](../orders/refund-payments.md).

{% hint style="danger" %}
An alternative is to use an online payment system to temporarily store the amount "pending" until the order has been validated.

_This feature is not yet implemented in Open Food Network. We are also working on the automated implementation of "credits" allowing a hub to reimburse in the form of a credit note which could be used by the customer as part payment for their next order._
{% endhint %}

## Inform the buyer about your pricing policy

You can notify your customers about your pricing policies for variable weight items \(such as meat\) in the [message box](../enterprise-profile/enterprise-settings.md#shop-preferences) displayed at the top of your shop front. This is found in the Enterprise Settings -&gt; Shop Preferences.

It might be useful to also add a reminder of these pricing policies in the description box of [Payment Methods](../shopfront/payment-methods.md). For example, you may wish to add : "Remember that the final price may vary by 10% depending on weight if you have purchased non-divisible items such as meat or large vegetables.".

