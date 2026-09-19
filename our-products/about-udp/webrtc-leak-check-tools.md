---
icon: check-to-slot
---

# Через що можна перевірити витік WebRTC

Перевірити WebRTC можна через ProxyShard IP Checker або сторонній сервіс Ipbinding. Почніть із нашого інструмента: він показує зовнішню IP-адресу, адресу WebRTC і результат перевірки UDP в одному звіті.

## 1. ProxyShard IP Checker

{% embed url="https://proxyshard.com/ip-checker" %}

### Нормальний результат

За правильної конфігурації значення `My IP address` і `WebRTC IP` збігаються. Це означає, що WebRTC використовує адресу проксі, а UDP-трафік не обходить підключення.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/ip-checker-overview_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/ip-checker-overview_white.png" alt="Коректний результат перевірки WebRTC">
  </picture>
</figure>

### UDP-кандидатів не отримано

Якщо в полі `WebRTC IP` відображається `error`, а в блоці `WebRTC Check` вказано `No UDP candidates received`, браузер не отримав UDP-кандидатів.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/webrtc-check-failed_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/webrtc-check-failed_white.png" alt="Перевірка WebRTC без UDP-кандидатів">
  </picture>
</figure>

{% hint style="warning" %}
Такий результат сам по собі не означає витік IP. Зазвичай WebRTC заблоковано або вибраний продукт чи програма не передає UDP. Перевірте [доступність UDP у продуктах](./README.md#dostupnist-udp-za-produktami) та використовуйте [програму з підтримкою UDP ASSOCIATE](webrtc-software-solutions.md).
{% endhint %}

{% hint style="danger" %}
Якщо `WebRTC IP` показує адресу, що відрізняється від `My IP address`, WebRTC обходить проксі. Такий результат означає витік.
{% endhint %}

Докладний опис полів наведено на сторінці [IP Checker](../ip-checker.md).

## 2. Ipbinding

[Ipbinding](https://ipbinding.online/) також показує WebRTC-кандидати. Результат читається так само: адреса WebRTC має збігатися з адресою проксі.

{% embed url="https://ipbinding.online/" %}
