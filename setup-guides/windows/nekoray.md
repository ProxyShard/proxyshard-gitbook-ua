# NekoRay

{% hint style="success" %}
NekoRay підтримує проксіювання TCP- і UDP-трафіку в режимі TUN.
{% endhint %}

## Завантаження та запуск

Завантажте архів для Windows зі [сторінки релізів NekoRay](https://github.com/MatsuriDayo/nekoray/releases), розпакуйте його та запустіть `nekoray.exe` або `nekobox.exe`. Під час першого запуску виберіть ядро `sing-box`.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/nekoray-github-download_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/nekoray-github-download_white.png" alt="Завантаження NekoRay з GitHub">
  </picture>
</figure>

## Створення профілю

Клацніть правою кнопкою миші на порожній області списку серверів і виберіть `New profile`.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/nekoray-main-new-profile_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/nekoray-main-new-profile_white.png" alt="Створення нового профілю NekoRay">
  </picture>
</figure>

У списку `Type` виберіть `Socks`.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/nekoray-profile-type-socks_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/nekoray-profile-type-socks_white.png" alt="Вибір типу Socks у NekoRay">
  </picture>
</figure>

Введіть дані підключення:

1. У полі `Name` задайте зрозумілу назву.
2. У `Address` і `Port` введіть адресу та порт проксі.
3. У розділі `Socks` виберіть `Version: 5`.
4. Заповніть `Username` і `Password`.
5. Натисніть `OK`.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/nekoray-profile-config_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/nekoray-profile-config_white.png" alt="Налаштування SOCKS5-проксі в NekoRay">
  </picture>
</figure>

{% hint style="info" %}
Розташування даних підключення описано в [загальній інструкції](../getting-started.md).
{% endhint %}

## Підключення

Виберіть створений профіль і ввімкніть `Tun Mode` у верхній панелі. Після запуску системний трафік проходитиме через налаштований проксі.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/nekoray-tun-mode-enable_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/nekoray-tun-mode-enable_white.png" alt="Увімкнення Tun Mode у NekoRay">
  </picture>
</figure>
