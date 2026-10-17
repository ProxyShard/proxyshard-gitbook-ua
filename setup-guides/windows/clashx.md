# Clash for Windows

{% hint style="success" %}
Clash for Windows підтримує проксіювання TCP- і UDP-трафіку в режимі TUN.
{% endhint %}

## Завантаження та запуск

Відкрийте [сторінку релізів Clash for Windows](https://github.com/lantongxue/clash_for_windows_pkg/releases) і завантажте `Clash.for.Windows-0.20.39-win.7z`.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/clashx-github-download_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/clashx-github-download_white.png" alt="Завантаження Clash for Windows з GitHub">
  </picture>
</figure>

Розпакуйте архів в окрему папку.

<figure><img src="../../.gitbook/assets/clashx-extract-archive.png" alt="Розпакування архіву Clash for Windows"><figcaption></figcaption></figure>

Запустіть `Clash for Windows.exe` від імені адміністратора. Це потрібно для встановлення та роботи системного мережевого драйвера.

<figure><img src="../../.gitbook/assets/clashx-run-as-administrator.png" alt="Запуск Clash for Windows від імені адміністратора"><figcaption></figcaption></figure>

## Налаштування профілю

1. Відкрийте `Profiles`.
2. Натисніть значок `<>` біля `config.yaml`.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/clashx-profiles-edit-config_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/clashx-profiles-edit-config_white.png" alt="Відкриття редактора config.yaml">
  </picture>
</figure>

Додайте проксі до блоку `proxies:` і введіть дані із замовлення. У прикладі використовується SOCKS5.

```yaml
proxies:
  - name: "ProxyShard-Germany"
    type: socks5
    server: 123.123.123.123
    port: 41733
    username: proxy_login
    password: proxy_password
    udp: true

proxy-groups:
  - name: "ProxyShard"
    type: select
    proxies:
      - ProxyShard-Germany

rules:
  - PROCESS-NAME,chrome.exe,ProxyShard
  - MATCH,DIRECT
```

`name` задає назву підключення. У `server`, `port`, `username` і `password` введіть дані проксі. Параметр `udp: true` вмикає UDP для цього сервера.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/clashx-profile-config-proxies_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/clashx-profile-config-proxies_white.png" alt="Налаштування проксі у config.yaml">
  </picture>
</figure>

{% hint style="info" %}
Розташування даних підключення описано в [загальній інструкції](../getting-started.md).
{% endhint %}

## Активація та перевірка

1. Відкрийте `Proxies`.
2. Виберіть режим `Global`.
3. Натисніть `Check` біля сервера ProxyShard.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/clashx-proxies-global-select_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/clashx-proxies-global-select_white.png" alt="Вибір Global і перевірка проксі">
  </picture>
</figure>

Якщо з'єднання доступне, на картці з'явиться час відгуку.

<figure><img src="../../.gitbook/assets/clashx-proxy-ping-result.png" alt="Успішна перевірка проксі у Clash for Windows"><figcaption></figcaption></figure>

## Кілька проксі

Додайте кожен сервер окремим елементом у `proxies:` і перелічіть їхні назви в групі `ProxyShard`. Після збереження сервери з'являться в розділі `Proxies`, де між ними можна перемикатися.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/clashx-proxies-multiple-list_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/clashx-proxies-multiple-list_white.png" alt="Кілька проксі у Clash for Windows">
  </picture>
</figure>

## Увімкнення TUN Mode

1. Відкрийте `General`.
2. У рядку `TAP Device` натисніть `Manage`, потім `Install`.
3. Увімкніть `TUN Mode`, щоб спрямувати системний трафік через вибраний проксі.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/clashx-general-tap-tun-setup_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/clashx-general-tap-tun-setup_white.png" alt="Встановлення мережевого адаптера та ввімкнення TUN Mode">
  </picture>
</figure>

## Перевірка підключення

Відкрийте [ProxyShard IP Checker](https://proxyshard.com/tools/ip-checker) і переконайтеся, що відображається IP-адреса проксі.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/clashx-ip-checker-result_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/clashx-ip-checker-result_white.png" alt="Перевірка IP-адреси після налаштування Clash for Windows">
  </picture>
</figure>

Додатково перевірте WebRTC через BrowserLeaks.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/clashx-browserleaks-check_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/clashx-browserleaks-check_white.png" alt="Перевірка WebRTC через BrowserLeaks">
  </picture>
</figure>

Якщо з'єднання не працює, перевірте дані в `config.yaml`, повторно запустіть програму від імені адміністратора та скористайтеся [інструкцією з діагностики](../../faq-and-support/faq/proxy-not-working.md).
