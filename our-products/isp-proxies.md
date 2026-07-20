---
icon: fire
---

# ISP проксі

<mark style="color:purple;">ISP проксі</mark> як і <mark style="color:purple;">Датацентр</mark> видаються лише одному користувачу, без спільного використання адреси кількома користувачами та інших прихованих обмежень. Адреси відносяться до типу <mark style="color:purple;">IPv4</mark> та мають підтримку <mark style="color:purple;">UDP</mark>.

<mark style="color:purple;">ISP проксі</mark> мають усі плюси, як у <mark style="color:purple;">Residential</mark> проксі та <mark style="color:purple;">Datacenter</mark>. Вони такі ж стабільні та статичні, як <mark style="color:purple;">Datacenter</mark>, але при цьому використовують IP-адреси, зареєстровані на домашніх Інтернет-провайдерах, як у <mark style="color:purple;">Residential</mark> проксі.

Це робить їх одним із найкращих варіантів для роботи з Tier-1 сайтами та сервісами, чутливими до типу <mark style="color:purple;">IP</mark>. А з підтримкою <mark style="color:purple;">UDP</mark> вони стають абсолютно недетектованими.
\
Нещодавнє оновлення на <mark style="color:purple;">ISP</mark> проксі додало можливість зміни відбитка (<mark style="color:purple;">p0f</mark>)

{% embed url="https://dashboard.proxyshard.com/en/isp-proxy" %}

## Характеристики

| Параметр       | Значення                           |
| -------------- | ---------------------------------- |
| Тип IP         | IPv4 (домашній провайдер)          |
| Шеринг         | Ні — один IP на одного користувача |
| Ліміт підключень | 2 500 на IP                      |
| Підтримка UDP  | ✓                                  |
| Підтримка p0f  | ✓ (+$0.6 / IP на місяць)           |
| Вартість       | **$2** / IP на місяць              |

## Доступні локації

| Країна |
| ------ |
| 🇹🇷 Туреччина |
| 🇺🇸 США |
| 🇨🇿 Чехія |

{% hint style="info" %}
Список локацій постійно розширюється.
{% endhint %}

## **Як вони працюють?**

У самому замовленні ви можете знайти кілька важливих пунктів і опцій, розглянемо їх:

Придбати ви можете на сторінці [ISP proxy](https://dashboard.proxyshard.com/en/isp-proxy), в ньому вам потрібно вказати <mark style="color:purple;">Країну</mark>, <mark style="color:purple;">Термін оренди</mark> та <mark style="color:purple;">Кількість</mark>. При необхідності можна активувати <mark style="color:purple;">Auto renew</mark>, для автоматичного продовження.

<figure><img src="../.gitbook/assets/image (57).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Після придбання проксі почнуть працювати протягом 1-2 хвилин, оскільки потрібна синхронізація бази даних із сервером проксі.
{% endhint %}

## Опис полів замовлення

Розглянемо поля <mark style="color:purple;">Замовлення</mark>:

<mark style="color:purple;">User ID</mark> - Це User використовується для внутрішньої ідентифікації вашого замовлення, іноді ми його просимо при зверненні до технічної підтримки.

<mark style="color:purple;">Status</mark> - статус замовлення, може мати статуси:

* <mark style="color:green;">**Active**</mark> - Активне замовлення
* <mark style="color:orange;">**On-Hold**</mark> - Очікування оплати замовлення при закінченні терміну оренди
* <mark style="color:red;">**Cancelled**</mark> - Скасоване замовлення

{% hint style="danger" %}
Замовлення зі статусом "<mark style="color:$danger;">**Cancelled**</mark>" неможливо відновити через три дні після завершення оренди.
{% endhint %}

<mark style="color:purple;">Price</mark> - Вартість продукту на місяць

<mark style="color:purple;">Username</mark> - Логін проксі

<mark style="color:purple;">Password</mark> - Пароль проксі

<mark style="color:purple;">Next Due Date</mark> - Наступна дата списання

<mark style="color:purple;">Copy proxy</mark> - кнопка для копіювання проксі в буфер обміну

<mark style="color:purple;">HTTP/SOCKS</mark> - Вибір типу протоколу проксі

<mark style="color:purple;">Re-generate</mark> - Зміна пароля на проксі

<mark style="color:purple;">Auto renew</mark> - перемикач для активації/деактивації продовження продукту щомісяця <mark style="color:purple;">(засоби списуються з балансу облікового запису в термін, вказаний при придбанні)</mark>

## Для яких завдань підходить

Будь-які криптобіржі, Polymarket, стабільні сесії web scraping, SEO моніторинг, e-commerce моніторинг цін, перевірка маркетплейсів, ad verification, brand monitoring, тестування сайтів із домашнього провайдерського ASN, QA авторизації та користувацьких сценаріїв, моніторинг доступності сайтів, account management.

## Плюси та мінуси ISP проксі

#### <mark style="color:green;">Плюси:</mark>

* **Справжні ISP адреси** — IP числяться за реальними домашніми інтернет-провайдерами (у геолокаційних базах тип ASN — провайдер, а не хостинг)
* **Надійні оператори домашнього зв'язку**
* **Широкий канал із мінімальною затримкою**
* **Статичні адреси в одні руки** — IP не змінюється протягом оренди
* **Підтримка p0f та UDP**

#### <mark style="color:red;">Мінуси:</mark>

* **Ціна** — вища, ніж у Datacenter проксі
* **Кількість доступних локацій** — вкрай складна інтеграція з реальними провайдерами, але ми постійно розширюємо список

{% hint style="info" %}
Про те, як можна налаштувати проксі, ви можете у нашому розділі "[Інструкція з використання ](../setup-guides/getting-started.md)"
{% endhint %}
