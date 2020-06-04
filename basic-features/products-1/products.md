# Добавить товары

Вы можете добавлять товары в свой каталог по одному \(подробности ниже\) или путем [массового испорта](product-and-inventory-import.md), если у вас есть все необходимые данные в .csv файле.

## Добавление товаров

После входа в Панель Администратора выберите Товары в горизонтальном синем меню и нажмите +Новый Товар.

![](../../.gitbook/assets/add-new-product.png)

Вы попадете на страницу Новый Товар.

![](../../.gitbook/assets/new-product2.png)

**Поставщик**

Выберите предприятие, которое производит и поставляет продукцию.

{% hint style="info" %}
Если вы производитель, это будете вы. Если вы являетесь центром, помните, что вы сможете добавлять товары только в созданные вами профили производителей или если вам предоставлено разрешение на управление товарами профилей производителей. Смотрите здесь для получения дополнительной информации.. Для получения дополнительной информации, смотрите [тут](../enterprise-profile/create-or-connect-with-your-supplying-producers.md).
{% endhint %}

**Название товара**: это название товара, отображаемое на витрине магазина.

**Единица измерения**: Выберите единицу, в которой продается товар \(г, кг, л … или предмет \(связка, сумка, пакет\)\)

Если вы выберете 'г', а затем введете 1000, товар для покупателя будет отображаться как 1кг. Имейте в виду, что некоторые единицы измерения будут влиять на работу определенных [сборов предприятия](../shopfront/enterprise-fees.md).

Например, [фиксированный сбор по весу](../shopfront/enterprise-fees.md#fee-calculators) может применяться только к продуктам с единицами 'кг'. В этом случае вы можете ввести нецелые числа единиц, например 0.2кг и продукт будет отображаться как 200г, но будет записан в 'кг' в отчетах и при расчете цен.

**Значение**: введите значение единиц, в которых продается этот товар \(например, если он продается за 100г, введите здесь '100' и выберите 'г' для 'единиц' или, если он продается в виде букетов цветов, введите '1' и 'единицы = штук'.

**Показывать как**: Это поле автоматически показывает, как будут отображаться поля единиц измерения и значения, после того как вы заполните поля единиц измерения и значения. \(т.е. единицы измерения = кг, значение = 2, показывать как = 2 кг\)

{% hint style="info" %}
Примечание: Если вы выбрали 'элементы' в качестве единицы измерения, поле 'Показывать как' изменится на 'имя элемента'. Заполните это типом предмета. \(то есть баночка, бутылка или гроздь\)
{% endhint %}

**Категория товара**: выберите наиболее подходящую категорию для этого продукта. Назначение категории продукту облегчает клиентам поиск товаров, которые они хотят купить; покупатели могут отфильтровать ваш список товаров по категориям в вашем магазине.

**Цена**: введите цену, упомянутую выше. Обратите внимание, что это базовая цена, взимаемая производителем и сумма, которую они будут получать за каждую покупку. Наценки и сборы \(для администраторов дистрибьюции и т.д.\) добавляются в [Сборах Предприятия](../shopfront/enterprise-fees.md), [Методах Доставки](../shopfront/shipping-methods.md#fee-calculators) и [Методах Оплаты](../shopfront/payment-methods.md#fee-calculators).

{% hint style="info" %}
Если ваше предприятие зарегистрировано для налогообложения или вы решили, что этот продукт облагается налогом, то цена, указанная здесь, **включает Налог**. Если вы решите, что этот продукт не облагается налогом, введенная вами цена будет безналоговой.
{% endhint %}

**В наличии**: укажите, сколько у вас есть в наличии этого товара и готового к продаже.

Используйте это поле, если вы хотите отслеживать уровень запасов в наличии. По мере того, как клиенты размещают заказы, уровень складских запасов снижается, а когда количество на складе достигает нуля, товар больше не будет виден в вашем магазине. Если вы не хотите отслеживать товар таким образом, нажмите 'по запроу'.

**По запросу:** Если вы выберете это поле, это будет означать, что товар всегда доступен. Платформа перестает отслеживать уровни запасов для товаров и вместо этого всегда будет показывать, что товар есть в наличии.

**Изображение**: Загрузить фото этого товара.

{% hint style="success" %}
Мы рекомендуем использовать фотографии хорошего качества в квадратном \(1:1\) форме и крайне желательно реальную фотографию ваших товаров, а не стандартное изображение из Интернете. Это делает продукт более привлекательным для потребителя. Всегда делайте свои фотографии при хорошем освещении.

Если вы используете изображение из Интернета, убедитесь, что оно не имеет авторских прав.
{% endhint %}

**Tax category:** Select the applicable tax category from the drop-down list. Tax \(VAT in the UK\) depends on the nature of the product and the country in which you are retailing in.

{% hint style="danger" %}
Tax will only be collected when enterprises have selected 'charges VAT = yes' under their enterprise settings -&gt; Business Details.
{% endhint %}

**Product description:** Tell your customers a little bit about this product. You might like to include a story about the specific tomato variety, include hyperlinks to any certification it may have etc.

{% hint style="info" %}
Don't forget to click on the "create" or "create and add new" button at the bottom of the page once all mandatory fields have been entered \(those indicated by a red asterisk\).
{% endhint %}

A short demonstration of the steps outlined above:

![](../../.gitbook/assets/productsadd.gif)

When you have finished creating a product, you are redirected to the "products" page where you will find all your products:

![](../../.gitbook/assets/productspage.jpg)

## Listing Similar / variations of a Product

If you are listing a product which comes in a number of different options \(say different sizes or flavours, each of which may or may not have a different price\), it is best to create a ‘variant’ for that product, rather than creating multiple, separate products. Creating product variants is discussed fully on the [next page](product-variants.md).

{% hint style="success" %}
Variants are useful if, for example, you sell lemons singularly as well as in 'packs' of 5. Rather than have two product listings the two options can be available for the same product.
{% endhint %}

If you would like to create a SIMILAR product then you can duplicate products by selecting the double page icon to the right of an item \(red box\). By subsequently selecting the pencil and paper icon \(green box\) the copied product can be edited and the details amended for the second item.

![](../../.gitbook/assets/productspagecopy.jpg)

## Refine product attributes

Using OFN you can add **properties or labels** to your products. This allows customers to find your items when searching for specific criteria \(eg. certified Organic\) and highlights specific qualities your products may have. Find out more [here](product-properties.md).

For tips on how to manage sales of **"irregular" products** such as meat or large vegetables sold in units but costed by weight, please read [here](pricing-irregular-items-kg.md).

Our **Group Buy** tool enables you to manage and organise sales of products in bulk lots. Find out more [here](group-buy-for-bulk-ordering.md).

