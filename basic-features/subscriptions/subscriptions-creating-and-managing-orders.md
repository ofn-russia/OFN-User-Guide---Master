# Подписки - Создание заказов и Управление ими

На этой странице описывается, как магазины могут настраивать уникальные подписки для отдельных клиентов, в том числе, какие товары включены в их подписку, к какому [расписанию](subscriptions-configuration.md#schedules) применяется подписка \(т.е. скорось, с которой они получают свой заказ\) и как приостановить/именить свою подписку.

{% hint style="danger" %}
В этой первой версии функции подписки, **предприятия должны настраивать подписки от имени своих клиентов**. Клиенты не могут настроить собственные подписки.
{% endhint %}

**Контрольный список действий перед созданием подписок для ваших клиентов:**

* Включить подписки в ваших [Настройках Предприятия](subscriptions-configuration.md#activate-subscriptions)
* Задать [методы доставки и оплаты](subscriptions-configuration.md#shipping-and-payment-methods-for-subscriptions)
* Связаться с вашими клиентами, чтобы [получить их данные](subscriptions-configuration.md#gather-information-from-your-customers)
* Добавить подписчиков в ваш [список клиентов](subscriptions-configuration.md#add-your-subscribers-to-your-customer-list).  
* Свяжитесь с вашими клиентами, чтобы попросить их [зарегистрировать учетную запись в ОСП](subscriptions-the-customers-perspective.md#signing-up-to-ofn), и если им будет выставлен счет в Stripe, попросить [сохранить свою карту и авторизовать ваш магазин для снятия с нее средств](subscriptions-the-customers-perspective.md#saving-credit-cards-and-authorising-charges).
* Создать минимум одно [Расписание](subscriptions-configuration.md#schedules)

## Создание подписок

Нажмите **Заказы** в синем горизонтальном меню, а затем выберите **Подписки** в зеленом подменю.

![](../../.gitbook/assets/sub1.jpg)

Нажмите **+Новая Подписка**, чтобы настроить повторяющийся заказ для вашего клиента. Сначала вам будет предложено выбрать магазин, в котором вы хотите создать новую подписку.

{% hint style="danger" %}
Вы должны создать расписание циклов заказа, прежде чем сможете создать подписку. Узнайте больше [здесь](subscriptions-configuration.md#schedules).
{% endhint %}

### Основные Подробности

![](../../.gitbook/assets/sub2.jpg)

**Клиент**: выберите клиента из выпадающего списка. Вы можете выбрать только тех людей, которые добавлены в [Список Клиентов](subscriptions-configuration.md#add-your-subscribers-to-your-customer-list) для Предприятия, с которым вы создаете подписку.

**Расписание**: выберите расписание, на которое этот клиент хочет подписаться.

**Способ оплаты**: выберите предпочтительный способ оплаты клиента. Это должен быть либо Stripe, либо способ оплаты вручную \(наличными, банковским переводом\). Смотрите [здесь](subscriptions-configuration.md#payment-methods) для получения дополнительной информации.

**Способ доставки**: выберите предпочтительный способ доставки.

**Начинается С**: Это дата, когда будет создан первый заказ клиента, сгенерированный по подписке.

{% hint style="danger" %}
Если эта дата находится посередине открытого цикла заказа в их расписании, то будет создан заказ для этого цикла заказа. Если нет, то их первый заказ на подписку будет размещен, когда начнется следующий цикл заказа, который будет открыт в их расписании.
{% endhint %}

**Заканчивается В**: после этой даты заказы клиента по подписке больше не будут генерироваться. Это поле является необязательным, если оставить его пустым, заказ будет генерироваться бесконечно.

{% hint style="danger" %}
Если дата 'Заканчивается В' приходится на середину будущего цикла заказа, то заказ по подписке размещаться не будет. Например:

* Если дата Заканчивается В - 10/01/2020, но самый близкий цикл заказа в расписании этого клиента должен открыться 9 января 2020 и закрыться 11 января 2020, то для клиента не будет сгенерирован заказ.
* Если дата Заканчивается В - 12/01/2020, то вышеуказанный цикл заказа сгенерирует последний заказ по подписке для клиента.
{% endhint %}

### Адрес

Заполните платежные реквизиты клиента. Сведения об адресе для клиентов, которые ранее размещали заказы на ОСП, будут заполнены автоматически.

![](../../.gitbook/assets/new-subscription-address.png)

{% hint style="warning" %}
Если вы обновите адрес/контактную информацию клиента на странице [Клиента](../shopfront/customer-management-and-conditional-displays-prices/customers.md), изменение не будет автоматически перенесено на его подписку. Вам нужно будет обновить их детали и здесь.
{% endhint %}

### **Добавить Товары**

Добавьте товары, которые клиент желает получать от вашего предприятия на регулярной основе.

![](../../.gitbook/assets/new-subscription-add-products.bin)

{% hint style="warning" %}
Вы можете добавлять только те товары, которые перечислены в будущих циклах заказа для вашего предприятия и которые также входят в выбранную клиентом подписку по расписанию.
{% endhint %}

### Проверить и Сохранить

Проверьте правильность сведений и нажмите '**Создать Подписку**' или '**Отмена**'.

{% hint style="warning" %}
Если расписание, для которого вы только что создали новую подписку клиента, имеет открытый цикл заказа, то его первый заказ будет сгенерирован немедленно, если вы не измените дату 'Начинается В' на какой-то момент в будущем.
{% endhint %}

#### Что произойдет, если стоимость товара изменится после подписки?

Цены на товары в рамках подписки будут обновлены и с клиента будет взиматься плата в соответствии с обновленной стоимостью. В начале каждого цикла заказа, с помощью которого создается их подписка, они получат электронное письмо со сводкой своего заказа, включая актуальные цены.

#### Что если товар в подписке недоступен в цикле заказа?

Когда элемент в подписке недоступен \(например, если это сезонный товар\), клиент получит уведомление в своих электронных письмах с подтверждением.

## Изменить подписку клиента

### Изменить базовую подписку

Чтобы внести изменения во всю подписку \(т.е. все заказы, сделанные с этого момента для клиента\), перейдите в раздел **Заказы** \(синее меню\) -&gt; **Подписки** \(зеленое подменю\).

Выберите предприятие, на которое у клиента есть подписка, в раскрывающемся меню.

![](../../.gitbook/assets/sub1%20%281%29.jpg)

После этого будет видна таблица с подписками всех ваших клиентов. Выберите значок Редактировать \(перо и бумага\) справа от клиента:

![](../../.gitbook/assets/editsub.jpg)

{% hint style="success" %}
Вы можете изменить товары, которые заказывает клиент через подписку, их предпочтительные способы доставки и оплаты, и даты начала/окончания их подписки.
{% endhint %}

{% hint style="danger" %}
Вы не можете изменить расписание подписки клиента. Вместо этого необходимо заново создать подписку в новом предпочтительном расписании, а старую версию удалить.
{% endhint %}

### Изменить один конкретный заказ

Если вы хотите изменить один предстоящий заказ в подписке, вы можете нажать на номер в столбце _**заказов**_ клиентов.

Это покажет все предстоящие заказы в расписании и вы сможете редактировать конкретный заказ.

![](../../.gitbook/assets/edit-single-subscription-order.bin)

### Удаление подписки

Чтобы удалить подписку для клиента, который больше не желает регулярно получать от вас товар, нажмите кнопку с **крестиком** справа от таблицы. Это предотвратит создание любых будущих подписок и навсегда удалит эту подписку.

![](../../.gitbook/assets/cancelsub.jpg)

{% hint style="warning" %}
Если вы удалите подписку во время открытого цикла заказа, вас спросят, хотите ли вы сохранить открытый заказ клиента или же он хочет удалить текущий заказ.
{% endhint %}

### Pause a subscription

A customer may want to pause their order while on holiday for instance. In this case, click on the **pause** button \(two vertical lines\) to the right hand side of the subscriptions table. This will prevent all future orders in the subscription from being generated, until it is activated again.

![](../../.gitbook/assets/pausesub.jpg)

To un-pause \(re-activate\) a subscription, click on the **play** \(arrow\) button.

{% hint style="warning" %}
If you pause a subscription while an order cycle is still open, you'll be asked whether you'd like to keep the current order or not.

Subscriptions re-activated in the middle of an open order cycle will generate orders immediately.
{% endhint %}

## How are subscriptions processed?

You have set up a subscription for a customer. What happens now, each time an order cycle opens and closes?

### **Order Cycle belonging to the subscription schedule opens:**

* Your customer's order will be created immediately.  They will receive an email notifying them of this.
* Stock levels of products ordered by the subscription will be deducted accordingly at this time.
* An email will be sent to the [manager of the enterprise](../enterprise-profile/enterprise-settings.md#users) coordinating the order cycle concerned summarising how many subscription have been placed, and how many had issues \(e.g. insufficient stock\). 
* If your enterprise is configured such that 'Orders can be changed/canceled while an order cycle is open' \(see [here](subscriptions-configuration.md#activate-subscriptions)\) then customers with a subscription generated order can edit or cancel.

{% hint style="info" %}
Note, if you create a subscription while there's an open order cycle in the schedule, _an order will be immediately created_ for that subscriber.
{% endhint %}

### **The Order Cycle Closes**

* When the Order cycle closes the subscription orders will be _confirmed_.  Customers will be sent an _order confirmation email_.
* Customers who opted to pay for their subscription by Stripe will have their credit/debit card debited at this point.
* An email will be sent to the [manager of the enterprise](../enterprise-profile/enterprise-settings.md#users) coordinating the order cycle concerned confirming how many subscription have been processed. It will also detail possible errors \(eg. a credit card that couldn't be billed\).

### Planning for future subscriptions

There are several ways in which you may opt to plan future order cycles for your enterprise, now that you offer customers the option of a regular automated subscription order:

* Create all order cycles for the season in advance. A quick way of doing this is to copy an order cycle and modify open/closing dates and name to span the period of time desired.  Add order cycles to the subscription schedules as desired.

{% hint style="info" %}
If you set up lots of order cycles in advance, be sure to check with your suppliers about seasonal availability of items!
{% endhint %}

* Create order cycles on a weekly \(or monthly\) basis. On creation, make sure you also add it to the relevant subscription schedule.

{% hint style="success" %}
Tips:

* You may like to promote the fact you offer subscriptions. This may attract potential customers to purchase items from your enterprise. Veg Box schemes are very popular and can be replicated using the subscription functionality.
* If you notice a number of customers order the same items regularly then offering them the option of an automated order \(subscription\) might be greatly appreciated.
{% endhint %}

