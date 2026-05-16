---
icon: server
---

# Датацентр проксі

<mark style="color:purple;">Датацентр проксі</mark> є проксі для високонавантажених сценаріїв і завдання, як правило розміщуються на хостингах, мають найвищу швидкість і стабільність.

<mark style="color:purple;">Проксі Датацентр</mark> як і <mark style="color:purple;">ISP</mark> видаються лише одному користувачу, без спільного використання адреси кількома користувачами та інших прихованих обмежень. Адреси відносяться до типу <mark style="color:purple;">IPv4</mark> і також мають підтримку <mark style="color:purple;">UDP</mark>.

## **Як вони працюють?**

У самому замовленні ви можете знайти кілька важливих пунктів і опцій, розглянемо їх:

Придбати ви можете на сторінці [Datacenter proxy](https://dashboard.proxyshard.com/en/datacenter-proxy), в ньому вам потрібно вказати <mark style="color:purple;">Країну</mark>, <mark style="color:purple;">Термін оренди</mark> та <mark style="color:purple;">Кількість</mark>. При необхідності можна активувати <mark style="color:purple;">Auto renew</mark>, для автоматичного продовження.

<figure><img src="../.gitbook/assets/image (66).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Після придбання проксі почнуть працювати протягом 1-2 хвилин, оскільки потрібна синхронізація бази даних із сервером проксі.
{% endhint %}

## Опис полів замовлення

Розглянемо поля <mark style="color:purple;">Замовлення</mark>:

<figure><img src="../.gitbook/assets/image (67).png" alt=""><figcaption></figcaption></figure>

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

## Плюси та мінуси Датацентр проксі

#### <mark style="color:green;">**Плюси**</mark>_<mark style="color:green;">**:**</mark>_

* **Висока швидкість**

Досягається шляхом розміщення адрес у великих ЦОДах, де можливе підключення широкосмугового інтернату в 10 Гб. Ідеально для високонавантажених додатків та завдання <br>

* **Низька вартість**

У порівнянні з іншими продуктами, мають вкрай низьку вартість через велику кількість та легку масштабованість <br>

* **Ідеальні для будь-яких завдань**

Підходять під усі завдання, які не вимагають маскування під реального користувача.
Такими завданнями можуть бути парсинг сайтів, робота з різними біржами, Facebook, Twitter та інші сценарії, де немає суворої політики щодо походження адреси.

#### <mark style="color:red;">**Мінус:**</mark>

* **Легке розкриття**

Дані проксі можуть не підійти в ряді завдань, де є фільтрація ДЦ адрес, наприклад проекти DePIN. Вони на ранній стадії відтинають можливість роботи таких адрес. Для таких випадків підійдуть тільки <mark style="color:purple;">ISP</mark>/<mark style="color:purple;">Мобільні</mark>/<mark style="color:purple;">Резидентські проксі</mark>

{% hint style="success" %}
Дані мінуси обходяться [ISP прокси](isp-proxies.md)
{% endhint %}

{% hint style="info" %}
Про те, як можна налаштувати проксі, ви можете у нашому розділі "[Інструкція з використання ](../setup-guides/getting-started.md)"
{% endhint %}
