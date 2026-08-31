---
icon: git-alt
---

# Програмні рішення для ввімкнення WebRTC

#### Для повноцінної роботи WebRTC потрібне програмне забезпечення з підтримкою UDP ASSOCIATE.

Приклади підтримуваних програм для різних операційних систем:

<mark style="color:purple;">**Антидетект-браузери:**</mark>

* [<mark style="color:$success;">Vision</mark>](../../setup-guides/antidetect-browsers/vision-browser.md): доступне та надійне рішення серед платних браузерів із підтримкою UDP, QUIC, Smart Fingerprint та інших корисних функцій. Понад 60% команд на нашому сайті обирають саме його.

{% hint style="success" %}
Поєднання наших [ISP Proxy](https://dashboard.proxyshard.com/en/isp-proxy) і браузера [Vision](../../setup-guides/antidetect-browsers/vision-browser.md) є одним із рекомендованих варіантів для роботи з UDP через проксі. ISP Proxy також підтримує зміну мережевого відбитка [p0f](../p0f-spoofing.md).
{% endhint %}

* [<mark style="color:$tint;">ShardX</mark>](../shardx-launcher.md): наше рішення з відкритим вихідним кодом, широким вибором профілів і коректною підтримкою UDP та QUIC.

<mark style="color:purple;">**Windows:**</mark>

* ProxiFyre + Windows Packet Filter
* Win2Socks
* Netch
* [ClashX](../../setup-guides/windows/clashx.md)
* [V2rayN](../../setup-guides/windows/v2rayn.md)

<mark style="color:purple;">**macOS:**</mark>

* [V2Box](../../setup-guides/ios-android/v2box.md)

<mark style="color:purple;">**Linux:**</mark>

* proxychains-NG + go-tun2socks
* redsocks-ng

<mark style="color:purple;">**Android:**</mark>

* Clash for Android
* SocksDroid
* [Super Proxy](../../setup-guides/ios-android/super-proxy.md)
* [V2Box](../../setup-guides/ios-android/v2box.md)
* [Potatso](../../setup-guides/ios-android/potatso.md)

{% hint style="info" %}
Актуальний список програм доступний в [Інструкції з використання](../../setup-guides/getting-started.md).
{% endhint %}
