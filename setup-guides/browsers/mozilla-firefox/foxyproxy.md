---
description: Налаштування проксі для Mozilla Firefox
---

# FoxyProxy

## Встановлення FoxyProxy

{% hint style="warning" %}
FoxyProxy працює лише з TCP-трафіком.
{% endhint %}

Встановіть [FoxyProxy Standard](https://addons.mozilla.org/firefox/addon/foxyproxy-standard/) із Firefox Add-ons.

{% embed url="https://addons.mozilla.org/firefox/addon/foxyproxy-standard/" %}

<figure>
  <picture>
    <source srcset="../../../.gitbook/assets/foxyproxy-addon-page_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../../.gitbook/assets/foxyproxy-addon-page_white.png" alt="FoxyProxy Standard у Firefox Add-ons">
  </picture>
</figure>

Після встановлення відкрийте FoxyProxy та перейдіть до налаштувань розширення.

<figure>
  <picture>
    <source srcset="../../../.gitbook/assets/foxyproxy-options-popup-disable_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../../.gitbook/assets/foxyproxy-options-popup-disable_white.png" alt="Відкриття налаштувань FoxyProxy">
  </picture>
</figure>

## Налаштування проксі

Відкрийте `Proxies` і натисніть `Add`.

<figure>
  <picture>
    <source srcset="../../../.gitbook/assets/foxyproxy-add-proxy-form_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../../.gitbook/assets/foxyproxy-add-proxy-form_white.png" alt="Додавання проксі у FoxyProxy">
  </picture>
</figure>

{% hint style="info" %}
Формат даних і приклад замовлення описані в розділі [Початок роботи](../../getting-started.md).
{% endhint %}

Укажіть назву профілю в полі `Title`. Виберіть тип проксі та заповніть поля `Hostname`, `Port`, `Username` і `Password` даними з `Proxy List` вашого замовлення. Натисніть `Save`.

<figure>
  <picture>
    <source srcset="../../../.gitbook/assets/foxyproxy-proxy-config-filled_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../../.gitbook/assets/foxyproxy-proxy-config-filled_white.png" alt="Заповнений профіль проксі у FoxyProxy">
  </picture>
</figure>

## Підключення

Відкрийте FoxyProxy та виберіть створений профіль.

<figure>
  <picture>
    <source srcset="../../../.gitbook/assets/foxyproxy-options-popup-proxyshard_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../../.gitbook/assets/foxyproxy-options-popup-proxyshard_white.png" alt="Вибір профілю проксі у FoxyProxy">
  </picture>
</figure>

Проксі підключено та готово до роботи в Mozilla Firefox.
