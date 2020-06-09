# Инструмент товарной номенклатуры

## Введение

"Инвентаризация" дает предприятиям повышенный контроль и гибкость в управлении своими товарами, если они этого требуют. Эта функция будет в основном интересна Центрам и менеджерам Центра.

С помощью "Инвентаризации" Центр A может изменять цену и уровень запасов товаров, на которые он имеет разрешение для розничной продажи. Эта функция может также позволить Центру A делать выбор только определенных товаров от его поставщиков, доступных для продажи на его витрине, но не всего ассортимента продукции. Все это можно сделать без изменения мастер-копии товаров. Следовательно, если оба Центра A и B снабжают одинаковыми товарами, то с помощью инструмента инвентаризации Центр A может изменять цену и другую основную информацию о товарах, которые он продает, не влияя на Центр B.

## Настройки профиля для Товарной номенклатуры

Чтобы получить доступ к инвентарю, перейдите в раздел 'Предприятия' \(в синем горизонтальном меню\), а затем 'Настройки'. В строке меню слева выберите 'Настройка товарной номенклатуры'.

![](../../.gitbook/assets/inventory-settings.png)

Есть две опции:

* **Новые товары могут быть размещены в моем магазине \(рекомендуется\):** Продукты вашего поставщика могут быть добавлены в ваш интернет-магазин _без необходимости предварительно добавлять их в ваш магазин / центр_. Когда вы создаете цикл заказа, _все товары_ от выбранных производителей будут доступны для вас, чтобы добавить его к 'входящей' части \(цикл заказа\). Это опция по умолчанию и рекомендуется для центров, которые не хотят изменять цену или уровень запасов товаров, которые они продают в розницу

{% hint style="warning" %}
БУДЬТЕ ОСТОРОЖНЫ - если вы сохраняете настройки своей товарной номенклатуры по умолчанию в режиме 'выключен', но в то же время загружаете товары в инвентарную номенклатуру своего Центра и изменяете их цены или уровни запасов, то измененная информация будет отображаться на витрине вашего магазина, а не в мастер копии.
{% endhint %}

* **Новые товары должны быть добавлены в мою товарную номенклатуру, прежде чем они могут быть помещены в мою витрину:** Когда вы создаете цикл заказа, только те продукты, которые вы ранее добавили в инвентарную номенклатуру Центра, будут видны для выбора во 'входящей' части цикла заказа.

## Просмотр Товарной номенклатуры вашего Магазина/Центра

Выберите меню 'Товары' в верхней части панели администратора, а затем нажмите 'Товарная Номенклатура' в зеленом подменю. Если вы управляете несколькими предприятиями, вам будет предложено выбрать одно, так как каждая товарная номенклатура управляется независимо.

![](../../.gitbook/assets/inventory1.jpg)

Если ваши поставщики добавляли новые товары между каждым посещением товарной номенклатуры вашего магазина / центра, вы увидите следующее сообщение:

![](../../.gitbook/assets/new-products-alert.png)

Пока вы не добавите эти товары в товарную номенклатуру, они будут оставаться в категории '**Новые товары**' и невидимы для выбора при создании цикла заказа. Нажав '**Просмотреть**', вы будете перенаправлены на список новых товаров.

## Просмотр Новых Товаров

Новые товары могут быть **Добавлены** в список товарной номенклатуры или **Скрыты**. Если в списке есть товар, для которого вы хотели бы переопределить детали или применить повторяющийся уровень запасов, вам нужно **добавить** его в свой список товарной номенклатуры. Если в вашем магазине есть товар, который вы никогда не хотите продавать или, по крайней мере, не хотите продавать в ближайшем будущем, вы можете **скрыть** его \(см. Раздел '**Скрытые товары'** ниже\).

![](../../.gitbook/assets/new-products.png)

{% hint style="info" %}
Помните, что если ваши Настройки Товарной Номенклатуры установлены так, что 'Новые товары должны быть добавлены в мою товарную номенклатуру, прежде чем они могут быть помещены в мою витрину', все товары, которые вы оставите в списке новых товаров, будут фактически скрыты. Если для вашего параметра 'Настройки Товарной Номенклатуры' выбрано 'новые товары могут быть размещены в моей витрине', тогда товары из вашего списка новых товаров будут отображаться в вашем цикле заказов.
{% endhint %}

## Управление Продуктами Вашей Товарной Номенклатуры

В вашем списке продуктов товарной номенклатуры вы можете переопределить информацию о товарах, настроить сброс уровня запасов и скрыть товары.

![](../../.gitbook/assets/viewing-inventory-settings.png)

С помощью кнопки столбцов в правой части таблицы вы можете выбрать, какие настройки вы хотели бы видеть и изменять.

![](../../.gitbook/assets/columns-1.png)

### Измените SKU, цены и уровень запасов для товаров в вашем магазине

Any changes you make here will be visible on your shop and will hence override details set by the supplier. You can modify the following fields:

* **SKU** – if you wish to use an alternative SKU \(reference number\) for a product, you can over-ride the producer’s SKU here by typing in an alternative.
* **Price** – You can set a different price to show in your shop. Keep in mind the units of the product will remain the same. Hence if the product is priced per kg then you can only modify its cost per kg and not change it to a fixed cost per item.
* **In Stock** – If your stock of this product differs from the available stock offered by the producers, you can indicate your stock. Your products will no longer be visible in the shop once the inventory stock level reaches zero.

{% hint style="info" %}
This might be handy if you receive a bulk purchase of say 50 items per month and need to keep track of their sales before the next delivery.
{% endhint %}

* **Unlimited?** – You can select whether to inherit producer stock levels \(in which case the number in the 'in stock' column will remain grey\), to have unlimited stock 'yes' \(hence the item will never run out and will always be available, if added to an active order cycle\) or to define your own stock levels 'no' \(in which case the number in the 'in stock' column will be on a white background\).

![](../../.gitbook/assets/inventorystock.jpg)

Refresh yourself about 'in stock' and 'unlimited' [here](products.md#adding-products).

{% hint style="warning" %}
It is not possible to alter product name, properties, description or image.
{% endhint %}

### Enable Stock Reset?

The **enable stock level reset** column allows you to reset the 'In Stock' amount to a default value, **\*\*for example at the start of each new order cycle. The** default amount\*\* is the number entered in this column next to the check box. The checkbox allows you to select only those items that you want to reset at any give time.

To reset the default stock for these products, click 'Actions' at the top left of the inventory table and then 'Reset stock levels to defaults'. Only products for which the enable stock reset box has been checked will be affected by this action.

![](../../.gitbook/assets/inventorystockreset.jpg)

> In this example the default stock level of baked beans is 5. There are currently 2 left in stock. If the user, at the beginning of an order cycle wishes to reset to 5 then they must click on 'Reset stock levels to defaults' under 'Actions'

{% hint style="info" %}
This is a useful feature for hubs who may receive deliveries of specific products once a month or on a regular schedule.
{% endhint %}

### Inherit?

If you have not changed any of the values in the Inventory table for a product, the check box "inherit?" will be, by default, checked. This means that the information entered by the producer and visible in grey will be displayed on your shopfront.

![](../../.gitbook/assets/inventoryinherit.jpg)

By modifying one or more of the fields, this check box will be automatically de-selected. To reset values \(price, stock, SKU etc\) to the producer's master copy values, you can re-select this box at any time.

### Hide

As in the **New Products** list, you can also **hide** products from your **Inventory List**. Clicking on the hide button will move the product to your **Hidden Products** list. If you have your inventory profile set up as '**New products must be added to my inventory before they can be added to my shopfront'** \(see [here](inventory-tool.md#profile-settings-for-the-inventory)\) then the product you just hid will no longer be available for selection in your hub's order cycle and thus will not be visible on your shopfront.

## Hidden Products

This is a list of all the products you have chosen to hide:

![](../../.gitbook/assets/hidden-products.png)

When viewing your list of hidden products you can choose to make them visible once more by clicking the '**Add**' button to the right of the item.

![](../../.gitbook/assets/inventoryhidden.jpg)

## Inventory and Order Cycles

When setting up order cycles you can on a case by case basis choose between selecting from all available products or only those which are in your shop/hub inventory.

This is controlled by visiting 'Advanced Settings' \(top right of order cycle page\):

![](../../.gitbook/assets/advanced-oc-settings.png)

This option has the same effect as changing our enterprise [profile settings for your inventory](inventory-tool.md#profile-settings-for-the-inventory), but unlike the latter it applies only to the order cycle in question.

{% hint style="danger" %}
After making any changes always remember to click 'Update' or 'Save' before moving on!
{% endhint %}

