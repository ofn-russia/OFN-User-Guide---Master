---
description: '1'
---

# Возврат и Корректировка Платежей

Иногда вам может потребоваться изменить сумму, которую клиент платит за свой заказ. Общие сценарии включают в себя:

* Заказы, содержащие товары с переменным весом, которые неизвестны на момент заказа \(например, [мясо или большие овощи](../products-1/pricing-irregular-items-kg.md), продаются по весу, но как готовые изделия\)
* Заказанный товар не был доставлен производителем.
* Клиент связывается с вами, чтобы добавить дополнительные товары в свою корзину.
* Один \(или более\) заказанный товар не соответствует ожидаемому качеству и вы хотите компенсировать это покупателю. Есть два основных случая:
* Заказчик **оплачивает свою продукцию при самовывозе**, поэтому оплата не была произведена заранее. В этом случае вы можете откорректировать заказ клиента, повторно отправить электронное письмо с подтверждением заказа и денежные средства, полученные в день самовывоза, отражают обновленную сумму к оплате.
* **Заказ был оплачен во время его офрмления** \(Stripe, PayPal или банковский перевод\). В этом случае есть три варианта:
  1. Остаток в КРЕДИТЕ \(вы должны деньги клиенту\) и вы хотите вернуть их.
  2. Остаток в КРЕДИТЕ и вы хотите, чтобы клиент мог использовать этот кредит для будущих покупок.
  3. Остаток в ДОЛГЕ \(клиент должен вам деньги\)

## Как вернуть Платеж

### Refunding a Stripe Payment

_If the customer made the payment for their order to your business Stripe account, then you will be able to issue a full or partial refund from the OFN admin interface._

Make sure the order you wish to refund is marked as 'PAID':

![](../../.gitbook/assets/image%20%2817%29.png)

Adjust the order as necessary \(read [here](view-orders.md#editing-an-order) for how to edit an order or read more about [bulk order management](view-orders.md#bulk-order-management) for managing scenarios such as [product shortage](view-orders.md#example-1-you-have-a-stock-shortage-and-must-reduce-customer-order-quantities-for-a-certain-product) or [irregularly priced meat items](../products-1/pricing-irregular-items-kg.md).\)

You will then see the that there is CREDIT on the modified order. Select the 'tick' to the right of the order to issue a refund via Stripe:

![](../../.gitbook/assets/capture-du-2019-02-27-20-04-19.png)

The refund will be recorded on your business' Stripe account:

![](../../.gitbook/assets/stripecredit.png)

{% hint style="info" %}
Refunds take 5-10 days to appear on a customer's statement.
{% endhint %}

{% hint style="warning" %}
The fees charged by Stripe \(1.4% - 2.9% + 20p per transaction\) are not refunded to your business. They are charged based on the amount originally paid.  
It might, therefore, be more advantageous to offer the customer credit against their next \(or future\) order rather than issue a refund.
{% endhint %}

If an order has been totally cancelled you can issue a full refund \(if the customer paid by Stripe\) by [Edit order](view-orders.md#editing-an-order) -&gt; Payments and then selecting the 'cross' to the right hand side of the table:

![](../../.gitbook/assets/stripefullrefund.png)

### Возврат платежа PayPal

Автоматическое частичное или полное возмещение средств клиентам, оплатившим свои заказы через PayPal на данный момент не поддерживается платформой ОСП. Вам нужно будет посетить свой бизнес-аккаунт PayPal и вернуть деньги через их платформу.  
Эта функциональность, которую мы надеемся добавить в будущем.

### Возврат Оплаты Банковским Переводом

_Клиент оплачивает свои покупки банковским переводом или любым другим неавтоматизированным способом \(т. е. любым способом, кроме Stripe или PayPal\) и вы регистрируете его платеж. Позднее необходимо_ [_отредактировать его заказ_](view-orders.md#editing-an-order) _\(товар недоступен или был доставлен бракованным\). После выполнения этой корректировки переплата, сделанная клиентом, отображается как кредит по его заказу._  
Чтобы оформить возврат банковского перевода, вам нужно будет сделать это через свой банковский аккаунт.

## Как оформить Кредит клиента под его следующий заказ

Альтернативой возврату переплаты может быть ручное удержание кредита клиента из его следующего заказа.

{% hint style="info" %}
В настоящее время, будучи менеджером Магазина или Центра, вам необходимо вручную настроить баланс клиентов, чтобы учесть их кредит. В будущем мы хотели бы автоматизировать этот процесс. Пожалуйста, [свяжитесь с нами](https://www.openfoodnetwork.org/find-your-local-open-food-network/), если что-то будет полезно для вашего предприятия.
{% endhint %}

## Как выставить счет клиенту на дополнительные средства

Например, клиент может попросить вас добавить дополнительный товар к заказу, за который он уже заплатил или вы можете обнаружить, что после получения мяса \([или других готовых изделий, оцененных по весу](../products-1/pricing-irregular-items-kg.md)\) общая сумма счета увеличивается незначительно.  
Любые дополнительные оплаченные средства должны быть записаны вручную. Клиент не сможет оплатить превышение по Stripe или PayPal через платформу ОСП.

{% hint style="info" %}
Если клиент желает добавить товар в свою корзину, который он первоначально забыл, но оплачивает его через Stripe или PayPal, то может быть проще попросить его создать другой заказ, чем редактировать существующий заказ.
{% endhint %}

