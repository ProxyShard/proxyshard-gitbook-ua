---
icon: server
---

# Придбання ISP / датацентрових проксі

## Купівля проксі

Щоб придбати [датацентр-проксі](https://dashboard.proxyshard.com/datacenter-proxy) або [ISP-проксі](https://dashboard.proxyshard.com/isp-proxy):

1. Відкрийте розділ `Datacenter Proxy` або `ISP Proxy` залежно від потрібного типу проксі.
2. У полі `Proxy region` виберіть країну проксі.
3. У полі `Billing cycle` виберіть період оплати.
4. У полі `Number of proxies` укажіть кількість проксі.
5. Увімкніть `Auto renew`, якщо хочете автоматично продовжувати замовлення.
6. За потреби увімкніть `Enable p0f settings`.
7. У полі `Total slots` укажіть кількість слотів для p0f.
8. Якщо у вас є промокод, введіть його в поле `Promocode` і натисніть `Apply`.
9. Перевірте вартість замовлення та натисніть `Buy now`.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/datacenter-purchase-form_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/datacenter-purchase-form_white.png" alt="Форма купівлі проксі">
  </picture>
</figure>

## Оплата замовлення

Після натискання `Buy now` відкриється рахунок зі статусом `Unpaid`. Перевірте суму в рядку `Total amount`, а потім натисніть `Pay with Wallet`.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/datacenter-invoice-payment_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/datacenter-invoice-payment_white.png" alt="Оплата рахунку з балансу ProxyShard">
  </picture>
</figure>

Після оплати замовлення з'явиться в блоці `Active products` і в розділі [`My orders`](https://dashboard.proxyshard.com/products). Для оплаченого замовлення відображається статус `Active`.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/datacenter-active-products_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/datacenter-active-products_white.png" alt="Список активних замовлень">
  </picture>
</figure>

{% hint style="warning" %}
Проксі почнуть працювати протягом 1-2 хвилин. Цей час потрібен для синхронізації замовлення.
{% endhint %}

## Продовження замовлення

Замовлення можна продовжувати автоматично або вручну.

Якщо ввімкнено `Auto renew`, система спробує продовжити замовлення за 1-2 години до завершення оплаченого періоду. Якщо коштів на балансі достатньо, оплата спишеться автоматично, а проксі продовжать працювати.

Якщо автоматичне продовження вимкнено або на балансі недостатньо коштів, замовлення отримає статус `On-hold`. Для ручного продовження відкрийте замовлення, натисніть ![](<../../.gitbook/assets/datacenter-renew-button.png>) та оплатіть новий рахунок.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/datacenter-order-details_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/datacenter-order-details_white.png" alt="Ручне продовження замовлення">
  </picture>
</figure>

{% hint style="danger" %}
Замовлення зі статусом `Canceled` продовжити неможливо. Цей статус надається через три дні після несплати замовлення.
{% endhint %}
