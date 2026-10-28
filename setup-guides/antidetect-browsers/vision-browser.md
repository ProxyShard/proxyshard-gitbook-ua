---
description: Антидетект-браузер із підтримкою UDP-проксі
---

# Vision Browser

{% hint style="success" %}
Vision Browser підтримує TCP- і UDP-трафік через SOCKS5-проксі.
{% endhint %}

## Встановлення та реєстрація

Відкрийте [сайт Vision Browser](https://browser.vision/r/ecf2408f-02de-4e4f-bc24-be368ac32325), завантажте програму та встановіть її.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/vision-website-download_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/vision-website-download_white.png" alt="Завантаження Vision Browser">
  </picture>
</figure>

Створіть обліковий запис. Ці дані потрібні для входу в програму.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/vision-sign-up_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/vision-sign-up_white.png" alt="Реєстрація у Vision Browser">
  </picture>
</figure>

Під час оплати тарифу можна використати промокод `PROXYSHARD` зі знижкою 20%.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/vision-plan-promo-code_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/vision-plan-promo-code_white.png" alt="Промокод PROXYSHARD у Vision Browser">
  </picture>
</figure>

## Створення першого профілю

1. Відкрийте `Profiles`.
2. Перейдіть у `Folders` і натисніть `Create folder`.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/vision-folders-create_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/vision-folders-create_white.png" alt="Створення папки профілів у Vision Browser">
  </picture>
</figure>

Введіть назву папки та збережіть її.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/vision-folder-create-form_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/vision-folder-create-form_white.png" alt="Назва папки профілів">
  </picture>
</figure>

У створеній папці натисніть `Create profile`.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/vision-profiles-create-profile_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/vision-profiles-create-profile_white.png" alt="Створення профілю Vision Browser">
  </picture>
</figure>

У панелі ShardX згенеруйте один проксі у форматі SOCKS5 і скопіюйте дані підключення.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/vision-residential-generate-single_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/vision-residential-generate-single_white.png" alt="Генерація SOCKS5-проксі у ShardX">
  </picture>
</figure>

У налаштуваннях профілю Vision відкрийте вкладку `SOCKS`, введіть дані проксі, перевірте з'єднання та натисніть `Save`.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/vision-create-profile-socks_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/vision-create-profile-socks_white.png" alt="Налаштування SOCKS5-проксі у профілі Vision">
  </picture>
</figure>

<figure><img src="../../.gitbook/assets/vision-folder-profile-created.png" alt="Створений профіль Vision Browser"><figcaption></figcaption></figure>

## Додавання списку проксі

Відкрийте вкладку `Proxies` і натисніть `Add proxy`.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/vision-proxies-add-proxy_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/vision-proxies-add-proxy_white.png" alt="Додавання проксі у Vision Browser">
  </picture>
</figure>

У панелі ShardX згенеруйте список проксі у форматі SOCKS5 і скопіюйте його.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/vision-residential-generate-list_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/vision-residential-generate-list_white.png" alt="Генерація списку SOCKS5-проксі">
  </picture>
</figure>

Вставте список у поле додавання. Після імпорту переконайтеся, що підключення мають статус `Online`.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/vision-proxies-imported-list_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/vision-proxies-imported-list_white.png" alt="Імпортований список проксі у Vision Browser">
  </picture>
</figure>

Щоб призначити проксі наявному профілю, натисніть значок у стовпці `Proxy`.

<figure><img src="../../.gitbook/assets/vision-profiles-proxy-column.png" alt="Стовпець Proxy у списку профілів"><figcaption></figcaption></figure>

Виберіть `Select proxy`, вкажіть потрібне підключення та перевірте його.

<figure><img src="../../.gitbook/assets/vision-edit-profile-select-proxy.png" alt="Вибір проксі для профілю Vision"><figcaption></figcaption></figure>

Після збереження проксі з'явиться у рядку профілю.

<figure><img src="../../.gitbook/assets/vision-profile-proxy-assigned.png" alt="Проксі призначено профілю Vision"><figcaption></figcaption></figure>

## Перевірка WebRTC

Запустіть профіль і відкрийте [ShardX IP Checker](https://proxyshard.com/ip-checker). Адреси TCP і WebRTC мають збігатися.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/vision-webrtc-check_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/vision-webrtc-check_white.png" alt="Перевірка TCP і WebRTC у Vision Browser">
  </picture>
</figure>
