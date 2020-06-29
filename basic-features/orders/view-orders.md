# Просмотр Заказов

В интерфейсе администратора есть два места, где можно просматривать и изменять заказы \(при необходимости\): сама страница [Заказов](view-orders.md#listing-orders) и страница [Пакетное Управление Заказами](view-orders.md#bulk-order-management).  
Особенности обеих этих страниц обсуждаются ниже.

## Список заказов

На странице списка заказов отображается список всех заказов, размещенных в вашем магазине \(ах\). Отсюда вы можете получить доступ к деталям отдельных заказов, редактировать заказы и отслеживать статус их оплаты и доставки. Подробнее о том, как создать новый заказ вручную для вашего клиента, смотрите [здесь](create-orders-manually.md).

На странице есть фильтры, которые позволяют вам выбирать, какие заказы вы хотите просмотреть. Вы можете фильтровать по дате, статусу или электронной почте и имени клиента.

![](../../.gitbook/assets/listingorders1new.jpg)

**Дистрибьютор**: это предприятие, через магазин которого был сделан заказ.

**Завершен в**: Это дата размещения заказа.

**Номер**: Это произвольно назначенный номер заказа. Символ восклицательного знака со словом 'Примечание' слева от него покажет, включил ли клиент комментарий при оформлении заказа. Наведите курсор на восклицательный знак, чтобы просмотреть комментарий.

**Статус:**

* Завершен - клиент закончил оформлять заказ
* Отменен - если администратор редактирует заказ и решает 'отменить его'
* Корзина - клиент находится в процессе покупки, но еще не оформил заказ

**Статус Оплаты:**

* Баланс - если это наличные или банковский перевод, то по умолчанию заказ будет 'Задолжность' до тех пор, пока администраторы предприятия-дистрибьютора вручную не отметят, что платеж получен, при этом указать, что состояние платежа изменится на 'Оплачен'.

![](../../.gitbook/assets/balancedue.jpg)

* Оплачен - Для автоматических платежей \(например, PayPal\) портал оплаты автоматически помечает заказ как 'оплачен' после его обработки. Неавтоматические платежи \(наличные, банковский перевод и т.п.\) также будут помечены как 'оплачен' при обновлении вручную. 
* Кредит- Если кто-то оплатил свой заказ, но затем вы изменили его и удалили товар, стоимость этого товара становится 'кредитом'.

![](../../.gitbook/assets/creditowed.jpg)

**Статус доставки:**

* В ожидании - если состояние платежа равно 'задолжность', то состояние доставки будет в состоянии ожидания, это означает, что до получения оплаты доставка не должна выполняться.
* Готово - когда платеж получен \(оплачен или имеет кредитный статус\), состояние доставки становится 'готово'.
* Отправлен - после доставки или сбора заказ может быть обновлен вручную менеджером магазина/центра \(редактировать заказ\), так что состояние доставки становится 'Отправлен'.

{% hint style="warning" %}
Вы можете ТОЛЬКО вручную обновить заказ до 'Отправлен', если состояние платежа 'Оплачен' или «Кредит принадлежит»  
You can ONLY manually update an order to 'Shipped' if the payment state is 'Paid' or 'Credit Owed'
{% endhint %}

**Customer email:**The customer’s contact email. A full list of customer emails can be downloaded in the ‘mailing list’[report](../reports.md).

**Total:**The total value of the customer’s order

### **Changing the payment and shipping state of an order**

On the right hand side of the listing view you can update the payment/shipping state of an order.

Click on the tick icon to indicate that payment has been received \(this records full payments only\).

![Update to Paid icon](../../.gitbook/assets/tick%20%281%29.png)

Click on the road icon to indicate that the order has been shipped.

![Update to Shipped icon](../../.gitbook/assets/shipped.png)

{% hint style="info" %}
The payment and shipping status of an order can also be updated when editing the order \(see below\).
{% endhint %}

{% hint style="danger" %}
When a shop or hub manager updates the 'Shipment state' to 'shipped' _**this will automatically send the customer an email**_ to say that their products have been shipped, irrespective of the shipping method. Hence it can cause confusion for orders due to be collected \(rather than shipped\).  
Another source of potential confusion to be aware of is when customers pay for an order on collection. Updating the payment \(and then shipping\) status of the order after the goods have been collected will send an email to the customer, even though they have their goods in practice.
{% endhint %}

### **Editing an order**

To the right of an order you will see a pen and paper icon. Click on this to access the order management page where you can edit, modify and cancel:

![](../../.gitbook/assets/edit-order.png)

You can also access full information concerning an order by clicking on the order number \(fourth column of the table\).

This is what the order management page looks like:

![](../../.gitbook/assets/editorder.jpg)

#### **Adding and removing products from an order**

You can add a product to the order by selecting the variant you require from a drop down list of those available \(at least 3 letters must be typed in to the field box 'Select Variant' for list of options to appear\).  
To remove a product from an order click the rubbish bin icon on the right hand side of the product.  
You can also change the quantity of each item ordered. Remember to click the **update and recalculate fees** button to save changes \(this will also update enterprise, shipping and payment method fees accordingly, where appropriate\).

**Additional options available under 'Actions'**

![](../../.gitbook/assets/orderactions.jpg)

* **Resend Confirmation**: If you have edited a customer's order, you may wish to resend them an updated order confirmation email.
* **Send Invoice**: This will automatically send the customer an invoice \(in .pdf format\) by email.

![](../../.gitbook/assets/invoicenew.jpg)

{% hint style="danger" %}
Please check regional regulations regarding the information legally required to be on an invoice. Currently our invoices are not compliant to French law. Invoices for enterprises which are registered for VAT are not compliant under UK law.  
We hope to bring about updates to correct these aspects. In the meantime you may wish to invoice through a [complementary software package](../../complementary-tools-software/).
{% endhint %}

* Print Invoice: This will generate the invoice in the form of a pdf for printing.
* Cancel Order: Cancel the order

#### **View customer details**

Customer information \(email, billing, shipping addresses and phone numbers\) are accessible from the menu on the right of the page:

![](../../.gitbook/assets/ordermenu.jpg)

#### **Modify an Order**

Click on 'Adjustments' in the right hand menu \(screen shot above\). On this page you can add or subtract from the order total by selecting the **+ New Adjustment button**.

![](../../.gitbook/assets/orderadjust.jpg)

You may wish to use this functionality to:

* grant a discount on an order if a product is damaged
* deduct credit owed to the customer from their total balance
* refund a customer \(for more information about Refunds visit [here](refund-payments.md).\)

#### Record Partial Payment

Visit the 'Payments' page from the right hand menu in screen shot above to record partial payments.

### Batch Print Invoices

To save time you can print multiple invoices at once \(rather than visiting each order in turn and selecting Actions-&gt; Print Invoice\).  
On the Listing Orders page check the box to the left of orders for which you would like to send an invoice. You can increase the number of orders per page from 15 to 100 and select all at once, if desired.  
Then click 'Print Invoices' button to the top right of the table:

![batch printing invoices](../../.gitbook/assets/batchprintinvoice.jpg)

A Loading page will pop up while the invoices are generated. On completion you will be able to view \(and download\) a file containing all the invoices for the orders selected:

![](../../.gitbook/assets/compileinvoice.jpg)

## Bulk order management

We have learned above that the [Listing Orders](view-orders.md#listing-orders) tab presents a table of the **orders per customer**. This page, on the other hand, details all the products that were purchased in your orders.  
This functionality is useful for modifying multiple orders at once that may contain the same product \(quantity change, product out of stock etc\). The page looks like:

![](../../.gitbook/assets/bom3.jpg)

**Start/End Date:** You can filter to display all orders that were placed within a given window of time.

**Producer:** You can filter for a given producer. This can narrow down the display, if you’re only interested in one product, supplied by one producer.

**Shop:** You can filter according to the shop at which the order was placed.

**Order Cycle:** Perhaps the most useful filter, the order cycle filter, will display only those orders which were placed within a selected order cycle.

**Quick Search:** Before or after applying filters, you can narrow your search down even further by searching for a key word. This could be a name, product, hub, producer, date, order number…

**Actions:** You can select the check boxes of multiple orders \(left hand column\), to perform the same function to all of them, such as delete.

**Columns:** You can select which fields you do or do not want to be displayed in the table:

![](../../.gitbook/assets/bomcol.jpg)

{% hint style="success" %}
Rows \('Name', 'Producer', 'Product: Unit'\) can be sorted according to their content by clicking on the relevant column heading: one click for sorting A-Z, two clicks for the reverse \(Z-A\).
{% endhint %}

{% hint style="warning" %}
The **Price** column indicates price of an item including tax but excluding fees \(enterprise, shipping or payment method fees\). Fees are recalculated each time an order is modified.
{% endhint %}

### Examples of using Bulk Order Management:

#### Example 1: You have a stock shortage, and must reduce customer order quantities for a certain product.

_In your current order cycle, customers placed orders for 20kg of tomatoes. Unfortunately there was a storm, and you were only able to harvest 10kg. You need to identify all customers who ordered tomatoes, and half their orders for tomatoes._

This can be done in bulk order management, as follows:

1. Filter according to the date range, or current order cycle.
2. Search for ‘tomatoes’. All orders for tomatoes within the date range/order cycle you selected will now display.
3. Click on the product ‘Tomatoes’ in the Product:Unit column.
4. A box will appear at the top of the page, showing the total quantity ordered \(across the date range/order cycle you’ve selected\).

![](../../.gitbook/assets/bomtom1.jpg)

You can then adjust the quantity \(or delete products\) of each unique order in the Quantity column. The Total Quantity Ordered in the box at the top will update automatically as you adjust orders.

{% hint style="danger" %}
No automated email will be sent to customers after you have adjusted their orders. It is good practice though, to manually do so else the customer may be disappointed on collection/delivery.
{% endhint %}

Here, the amount of tomatoes allocated to each order has been reduced to meet the total available of 10kg:

![](../../.gitbook/assets/bomtom3.jpg)

#### **The ‘Shared Resource’ checkbox**

This checkbox allows you to make adjustments to all variants of the same product at once. For example, you may retail tomatoes in 1kg and 3kg bags. By selecting 'Shared Resource' you will be able to edit the quantities of both variants ordered at once.

![](../../.gitbook/assets/bomtomshared.jpg)

#### Example 2: Updating the final weight of products.

When selling indivisible products such as legs of lamb, or whole pumpkins, you may not know the final weight and price of the product until after the customer has placed their order. \(Read more [here](../products-1/pricing-irregular-items-kg.md).\) You can use Bulk Order Management to update the item’s exact weight once you have the product in front of you.

For the example of a 1kg fish:

1. Filter for the order cycle or date range of interest.
2. Search for the desired product
3. Make the **Weight/Volume** and **Price** columns visible.
4. Enter the actual weight of the fish that each customer will receive in the weight/volume column. The price will automatically recalculate based on this weight.
5. Click update.

![](../../.gitbook/assets/bomfish.jpg)

## A **Customer’s view of their order**

Your customers can view a list of their orders when they login to the OFN, and click on their account \(see below\).

![](../../.gitbook/assets/account-login.png)

Here your customers will be able to see the past orders and payments as well as a running balance at your shop \(and any others on OFN where they have placed an order\).

![](../../.gitbook/assets/orders.png)

{% hint style="warning" %}
For non-automated payments \(cash, cheque, bank transfer etc\) the customer's 'balance' will display as 'owing' until you have [manually recorded the payment](view-orders.md#editing-an-order).  
_**If payments are not updated regularly by a shop/hub manager this can be confusing to your customers as they may have in fact paid but it won't be documented above.**_
{% endhint %}

