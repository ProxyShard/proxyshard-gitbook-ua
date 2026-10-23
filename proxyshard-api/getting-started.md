# Початок роботи

API ProxyShard дає змогу отримувати інформацію про профіль і замовлення, керувати проксі та виконувати інші операції зі своїх застосунків і скриптів.

## Де отримати API-ключ

1. У лівому нижньому куті натисніть кнопку з трьома крапками поруч із профілем.
2. Виберіть `Settings`.
3. Відкрийте вкладку `API`.
4. Натисніть `Copy`, щоб скопіювати ключ.

<figure>
  <picture>
    <source srcset="../.gitbook/assets/proxyshard-api-key_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/proxyshard-api-key_white.png" alt="Отримання API-ключа в особистому кабінеті ProxyShard">
  </picture>
</figure>

{% hint style="warning" %}
Не публікуйте API-ключ і не передавайте його стороннім. Кнопка `Change API Key` створює новий ключ. Після заміни оновіть ключ у всіх скриптах та інтеграціях.
{% endhint %}

## Автентифікація

Базова адреса API: `https://user-api.proxyshard.com`.

Для методів, які потребують автентифікації, передавайте API-ключ у заголовку запиту:

```http
Authorization: Bearer <API_KEY>
```
