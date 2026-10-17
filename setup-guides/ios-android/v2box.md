# V2Box

{% hint style="success" %}
V2Box підтримує UDP-трафік.
{% endhint %}

## Встановлення V2Box

Встановіть V2Box із магазину застосунків для вашого пристрою.

#### <mark style="color:green;">Android</mark>

{% embed url="https://play.google.com/store/apps/details?id=dev.hexasoftware.v2box" %}

#### <mark style="color:blue;">**iOS**</mark>

{% embed url="https://apps.apple.com/app/v2box-v2ray-client/id6446814690" %}

## Налаштування V2Box

1. Відкрийте `Configs`.
2. Натисніть `+`, щоб створити конфігурацію.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/v2box-ios-configs-add_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/v2box-ios-configs-add_white.png" alt="Додавання конфігурації у V2Box">
  </picture>
</figure>

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/v2box-ios-add-manual-config_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/v2box-ios-add-manual-config_white.png" alt="Ручне налаштування конфігурації у V2Box">
  </picture>
</figure>

У полі `Protocol` виберіть `SOCKS`.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/v2box-ios-protocol-socks_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/v2box-ios-protocol-socks_white.png" alt="Вибір протоколу SOCKS у V2Box">
  </picture>
</figure>

Уведіть назву конфігурації в полі `Remarks`. Заповніть поля `Address`, `Port`, `Username` і `ID/Password/Key` даними з `Proxy List` вашого замовлення, потім натисніть `Save`.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/v2box-ios-server-form_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/v2box-ios-server-form_white.png" alt="Налаштування проксі у V2Box">
  </picture>
</figure>

{% hint style="info" %}
Формат даних і приклад замовлення описані в розділі [Початок роботи](../getting-started.md).
{% endhint %}

Поверніться до `Configs`, виберіть створену конфігурацію та використайте `Slide to Connect` для підключення.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/v2box-ios-connected_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/v2box-ios-connected_white.png" alt="Підключення проксі у V2Box">
  </picture>
</figure>

Перевірте підключення через [Proxy Tester](../../our-products/proxy-tester.md).
