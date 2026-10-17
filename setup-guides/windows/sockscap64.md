# SocksCap64

{% hint style="success" %}
SocksCap64 підтримує проксіювання TCP- і UDP-трафіку.
{% endhint %}

## Встановлення

Завантажте `SocksCap64-setup-4.7.exe` зі [сторінки релізу](https://github.com/bobo2334/sockscap64/releases/tag/4.7), встановіть програму та запустіть її від імені адміністратора.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/sockscap64-github-download_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/sockscap64-github-download_white.png" alt="Завантаження SocksCap64 з GitHub">
  </picture>
</figure>

## Додавання проксі

1. Натисніть `Proxy` у верхній панелі.
2. У вікні `Proxy Manager` натисніть `+`.
3. Заповніть дані підключення:
   - `Proxy Address`: IP-адреса або домен сервера;
   - `Port`: порт підключення;
   - `Account`: логін;
   - `Password`: пароль;
   - `SOCKS Type`: `SOCKS 5`.
4. Натисніть `Save`.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/sockscap64-proxy-manager-config_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/sockscap64-proxy-manager-config_white.png" alt="Налаштування проксі у SocksCap64">
  </picture>
</figure>

{% hint style="info" %}
Розташування даних підключення описано в [загальній інструкції](../getting-started.md).
{% endhint %}

## Додавання програми

Натисніть `Apps`, виберіть потрібну програму у вікні `Programs selector` і натисніть `OK`.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/sockscap64-programs-selector-add_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/sockscap64-programs-selector-add_white.png" alt="Додавання програми у SocksCap64">
  </picture>
</figure>

## Запуск через проксі

Клацніть правою кнопкою миші на доданій програмі та виберіть `Run selected program in tunnel`. Програма запуститься через налаштований SOCKS5-проксі.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/sockscap64-run-program-in-tunnel_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/sockscap64-run-program-in-tunnel_white.png" alt="Запуск програми через проксі-тунель">
  </picture>
</figure>
