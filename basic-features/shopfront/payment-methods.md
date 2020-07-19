# Методы Оплаты

{% hint style="danger" %}
Вы **должны** создать хотя бы один способ оплаты, прежде чем открыть свой магазин.
{% endhint %}

Прежде чем читать дальше, вам может понадобиться краткая демонстрация того, как настроить свой первый способ оплаты:

![](../../.gitbook/assets/paymentmethod.gif)

## Настройка Спопоба Оплаты

* Перейдите на страницу **Способы оплаты**, нажав **Предприятия** в синем горизонтальном меню, а затем нажмите **Настройки** рядом с вашим предприятием. Страница **Способы оплаты** находится в меню слева.
* Нажмите **Создать новый способ оплаты +**. Вы будете перенаправлены на такую страницу:

![](../../.gitbook/assets/paymentmethod1%20%281%29.jpg)

* Отметьте свое предприятие в поле с правой стороны страницы под названием Центры. Это указывает, к какому предприятию будет применяться способ оплаты, который вы собираетесь создать. Вы можете выбрать более одного предприятия.
* **Название**: выберите название для этого способа оплаты. \(например, 'Оплатить с помощью кредитной карты, используя Paypal'\). Это имя отображается при оформлении заказа и в электронном письме с подтверждением заказа.

![](../../.gitbook/assets/paymentmethod2.jpg)

* **Описание**: предоставьте дополнительную информацию о способе оплаты. Например, для банковского перевода вы можете ввести банковские реквизиты счета в это поле, на который клиент должен выполнить оплату. Это описание отображается при оформлении заказа и в письмах с подтверждением заказа.
* **Активно**: выберите, будет ли данный способ оплаты видимым и доступным или нет.
* **Метки**: используйте правила меток, если вы хотите сделать определенные способы оплаты доступными/недоступными для определенных клиентов \(например, вы можете разрешить оплату оптовым клиентам только безналичным расчетом, но "заставить" внутренних клиентов платить с помощью кредитной карты или PayPal.\). Для получения дополнительной информации читайте[ здесь](customer-management-and-conditional-displays-prices/).
* **Платежные системы**: выберите вариант, который соответствует способу оплаты, который вы создаете. Есть пять вариантов:
  * Наличные/Банковский перевод. \(Наличными или банковским переводом. Эти платежи не проходят через портал онлайн-платежей и не включают автоматическую проверку\) 
  * MasterCard Интернет Шлюз \(MIGS\) 
  * PayPal Express
  * [Pin Payments](https://pinpayments.com/) \(Только Австралия\). Недоступно для России
  * Stripe. Недоступно для России
* **Калькулятор**: выберите, каким образом любые платежи, связанные с методом оплаты, будут применяться к заказу. Обратите внимание, что сбор за метод оплаты может быть установлена в ноль. См. ниже для получения дополнительной информации о [Сборы Метода Оплаты](payment-methods.md#fee-calculators)

При нажатии кнопки Создать будет создан способ оплаты и у вас появятся новые поля для определения комиссий за способ оплаты. Видимые поля зависят от того, какой Калькулятор вы выбрали.

{% hint style="info" %}
Если вы измените поле Калькулятор в поле сборы Способа оплаты, вы должны сначала сохранить изменения \(Обновить\), чтобы новые связанные поля стали видимыми.
{% endhint %}

## Интегрированные Платежные Системы

Для Paypal, MasterCard ниже дополнительные инструкции.

{% tabs %}
{% tab title="Paypal" %}
Чтобы настроить способ оплаты PayPal, вам понадобится коммерческая или торговая учетная запись PayPal. Вы можете создать его[ здесь](https://www.paypal.com/au/webapps/mpp/merchant). После этого вы можете настроить 'API доступ' в PayPal, что позволит ОСП напрямую связывать клиентов с вашей учетной записью PayPal.

1. Войдите в ваш аккаунт PayPal
2. Под именем вашей учетной записи в правом верхнем углу есть раскрывающееся меню с 'Настройки учетной записи'

![](../../.gitbook/assets/paypalmay1.jpg)

1. Выберите 'Update' из API Access

![](../../.gitbook/assets/paypalmay2.jpg)

1. Выберите 'Manage API credentials' из пользовательского варианта оформления заказа.

![](../../.gitbook/assets/paypalmay3.jpg)

Отсюда вы сможете получить доступ к своему имени пользователя API, паролю и подписи.

![](../../.gitbook/assets/paypalmay4.jpg)

**В ОСП** убедитесь, что вы вошли как пользователь Предприятия. Перейдите на Предприятие и создайте Способ Оплаты. Выберите PayPal и введите данные с сайта PayPal.

**Server:** Измените поле ‘server’ на ‘live’ – это чувствительно к регистру.

**Login:** Введите the API Username.

**Password:** Введите API Password.

**Signature:** Введите API Signature в этом поле.

![](../../.gitbook/assets/paypal3.jpg)

**Solution:** Solution определяет, нужен ли пользователю аккаунт PayPal для оформления заказа.

Введите “Mark” если выхотите, чтобы пользователи имели paypal аккаунт или “Sole” если они могут оформлять заказ не имея Paypal аккаунта \(с кредитной картой\).

**Landing Page:** Вы можете выбрать, какую страницу показывать клиентам, после того как они будут перенаправлены на PayPal.

Введите "Login", чтобы направить клиента к форме входа в PayPal \(если выше вы выбрали "Mark"\). Или введите "Billing", чтобы показать клиентам форму, в которой они могут ввести данные своей кредитной карты и возможно, зарегистрировать учетную запись PayPal \(если выше вы выбрали "Sole"\).
{% endtab %}

{% tab title="MIGS" %}
MasterCard Интернет Шлюз \(MIGS\)

Настройка этой услуги должна быть сделана через ваш банк. Пока что это было проверено с Бендиго Банком.
{% endtab %}

{% tab title="Stripe" %}
[Stripe](https://stripe.com/au) is an online payment platform similar to Paypal. It will allow you to accept credit card payments from your customers. Stripe is a global platform, but is only available on certain OFN instances. Contact your [local OFN team](https://openfoodnetwork.org/ofn-local/) to see whether it’s available on your OFN.

#### Why use Stripe?

Stripe is simple to setup for shop owners and is reasonably priced. The fees charged by Stripe vary in each country; [Australia](https://stripe.com/au/pricing), [Canada](https://stripe.com/ca/pricing), [France](https://stripe.com/fr/pricing), [UK](https://stripe.com/gb/pricing), [USA](https://stripe.com/us/pricing).

Stripe is also easy for customers to use. Unlike Paypal, when the customer checks out, they don’t need to login with Paypal to place their order, rather they just need to enter their card details and then complete their order.

Stripe is the recommended payment method for shops who wish to use [**subscriptions** ](../subscriptions/)on OFN, as Stripe allows customers to give permission to a shop to automatically bill their credit card for subscription orders. This isn’t offered by Paypal, Pin or MIGS payment platforms.

#### Setup

**Connect with Stripe**

Before you can setup a payment method that uses Stripe, you’ll need to Connect with Stripe. To do this, click on the ‘Connect with Stripe’ button.

![](../../.gitbook/assets/connect-with-stripe.png)

You’ll be taken to a form to fill in your details. If you already have an account with Stripe, you can login, if not, fill in the form to create a Stripe account.

The information you’ll be asked for includes: country, a description of your business, your Business address and ABN, your personal details and your bank account \(where received payments will be deposited\).

**Create a New Payment Method**

Once you’ve connected with Stripe, you can then create a payment method which will work with your connected account.

Treat the **Name**, **Description**, **Active** and **Tags** fields as you would with any payment method.

**Provider:** Select Stripe.

Once you select Stripe, ‘Provider Settings’ will be shown.

**Stripe Account Owner:**

Select the enterprise that has a Stripe account connected.

If you select an enterprise that is not Connected to Stripe \(see above\) , you will get the error shown below. Either click ‘Connect One’ or return to your Payment Methods tab to Connect with Stripe. See instructions above.

![](../../.gitbook/assets/stripe-connect.png)

#### Stripe Payments for Customers

When customers checkout in a shop and pay with a Stripe payment method, they’ll have the options of selecting a tickbox allowing their credit card details to be stored against their account \(if they are logged in\).

Customer can also save a credit card in their Account, or delete saved ones.

![](../../.gitbook/assets/add-card.png)

When the customer next shops with an OFN shop offering Stripe as a payment method, they’ll be able to select from their saved credit cards.

**Viewing and redeeming your payments via Stripe**

When a customer pays for their order with Stripe, the funds \(minus Stripe's fees\) will go to your stripe account. Depending on your setting in Stripe the funds will be automatically transferred to your chosen bank account periodically.

**Taking further payment**

If you need to take additional payment from a customer because they have further balance due, you can create an invoice in Stripe. The customer will get sent an email asking for them to pay with Credit/Debit card. This won't be communicated to OFN, so you'll need to mark the payment off manually.

![](../../.gitbook/assets/image%20%2831%29.png)
{% endtab %}

{% tab title="Pin Payments" %}
For Pin Payments you only require your API key. You need to set up an account with Pin Payments first, and can get a discount by signing up as an OFN member \([https://pinpayments.com/partners/openfoodnetwork/signup](https://pinpayments.com/partners/openfoodnetwork/signup)\)

**API Key:**Enter your “Live Secret API Key’ here – you can find this in your PinPayments account \(see below\). First from your account, select API Keys. Then once you have generated an API key, copy the ‘Live Secret API Key’ and paste it into the API key field in OFN.

![](../../.gitbook/assets/api-keys.png)

![](../../.gitbook/assets/api-2.png)

**Server:**Type ‘live’ – this is case sensitive.
{% endtab %}
{% endtabs %}

## Сборы Метода Оплаты

![](../../.gitbook/assets/fee-calculators.png)

Вы можете прикрепить сборы к способам оплаты. Чаще всего это используется, чтобы возложить оплату комиссии платежного портала на клиента. Например, вы можете взимать с клиента плату за удобство оплаты через PayPal, чтобы покрыть плату, взимаемую PayPal.

{% hint style="danger" %}
Сбор Метода Оплаты не включает налог \(НДС\)
{% endhint %}

### Калькуляторы Сбора

**Фиксированный Процент** - эта комиссия взимается в процентах от общей суммы, потраченной в заказе.

**Фиксированный Процент \(за заказ\)** - этот сбор применяется в качестве стандартного сбора для всех заказов, независимо от размера заказа.

**Гибкая Ставка** - этот калькулятор сборов особенно полезен, если вы хотите поощрять клиентов размещать крупные заказы: стоимость доставки может быть уменьшена или равна нулю при достижении порогового количества товаров.

* 'Стоимость первого товара': сбор за первый товар в заказе.
* 'Дополнительная стоимость товара': сбор взимаемая за товары, не входящие в первую позицию.
* 'Максимальное количество позиций': максимальное количество предметов, на которые будет взиматься сбор. За товары, приобретенные сверх этой суммы, плата не взимается.

![](../../.gitbook/assets/paymentflex.jpg)

> Например: 'Стоимость первого товара' установлена в 0.20руб, 'Дополнительная стоимость товара' равна 0.10руб. и 'Максимальное количество позиций' равно 3, тогда клиент, покупающий 5 позиций заплатит сбор/комиссию 0.40руб\(0.20руб за первую позицию, по 0.10руб за позиции два и три и 0.00руб за позиции четыре и пять\).

**Единая ставка \(за единицу\)** - эта сумма является постоянной и применяется к товарам, перечисленным как 'предметы'. \(Не применяется к товарам, продаваемым по весу или объему. Следовательно, с клиента не взимается соответствующая стоимость доставки, например, покупая рис по кг\).

**Ценовой пакет** - это гибкий метод оплаты за доставку, который определяется _общей суммой продаж_, а не количеством приобретенных товаров \(Гибкая Ставка выше\)

* 'Минимальная сумма': Денежное значение порога между Обычной стоимостью доставки и стоимостью Скидки на доставку.
* 'Обычная сумма': Стоимость доставки применяется к продажам ниже порогового значения, указанного в 'Минимальной сумме'.
* ‘Сумма скидки’: стоимость доставки применяется к продажам, превышающим порог, указанный в 'Минимальной сумме'.

![](../../.gitbook/assets/paymentpc.jpg)

{% hint style="info" %}
Порталы оплаты часто взимают с компаний фиксированную сумму за транзакцию плюс небольшой % от общей стоимости. Таким образом, комиссионные, с которыми сталкиваются Центр или Магазин, для клиентов, которые покупают одну и ту же общую сумму в нескольких небольших покупках будут выше, чем если бы покупатель делал все свои покупки одновременно.

Калькуляторы Гибких Тарифов и Ценовых Пакетов, применяемые к сбору за метод оплаты, могут оказаться полезными для противодействия этому балансу.
{% endhint %}

## Возвраты

Выдача и управление возвратами зависит от того, как клиент изначально оплатил свой заказ. Более подробную информацию можно найти [здесь](../orders/refund-payments.md).

