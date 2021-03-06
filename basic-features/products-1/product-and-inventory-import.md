---
description: >-
  На этой странице объясняется, как оба производителя могут импортировать
  сведения о товаре, а дистрибьюторы могут настраивать свои складские запасы
  оптом.
---

# Импорт Товара и Товарной Номенклатуры

Инструмент импорта товаров и товарной номенклатуры позволяет загружать файл .csv для добавления и обновления вашего запаса. Это может быть намного быстрее и эффективнее, чем добавление или обновление продуктов один за другим. Для производителей, которые уже регулярно обновляют каталог своей продукции в электронной таблице Excel, это может сэкономить много времени!

Инструмент для импорта товаров и товарной номенклатуры можно найти, щелкнув **Товары** в горизонтальном синем меню и **импорт товара** в зеленом меню.

Существует четыре основных способа использования инструмента:

1. Импорт новых [товаров](./)
2. Обновление информации существующих товаров
3. Импорт товаров в [товарную номенклатуру ](inventory-tool.md)нового магазина/центра 
4. Обновление товаров в товарной номенклатуре магазина/центра

{% hint style="info" %}
Если вам нужна эта функциональность, сообщите об этом [в ОСП](https://openfoodnetwork.ru). Мы приветствуем ваши отзывы.
{% endhint %}

Во всех случаях этот процесс включает в себя загрузку шаблона csv, заполнение полей, а затем загрузку файла csv обратно в ОСП.

{% hint style="warning" %}
**Важное примечание к файлам CSV**: Microsoft Excel не открывает файлы .csv напрямую.  
Если можете, мы рекомендуем скачать бесплатный офисный пакет LibreOffice [https://www.libreoffice.org/download/download/](https://www.libreoffice.org/download/download/)  
С Libre Office Calc, вы сможете очень легко открывать и редактировать CSV и сохранять их в нужном формате кодировки UTF-8.  
Если вы не можете использовать Libre Office, тогда чтобы открыть файл CSV в Microsoft Excel, вам нужно выполнить следующие шаги: [https://support.office.com/en-gb/article/import-or-export-text-txt-or-csv-files-5250ac4c-663c-47ce-937b-339e391393ba](https://support.office.com/en-gb/article/import-or-export-text-txt-or-csv-files-5250ac4c-663c-47ce-937b-339e391393ba)
{% endhint %}

{% hint style="danger" %}
Не все поля могут быть захвачены и загружены/обновлены с помощью этого инструмента. В настоящее время[ Изображения](products.md), [Свойства](product-properties.md) и параметры [Групповой Покупки](group-buy-for-bulk-ordering.md) необходимо загружать вручную для каждого товара.
{% endhint %}

{% hint style="danger" %}
Мы надеемся включить их в будущие разработки.
{% endhint %}

## Импорт Новых Товаров

Используйте эти инструкции, если вы хотите добавить новые товары в профиль производителя.

{% hint style="success" %}
Вы можете одновременно загружать новые товары и обновлять существующие с помощью одной загрузки CSV. Инструкции в этом руководстве разделены для ясности, но вы можете объединить новые новары и обновления существующих в одной электронной таблице.
{% endhint %}

### Подготовка CSV файла для импорта

Сначала загрузите **CSV-файл шаблона списка товаров** со страницы **Импорт товара** и откройте его в Libre Office \(Excel или аналогичный\).

Вы увидите, что шаблон содержит все заголовки столбцов, необходимые для успешного импорта товара. Каждая строка для нового продукта или варианта. Ниже приводится описание того, как заполнять каждый столбец.

{% hint style="danger" %}
Обратите внимание, что все поля чувствительны к регистру. Например. Вы должны использовать _мл_, а не _Мл_ или _Молочные_ продукты, а не _молочные_.
{% endhint %}

| Заголовок Столбца | Обязательный? | Описание | Пример |
| :--- | :--- | :--- | :--- |


| producer | Да | Это имя профиля производителя, которому будет присвоен этот товар | Демо Ферма дяди Вани |
| :--- | :--- | :--- | :--- |


| sku | Нет | SKU код для этого товара | AD001265 |
| :--- | :--- | :--- | :--- |


| name | Да | Имя/название товара | Йогурт |
| :--- | :--- | :--- | :--- |


| display\_name | Нет | Это поле применяется если вы создаете варианты \(см. инструкции ниже\). Если вы не создаете варинт, оставьте это поле пустым. | Малиновый Йогурт |
| :--- | :--- | :--- | :--- |


| category | Да | В какой категории находится этот товар? Доступные категории перечислены на странице Импорта Товара. | Молочка |
| :--- | :--- | :--- | :--- |


| units | Да | Значения веса, объема и количества | 500 |
| :--- | :--- | :--- | :--- |


| unit\_type | Возможно | В каких единицах продается \(г, кг, мл, л\)? Если продается как предмет \(например, связка\), оставьте пустым | г |
| :--- | :--- | :--- | :--- |


| variant\_unit\_name | Возможно | Если товар продается как предмет \(например, буханка, куча, тыква\), напишите здесь тип предмета | Bunch |
| :--- | :--- | :--- | :--- |


| price | Да | Цена товара. Если товар облагается налогом, это должна быть цена с учетом налога. | 3.70 |
| :--- | :--- | :--- | :--- |


<table>
  <thead>
    <tr>
      <th style="text-align:left">
        <p>On_Hand</p>
        <p>(in_stock)</p>
      </th>
      <th style="text-align:left">&#x412;&#x43E;&#x437;&#x43C;&#x43E;&#x436;&#x43D;&#x43E;</th>
      <th style="text-align:left">&#x415;&#x441;&#x43B;&#x438; &#x443; &#x432;&#x430;&#x441; &#x435;&#x441;&#x442;&#x44C;
        &#x43E;&#x433;&#x440;&#x430;&#x43D;&#x438;&#x447;&#x435;&#x43D;&#x43D;&#x44B;&#x439;
        &#x437;&#x430;&#x43F;&#x430;&#x441; &#x434;&#x43B;&#x44F; &#x442;&#x438;&#x43F;&#x430;
        &#x442;&#x43E;&#x432;&#x430;&#x440;&#x430;, &#x443;&#x440;&#x43E;&#x432;&#x435;&#x43D;&#x44C;
        &#x437;&#x430;&#x43F;&#x430;&#x441;&#x430; &#x437;&#x434;&#x435;&#x441;&#x44C;.
        &#x415;&#x441;&#x43B;&#x438; &#x443; &#x432;&#x430;&#x441; &#x435;&#x441;&#x442;&#x44C;
        &#x431;&#x435;&#x441;&#x43A;&#x43E;&#x43D;&#x435;&#x447;&#x43D;&#x44B;&#x439;
        &#x437;&#x430;&#x43F;&#x430;&#x441; (&#x432;&#x44B; &#x432;&#x441;&#x435;&#x433;&#x434;&#x430;
        &#x43C;&#x43E;&#x436;&#x435;&#x442;&#x435; &#x435;&#x433;&#x43E; &#x43F;&#x43E;&#x43B;&#x443;&#x447;&#x438;&#x442;&#x44C;),
        &#x432;&#x432;&#x435;&#x434;&#x438;&#x442;&#x435; 0 &#x438; &#x438;&#x441;&#x43F;&#x43E;&#x43B;&#x44C;&#x437;&#x443;&#x439;&#x442;&#x435;
        &#x43D;&#x435;&#x43E;&#x433;&#x440;&#x430;&#x43D;&#x438;&#x447;&#x435;&#x43D;&#x43D;&#x44B;&#x439;
        &#x441;&#x442;&#x43E;&#x43B;&#x431;&#x435;&#x446;</th>
      <th style="text-align:left">40</th>
    </tr>
  </thead>
  <tbody></tbody>
</table>

| available\_on | Нет | Оставьте пустым |  |
| :--- | :--- | :--- | :--- |


| On\_demand \(unlimited\) | Да | Если у вас есть бесконечные запасы для этого товара, введите 1, если вы используете on\_hand, оставьте пустым. Если вы введете число в in\_stock _и_ 1 в неограниченном количестве, товар будет неограниченным. | 1 |
| :--- | :--- | :--- | :--- |


| shipping\_category | Да | В какой категории доставки находится этот товар? Доступные категории доставки перечислены на странице импорта товара. |  |
| :--- | :--- | :--- | :--- |


| tax\_category | Нет | Если цена вашего товара включает налог типа GST, если нет, оставьте пустым | GST |
| :--- | :--- | :--- | :--- |


| description | Нет | Вы можете создать описание, но не можете его обновить. Пожалуйста, убедитесь, что текст, который вы написали, соответствует текущему описанию в случае обновления. | Этот Йогурт сделан из местной малины |
| :--- | :--- | :--- | :--- |


В процессе импорта варианты различаются по единицам \(например, салат продается в упаковках по 500г и 750г\) или по полям display\_name \(например, йогурт продается в нескольких вариантах\). Пока имя товара совпадает, строки будут импортированы как варианты. В приведенном ниже примере показан салат, предлагаемый в вариантах 500г и 750г и йогурт, который представлен в нескольких вариантах.

| name | display\_name | price | units | unit\_type |
| :--- | :--- | :--- | :--- | :--- |
| Пакет Салата |  | 3.50 | 500 | г |
| Пакет Салата |  | 5.50 | 750 | г |
| Йогурт | Банан | 4 | 500 | г |
| Йогурт | Клубника | 4 | 500 | г |

Изображение ниже показывает, как эти товары будут отображаться в магазине. Обратите внимание, что поле 'name' становится первичным заголовком, а поле 'display\_name' становится вторичным заголовком. В случае с Пакет Салата поле 'display\_name' пустое, поэтому по умолчанию используется 'name'.

![](../../.gitbook/assets/image%20%281%29.png)

#### Unit type examples

Below are some examples to show how products with different units \(g, ml, kg and items\) should be uploaded.

| producer | **name** | **category** | **price** | **units** | **unit\_type** | **variant\_unit\_name** |
| :--- | :--- | :--- | :--- | :--- | :---: | :---: |
| Sue's Salads | Salad Bag | Vegetables | 3.50 | 500 | g |  |
| Henry Orchards | Fruit Juice | Drinks | 3.50 | 300 | ml |  |
| Fernwell Produce | Potatoes | Vegetables | 9.50 | 5 | kg |  |
| Tom's Bakery | Wholemeal Bread | Baked goods | 3.00 | 1 |  | loaf |

### Import the CSV

Once you have filled out the **Product List Template CSV** you are ready to upload it into OFN.

1. Go to **Products** &gt;  **Product Import.**
2. **Select import type:** Select Product List
3. **Select a spreadsheet to upload:** Find the csv file you wish to upload.

   Because you are uploading new products, you can leave the '_Set stock to zero for all exiting products not present in the file_' checkbox unchecked.

4. Click **Upload**.

You'll be shown a summary of your upload, including any errors. You'll also be told how many products you are creating and how many you are updating. If you're happy with the upload results, click **save**.

{% hint style="success" %}
It's good practice to check that the products uploaded/updated as you intended.
{% endhint %}

You can then upload another spreadsheet or go to the products page to view your new products.

## Update Existing Product Details

The instructions below relate to updating the details of an existing product. This tool is intended as a quick way to update product prices and stock levels.

{% hint style="info" %}
You can simultaneously upload new products and update existing products with a single CSV upload. The instructions in this guide are separated for clarity but you can combine new products and updates in the same spreadsheet.
{% endhint %}

### Prepare the CSV file for import

The process for updating product details is similar to [uploading new products](product-and-inventory-import.md#import-new-products). The first step is to download the **Product List Template** and fill in the product names and the supplier names. If you have this spreadsheet on hand from a previous upload even better.

The system requires seven fields to correctly identify the product you want to update. There are four fields which can be updated and four fields which cannot using this tool.

| Required fields \(you can't update\) | Fields you can update | Fields that won't update and aren't required |
| :--- | :--- | :--- |
| \*producer | sku | ^variant\_unit\_name |
| \*name | price | ^tax\_category |
| ^category | in\_stock | ^shipping\_category |
| \*units | unlimited | ^description |
| ^unit\_type \(if applicable\) |  |  |
| ^variant\_unit\_name \(if applicable\) |  |  |
| \*display\_name |  |  |

_^ if you try to update these fields you'll see an error message_

_\*If you try to update these fields you'll actually create new products or variants, rather than update an existing product._

Once complete, the .csv can be [imported](product-and-inventory-import.md#import-the-csv) in the same manner as for new products.

{% hint style="info" %}
**Set stock to zero for all exiting products not present in the file:**  
If you select this tickbox the system will set the 'In Stock' value to zero for _all products already your product list_.  
If a product was 'Unlimited' it will remain 'Unlimited'.  
The Products in this import will retain the stock level set in the .csv
{% endhint %}

## Import New Inventory or update your inventory

Use these instructions if you want to add or update new products to your [inventory](inventory-tool.md).

### Prepare the CSV file for import

Firstly, download the **Inventory Template CSV** file from the **Product Import** page.

You'll see that the template gives all the column headings required to successfully import a product. Each row is for a new product or variant. Below is a description of how to fill in each column.

{% hint style="info" %}
Note that all fields are case sensitive. E.g. you must use mL not ml , or Dairy not dairy.
{% endhint %}

| Column Title | Required? | Description | Example |
| :--- | :--- | :--- | :--- |
| producer | Y | This is the name of the producer profile that this inventory item will be assigned to | Four Mile Farm |
| distributor | Y | This is the name of the hub profile the inventory item will be assigned to | Demo Hub |
| name | Y | This is the name of the product | Yoghurt |
| display name | N | This field applies if you are creating variants \(see instructions below\). If you're not creating a variant leave this field blank. | Rasberry Yoghurt |
| variant\_unit\_name | Y | If the product is sold as an item \(e.g loaf, bunch, pumpkin\) write the item type here | Bunch |
| units | Y | The weight, volume or quantity value | 500 |
| unit\_type | Y | What unit is it sold in \(g, kg, T, mL, L\)? If sold as an item \(e.g. bunch\) leave blank | g |
| price | Y | The price of the product. If the item carries tax, this must be the tax inclusive price. | 3.70 |
| On\_Hand  \(in\_stock\) | Y | Please check the rules for unlimited below | leave blank as unlimited is set to 1 |
| On\_demand \(unlimited\) | Y | If blank - Read as "Use producer stock settings", so "in\_stock" should be blank.   If you set it to "1" - Read as unlimited of "Yes", so "in\_stock" should be blank.     If you set it to "0" - Read as unlimited of "No", so "in\_stock" is required. | 1 |
| sku | N | The SKU code for this product | AD001265 |

### Import the CSV <a id="import-the-csv"></a>

Once you have filled out the **Inventory Template CSV** you are ready to upload it into OFN.

1. Go to **Products** &gt;  **Product Import.**
2. **Select import type:** Select Inventories
3. **Select a spreadsheet to upload**
4. Click **Upload**.

You'll be shown a summary of your upload, including any errors. You'll also be told how many products you are creating and how many you are updating. If you're happy with the upload results, click **save**.

{% hint style="success" %}
It's good practice to check that the products uploaded/updated as you intended.
{% endhint %}

