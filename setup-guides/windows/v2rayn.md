# v2rayN

{% hint style="success" %}
v2rayN підтримує проксіювання TCP- і UDP-трафіку в режимі TUN.
{% endhint %}

## Завантаження та запуск

Відкрийте [сторінку останнього релізу v2rayN](https://github.com/2dust/v2rayN/releases/latest), завантажте `v2rayN-windows-64.zip`, розпакуйте архів і запустіть `v2rayN.exe` від імені адміністратора.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/v2rayn-github-download_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/v2rayn-github-download_white.png" alt="Завантаження v2rayN з GitHub">
  </picture>
</figure>

## Додавання SOCKS-сервера

Відкрийте меню `Configuration` і виберіть `Add [SOCKS]`.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/v2rayn-menu-add-socks_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/v2rayn-menu-add-socks_white.png" alt="Додавання SOCKS-сервера у v2rayN">
  </picture>
</figure>

Заповніть параметри підключення:

- `Alias (remarks)`: будь-яка зрозуміла назва;
- `Address`: IP-адреса або домен проксі;
- `Port`: порт підключення;
- `User(Optional)`: логін;
- `Password(Optional)`: пароль.

Натисніть `Confirm`, щоб зберегти профіль.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/v2rayn-socks-config-dialog_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/v2rayn-socks-config-dialog_white.png" alt="Налаштування SOCKS-проксі у v2rayN">
  </picture>
</figure>

{% hint style="info" %}
Розташування даних підключення описано в [загальній інструкції](../getting-started.md).
{% endhint %}

## Підключення

Виберіть створений сервер і перевірте затримку. Потім увімкніть `Enable Tun` у нижній панелі, щоб спрямувати системний трафік через проксі.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/v2rayn-enable-tun-mode_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/v2rayn-enable-tun-mode_white.png" alt="Увімкнення Enable Tun у v2rayN">
  </picture>
</figure>
