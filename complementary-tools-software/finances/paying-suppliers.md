# Оплата поставщикам с файлами ABA \(Австралия\)

Пользователи, которые управляют магазином с несколькими поставщиками \(пользователи центра\), часто спрашивают нас о самом быстром способе пересылки платежей, которые они получают от клиентов, их поставщикам. Например, вы можете хранить товары от 20 производителей в своем центре-магазине. Получив заказы и платежи от клиентов, вы хотите быстро определить, сколько нужно перевести каждому поставщику, а затем быстро произвести оплату.

Эта страница описывает несколько способов, которыми пользователи могут платить своим поставщикам.

## Выясните, сколько вы должны своим поставщикам

Вы можете использовать [Отчеты](../../basic-features/reports.md), чтобы получить разбивку стоимости товаров, проданных от каждого поставщика. В отчете [Общее Количество Поставщиков в Цикле Заказа](../../basic-features/reports.md#order-cycle-supplier-totals) указывается общая стоимость товаров, проданных от каждого поставщика. В качестве альтернативы вы можете скачать отчет Общее Количество Клиентов в Цикле Заказа и создать несколько сводных таблиц для извлечения необходимых данных.

## Платежи поставщикам

Когда у вас есть суммы, которые вы должны заплатить каждому поставщику, следующим шагом часто является ввод этих сумм в вашу онлайн банковскую систему, чтобы сделать банковский перевод каждому поставщику. Это может занять много времени для тех, у кого много поставщиков.

На данный момент в ОСП отсутствует автоматизированная система расчета задолженности перед поставщиками и автоматической пересылки им платежей.

### Быстрый платеж нескольким поставщикам с помощью ABA-файла

{% hint style="info" %}
Примечание: Файл ABA представляет собой австралийский формат банковского файла, поэтому эта опция относится только к австралийским пользователям.
{% endhint %}

Альтернативой для австралийских пользователей является создание ABA-файла. ABA-файл - это файл такого типа, как электронная таблица Excel, который может быть загружен в большинство систем онлайн-банкинга австралийского банка, как способ оплаты нескольким людям без ввода их индивидуальных платежей вручную.

Существует несколько способов создания ABA-файла.

**1\) Используйте свою систему учета для создания ABA-файла**

При использовании системы учета, такой как MYOB, Quickbooks или Xero, вероятно, что пакет будет иметь инструмент "ABA generation". Эти инструменты различаются, но, как правило, они позволяют ввести суммы, которые вы хотите заплатить каждому поставщику, а также их банковские реквизиты \(BSB, номер счета, имя и т.д.\), и затем будет создан файл ABA. После чего вы можете загрузить этот файл в свой банк и платежи будут массово осуществляться.

{% hint style="info" %}
Возможно, вам потребуется связаться с банком, чтобы включить загрузку файла ABA. Это также может зависеть от типа банковского счета, который у вас есть, поэтому в первую очередь проверьте, что они это предлагают.
{% endhint %}

**2\) Использование оклайн генератора файлов ABA**

Cemtaxaba - это онлайн генератор файлов ABA, который может превратить файл Excel в файл ABA. Существуют комиссии, связанные с инструментом, проверьте их веб-сайт для получения подробной информации[ https://www.cemtexaba.com/](https://www.cemtexaba.com/)

Процесс использования этого инструмента заключается в следующем.

1\) Загрузите CSV-файл шаблона CemtexABA.

2\) Введите подробные данные в соответствующие столбцы. Они запрашивают банковские реквизиты получателя и сумму, которую вы хотите перевести.

3\) Загрузите CSV на веб-сайт Cemtexaba. Они запросят у вас банковские реквизиты \(данные 'плательщика'\), а затем предоставят вам файл ABA

4\) Загрузите файл ABA в свою систему онлайн-банкинга для выполнения массового платежа.

