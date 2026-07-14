---
icon: house-signal
---

# Standard Residential

<mark style="color:purple;">Standard Residential</mark> — базовий пул резидентських проксі ProxyShard. Проксі розміщені на реальних домашніх пристроях, що пройшли стандартні фільтри відбору. Підтримують <mark style="color:purple;">UDP</mark>, що робить їх оптимальним вибором для завдань з <mark style="color:purple;">WebRTC</mark>.

{% embed url="https://dashboard.proxyshard.com/en/residential-main" %}

## Характеристики

| Параметр                    | Значення                       |
| --------------------------- | ------------------------------ |
| Розмір пулу                 | 300 000 — 400 000 пристроїв    |
| Макс. кількість з'єднань    | 35 000                         |
| Макс. швидкість на замовлення | 75 Mbps                      |
| Підтримка UDP               | ✓ (недоступно в локації США)   |
| [Фільтрація Device OS (p0f)](README.md#opis-poliv-nalashtuvan) | ✗ |
| Тарифікація                 | За гігабайти (Pay as you go)   |
| Вартість                    | **$2 / ГБ**                    |

## Для яких завдань підходить

- Автоматизація, парсинг, боти
- Мультиакаунтинг з антидетект-браузерами
- Завдання, що потребують підтримки <mark style="color:purple;">UDP / WebRTC</mark>
- Робота з платформами, що блокують датацентрові IP

{% hint style="info" %}
Потрібно прибрати обмеження за трафіком? Дивіться [Unlimited Residential](unlimited-residential-proxy.md) — той самий пул, але без підрахунку гігабайтів.\
Потрібен максимально великий і чистий пул? Дивіться [Premium Residential](premium-residential.md).
{% endhint %}

З обмеженнями продукту можна ознайомитися [тут](../restrictions.md).
