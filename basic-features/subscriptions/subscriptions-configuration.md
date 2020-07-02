# Настройка

## Активация подписок

Чтобы активировать функцию подписки для вашего предприятия, выберите Предприятия -&gt; Настройки -&gt; [настройки магазина](../enterprise-profile/enterprise-settings.md#shop-preferences).

Внизу страницы измените Подписки на 'включено'

![](../../.gitbook/assets/subscriptions1.jpg)

**Гостевые заказы:** Для предприятий с включенными подписками мы рекомендуем, чтобы все клиенты входили в систему, прежде чем они смогут совершать покупки у вас. Это гарантирует, что любой клиент с подпиской войдет в систему и увидит свой существующий заказ на подписку, а случайно не разместит повторный заказ.

**Изменение заказов**: для клиентов с регулярным повторяющимся заказом на вашем предприятии по подписке, следующие варианты подразумевают:

* _Размещенные заказы не могут быть изменены/отменены_: клиент должен будет связаться с вами, чтобы изменить свой обычный заказ \(изменить количество каждого запрошенного товара или отменить заказ\).
* _Клиенты могут изменять/отменять заказы пока цикл заказа открыт_: клиент может изменить количество товаров, которое он запрашивает в своей подписке и/или отменить весь заказ.

{% hint style="info" %}
Во всех случаях, если клиент с заказом на подписку желает приобрести товар, который не является частью его обычного заказа, он должен будет сделать вторую корзину и оформить заказ. _Ни вы, ни они не могут добавлять новые товары в свой заказ на подписку после того, как цикл заказа открыт._
{% endhint %}

## Способы Доставки и Оплаты для Подписок

Когда вы создаете подписку клиента, вам нужно выбрать способ доставки, который он будет использовать и способ оплаты, по которому будет выставлен счет. Это впоследствии будет применяться ко всем следующим заказам, размещенным от его имени посредством подписок.

### **Методы доставки**

К подписке вы можете применить любой [метод дотавки/оплаты](../shopfront/shipping-methods.md).

### **Методы оплаты**

Вы можете назначить подписке только два [метода оплаты](../shopfront/payment-methods.md).

1. **Ручные способы оплаты**: наличными, чеком, банковским переводом \(т.е. любым способом, который не предполагает автоматической проверки в режиме онлайн платформой ОСП\).
2. **Stripe:** Stripe - это платежный шлюз, который принимает платежи с помощью кредитных карт. Подробную информацию о настройке платежей Stripe для вашего предприятия можно найти [здесь](../shopfront/payment-methods.md#integrated-payment-providers).

{% hint style="info" %}
С каждым заказом, автоматически размещаемым по подписке, с банковской карты клиента будет списываться сумма для оплаты заказа \(после закрытия соответствующего цикла заказа\). Сумма списания будет отражать любые изменения, внесенные вами или ими в заказ.  
С клиентов не будет взиматься плата, если они отменят свой заказ подписки.
{% endhint %}

{% hint style="warning" %}
Для правильного списания средств с клиентов, необходимо иметь учетную запись на платформе Открытая Сеть Продуктов. На свою учетную запись ОСП они должны иметь зарегистрированную кредитную карту по умолчанию и дать разрешение вашему предприятию на списание средств с этой карты. Более подробную информацию можно найти [здесь](subscriptions-the-customers-perspective.md#saving-credit-cards-and-authorising-charges).
{% endhint %}

{% hint style="success" %}
Если вы используете Stripe в качестве способа оплаты подписок, клиенту будет полезно, если вы добавите четкое и подробное объяснение того, как будет обрабатываться платеж, если он выберет эту опцию.

Например, вместо того, чтобы называть [способ оплаты](../shopfront/payment-methods.md) 'Кредитная карта', вы можете назвать его 'автоматическим выставлением счетов по кредитной карте за подписки'. Возможным описанием может быть 'С вашей кредитной карты по умолчанию, сохраненной в вашей учетной записи ОСП, будет списана сумма, когда ваш заказ на подписку будет подтвержден в среду вечером'. Это имя и описание будут отображаться в электронном письме с подтверждением клиентам-подписчикам \(см. пример ниже\), поэтому лучше указать подробности, чтобы клиент знал, чего ожидать.
{% endhint %}

![](../../.gitbook/assets/image%20%2815%29.png)

## Сбор информации с ваших клиентов

Чтобы настроить подписку для клиента, вам необходимо получить от него некоторую информацию, как описано ниже:

**Имя, номер телефона** и **email:** Помните, что любой клиент, желающий иметь автоматический регулярный заказ \(подписку\) на вашем предприятии, ДОЛЖЕН иметь зарегистрированную и подтвержденную учетную запись пользователя на платформе ОСП. Клиенты с подписками должны быть в [Списке Клиентов](../shopfront/customer-management-and-conditional-displays-prices/customers.md) вашего предприятия. Подробности смотрите [ниже](subscriptions-configuration.md#add-your-subscribers-to-your-customer-list).

**Адрес для выставления счетов и доставки**

**Товары**: Какие товары они хотят включить в свою подписку?

**Метод Доставки**: Вам необходимо назначить метод доставки/самовывоза для их заказа по подписке. Как бы они предпочли получить товар?

**Метод Оплаты**: клиенты могут выбрать один из способов оплаты вручную \(например, наличными, банковским переводом\) или оплатить с помощью кредитной карты через счет Stripe в вашем магазине. Если клиент желает оплатить свои заказы на подписку через Stripe, ему нужно будет добавить платежную карту по умолчанию и дать разрешение. Смотрите [здесь](subscriptions-the-customers-perspective.md#saving-credit-cards-and-authorising-charges) для более подробной информации.

**Начальная и конечная даты их заказов по подписке**: Помните, что для заказа по подписке, который будет создан для данного цикла заказа, он должен иметь дату начала либо до, либо после даты открытия цикла заказа, а дата окончания подписки должна быть после даты закрытия цикла заказа.

## Добавьте своих подписчиков в свой список клиентов

Прежде чем вы сможете настроить заказ подписки для клиента, его необходимо добавить в [список Клиентов](../shopfront/customer-management-and-conditional-displays-prices/customers.md).

**После того, как вы добавили своих клиентов в свой список клиентов, отправьте им электронное письмо** и [попросите их зарегистрировать учетную запись в ОСП](subscriptions-the-customers-perspective.md#signing-up-to-ofn). Если вы планируете выставлять счета клиентам, использующим Stripe, вам также необходимо попросить их выполнить дополнительные действия, описанные [здесь](subscriptions-the-customers-perspective.md#saving-credit-cards-and-authorising-charges), для добавления кредитной/дебетовой карты по умолчанию к их учетной записи пользователя ОСП и предоставления вашему предприятию разрешения на прием платежей.

{% hint style="info" %}
Вы можете добавлять покупателей в свой список Клиентов до или после того, как они зарегистрируют учетную запись в ОСП. Однако, прежде чем заказ на подписку может быть успешно настроен, клиент должен подтвердить адрес электронной почты, на который зарегистрирована его учетная запись ОСП.
{% endhint %}

{% hint style="warning" %}
Если вы хотите дебетовать клиента по его заказу на подписку с помощью Stripe, он должен быть добавлен в ваш список клиентов ДО того, как они смогут разрешить вашему предприятию принимать платежи со своей кредитной / дебетовой карты.  
If you wish to debit a customer for their subscription order by Stripe then they must be added to your [Customer list](../shopfront/customer-management-and-conditional-displays-prices/customers.md) BEFORE they can [authorise your enterprise to take payments ](subscriptions-the-customers-perspective.md#saving-credit-cards-and-authorising-charges)from their credit/debit card.  
Hence we recommend the following procedure:

1. Contact the customer and obtain all the info you require \(see [above](subscriptions-configuration.md#gather-information-from-your-customers)\)
2. Add them to your [customer list](../shopfront/customer-management-and-conditional-displays-prices/customers.md).
3. Email the customer, asking them to [register with OFN](subscriptions-the-customers-perspective.md#signing-up-to-ofn) for an account and [add their credit/debit card details](subscriptions-the-customers-perspective.md#saving-credit-cards-and-authorising-charges) to that account.
4. [Create the subscription](subscriptions-creating-and-managing-orders.md).
{% endhint %}

## Schedules

{% hint style="info" %}
If you are new to OFN we encourage you to get familiar with setting up [order cycles](../shopfront/order-cycle/) before setting up schedules and subscriptions
{% endhint %}

### About Schedules

Subscriptions are setup so that every time an enterprise opens an order cycle, orders can be automatically generated for customers who have a subscription with that shop. The frequency with which a subscription order is placed for a particular customer \(ie which of your active order cycles triggers their subscription\) is controlled by a facility called '**Schedules**'.

Schedules are groups that order cycle can be assigned to. Once a schedule has been created, customer subscriptions are applied to the schedule, so that an order for their subscription will only be generated for new order cycles in that schedule.

{% hint style="info" %}
You may have some customers who would like a regular order every week, in which case you would add their subscriptions to a schedule which includes all of your weekly order cycles. For other groups of customers, desiring their orders only fortnightly/monthly you can create additional schedules which only include alternate/one-in-four of your weekly order cycles.
{% endhint %}

{% hint style="success" %}
There's lots of flexibility in this arrangement and so feel free to experiment to come up with the order cycle-schedule combination which works best for your enterprise. For example you may wish to have 'odd week' and 'even week' schedules, 'wholesale' schedules, 'monthly meat' schedules....
{% endhint %}

### Create a schedule

Having completed all the steps outlined above, the **+New Schedule** button will appear at the top of your Order Cycles menu:

![](../../.gitbook/assets/ordercycle1.jpg)

{% hint style="warning" %}
You must have at least one open or due to open order cycle to be able to create a new schedule.
{% endhint %}

![](../../.gitbook/assets/new-schedule.bin)

**Name:** Give the schedule a logical name which describes this group of order cycles. E.g. ‘weekly’, ‘monthly’, ‘Tuesday Deliveries’, ‘wholesale’ or ‘retail’. This name is not visible to customers.

{% hint style="info" %}
If you manage several OFN enterprises, with subscriptions being enabled in more than one, then naming your schedules clearly is essential eg. weekly\_hubA, weekly\_hubB, fortnightly\_hubA, fortnightly\_hubB.  
Each enterprise will need a different schedule but when you create a subscription for a customer the schedules for all your enterprises will be visible. Hence, the descriptive name will help you make sure the subscription is created for the correct enterprise for that particular customer.
{% endhint %}

You can add existing order cycles into and out of the new schedule by clicking the &lt; and &gt; buttons.

Click **create** when you are finished.

### Edit or Delete a schedule

To edit or delete a schedule, click on the schedule’s name next to a corresponding order cycle, in the ‘schedules’ column. \(The 'Schedules' column may need to be made visible by ticking it in the drop-down columns menu at the top right.\)

![](../../.gitbook/assets/show-schedules.bin)

You can change the name of the schedule, add/remove order cycles from it or delete the schedule.

![](../../.gitbook/assets/delete-schedule.bin)

{% hint style="danger" %}
You can not delete a schedule if there are subscriptions associated with it.
{% endhint %}

### Adding or removing order cycles from schedules

You can add and remove order cycles from schedules by either editing the schedule \([above](subscriptions-configuration.md#edit-or-delete-a-schedule)\), or by editing the order cycle and adding/removing the schedule in the ‘schedules’ field:

![](../../.gitbook/assets/ordercycle3.jpg)

{% hint style="success" %}
Order cycles can be in more than one schedule. For example if your order cycles are weekly but you have three schedules \(weekly, fortnightly-odd weeks and fortnightly-even weeks\) then one order cycle might be associated with both the 'weekly' and 'fortnightly-odd' week schedules.
{% endhint %}

