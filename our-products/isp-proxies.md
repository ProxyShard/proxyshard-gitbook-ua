---
icon: fire
---

# ISP проксі

<mark style="color:purple;">ISP проксі</mark> як і <mark style="color:purple;">Датацентр</mark> видаються лише одному користувачу, без спільного використання адреси кількома користувачами та інших прихованих обмежень. Адреси відносяться до типу <mark style="color:purple;">IPv4</mark> та мають підтримку <mark style="color:purple;">UDP</mark>.

<mark style="color:purple;">ISP проксі</mark> мають усі плюси, як у <mark style="color:purple;">Residential</mark> проксі та <mark style="color:purple;">Datacenter</mark>. Вони такі ж стабільні та статичні, як <mark style="color:purple;">Datacenter</mark>, але при цьому використовують IP-адреси, зареєстровані на домашніх Інтернет-провайдерах, як у <mark style="color:purple;">Residential</mark> проксі.

Це робить їх одним із найкращих варіантів для обходу блокувань та роботи з сайтами чутливими до типу <mark style="color:purple;">IP</mark>. Але за допомогою <mark style="color:purple;">UDP</mark> вони стають абсолютно не детектовані.
\
Нещодавнє оновлення на <mark style="color:purple;">ISP</mark> проксі додало можливо зміни відбитка (<mark style="color:purple;">p0f</mark>)

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

## Плюси та мінуси ISP проксі

Так як вони поєднують лише плюси датацентрових та резидентських проксі, у них немає мінусів, за винятком ціни та кількості доступних локацій.

{% hint style="info" %}
Про те, як можна налаштувати проксі, ви можете у нашому розділі "[Інструкція з використання ](../setup-guides/getting-started.md)"
{% endhint %}
