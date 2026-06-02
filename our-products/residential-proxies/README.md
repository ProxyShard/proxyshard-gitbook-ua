---
icon: house-signal
---

# Резидентські проксі

<mark style="color:purple;">Резидентські проксі</mark> розміщені на реальних домашніх пристроях. Ідеально підходять для роботи з безліччю IP домашніх провайдерів, підтримують тонке націлювання аж до вибору оператора.\
З обмеженнями продуктів можна ознайомитися [тут](../restrictions.md).

{% hint style="warning" %}
Адреси видаються на реальних домашніх IP. Сесія може змінитися будь-якої миті, якщо пристрій у пулі вийде з мережі роздачі трафіку. Якщо вам потрібен **статичний IP** — дивіться [Datacenter](../datacenter-proxies.md) або [ISP проксі](../isp-proxies.md).
{% endhint %}

## Тарифи

| Параметр                | [Standard](standard-residential.md) | [Unlimited](unlimited-residential-proxy.md) | [Premium](premium-residential.md) |
| ----------------------- | ------------------------------------ | ------------------------------------------- | --------------------------------- |
| Розмір пулу             | 600k — 750k                          | 600k — 750k (= Standard)                    | 2.8M — 3.2M                       |
| Макс. з'єднань          | 35 000                               | 5 000                                       | —                                 |
| Макс. швидкість         | 75 Mbps                              | 75 Mbps                                     | 75 Mbps                           |
| Підтримка UDP           | ✓ (крім США)                         | ✓ (крім США)                                | ✗                                 |
| Безлімітний тариф       | ✗                                    | ✓                                           | ✗                                 |
| Тарифікація             | За ГБ (Pay as you go)                | День / Пів місяця / Місяць                  | За ГБ (Pay as you go)             |
| Вартість                | **$2 / ГБ**                          | **$30** / д · **$399** / пів міс. · **$699** / міс. | **$3 / ГБ**                 |

## Доступні локації

Актуальний список країн, регіонів, міст та операторів — на окремій сторінці:

{% content-ref url="available-countries.md" %}
[available-countries.md](available-countries.md)
{% endcontent-ref %}

## **Як почати використовувати?**

Розрахунок вартості резидентських проксі здійснюється від кількості придбаних гігабайт на замовлення.
\
Щоб отримати доступ до вибору країни та інших параметрів, потрібно [**придбати**](https://dashboard.proxyshard.com/residential-main) замовлення. Для цього перейдіть на сторінку ![](<../../.gitbook/assets/image (70).png>) і вкажіть кількість гігабайтів\
<br>

<figure><img src="../../.gitbook/assets/image (71).png" alt=""><figcaption></figcaption></figure>

## Опис полів налаштувань

У самому замовленні є кілька важливих пунктів і опцій. Розглянемо їх.

<figure><img src="../../.gitbook/assets/image (73).png" alt=""><figcaption></figcaption></figure>

<mark style="color:purple;">**Traffic used**</mark> - Скільки витрачено \ Скільки придбано

<mark style="color:purple;">**Country**</mark> - Вибір країни

<mark style="color:purple;">**Region**</mark> - Вибір регіону країни

<mark style="color:purple;">**City**</mark> - Вибір міста регіону

<mark style="color:purple;">**ISP**</mark> - Вибір типу провайдера (Тимчасово недоступний)

<mark style="color:purple;">**Session**</mark> - Вибір типу сесії, на вибір дається <mark style="color:purple;">Sticky</mark> та <mark style="color:purple;">Rotate</mark>.

* <mark style="color:purple;">Sticky</mark> дозволяє утримати одну IP адресу і залежить від вибраного параметра TTL.
* <mark style="color:purple;">Rotate</mark> змінює IP при кожному зверненні. Пул IP діапазонів у <mark style="color:purple;">Sticky</mark> менший, ніж у <mark style="color:purple;">Rotate</mark>

<mark style="color:purple;">**Protocol**</mark> - HTTP/SOCKS.\
Це основні протоколи для встановлення з'єднання із сервером проксі.

<mark style="color:purple;">**TTL**</mark> - З'являється при виборі <mark style="color:purple;">Session - Sticky</mark> та відповідає за час життя IP адреси (<mark style="color:purple;">Time to live</mark>). Мінімально можливий <mark style="color:purple;">TTL</mark> - 60 секунд (1 хвилина).

<mark style="color:purple;">**Relay**</mark> **-** Встановлюється лише у випадках, якщо немає підключення

<mark style="color:purple;">**Username\Password\Host\Port**</mark> - Дані для підключення також формуються в списку проксі і підтримують умовне форматування.

{% hint style="info" %}
Порти на проксі не впливають на кінцеву адресу, що отримується, це просто номер порту для віддаленого сервера проксі і не більше того!
{% endhint %}

<mark style="color:purple;">**Traffic Statistics**</mark> - Похвилинна статистика використаного трафіку. Є затримка у відображенні 10-20 хвилин.

<figure><img src="../../.gitbook/assets/image (78).png" alt=""><figcaption></figcaption></figure>

Наприкінці замовлення, ви можете виявити статистику запитів з вашого резидентського трафіку, в окремих випадках можуть бути затримки у відображенні до 20 хвилин.

## **Інструкція з налаштування**

1. Вкажіть налаштування - <mark style="color:purple;">Країна</mark>, <mark style="color:purple;">Регіон</mark> та інші параметри при необхідності

<figure><img src="../../.gitbook/assets/image (4) (1) (1).png" alt=""><figcaption></figcaption></figure>

2. Протокол <mark style="color:purple;">HTTP</mark> або <mark style="color:purple;">SOCKS5</mark> встановлюється за вашим бажанням <mark style="color:$info;">(як правило для роботи UDP встановлюють SOCKS5)</mark>

<figure><img src="../../.gitbook/assets/image (7) (1).png" alt=""><figcaption></figcaption></figure>

3. Сервер (<mark style="color:purple;">Relay</mark>) вказується лише при проблемах з підключенням

<figure><img src="../../.gitbook/assets/image (5) (1) (1).png" alt=""><figcaption></figcaption></figure>

4. Інші параметри встановлюються за необхідності

<figure><img src="../../.gitbook/assets/image (6) (1).png" alt=""><figcaption></figcaption></figure>

5. Натиснути кнопку <img src="../../.gitbook/assets/image (76).png" alt="" data-size="line"> та скопіювати проксі з <mark style="color:purple;">Proxy List</mark>

<figure><img src="../../.gitbook/assets/image (75).png" alt=""><figcaption></figcaption></figure>

В подальшому, якщо вам потрібна інша країна, потрібно вказати нові налаштування і натиснути <img src="../../.gitbook/assets/image (77).png" alt="" data-size="line"> і повторно встановити нові проксі в програму, звідки здійснюється підключення.

{% hint style="info" %}
Додаткову інформацію про форматування підключення можна дізнатися за посиланням [](how-to-use-residential-proxies.md)
{% endhint %}

{% hint style="warning" %}
Проксі в Proxy List не зберігаються, оскільки це динамічне поле. Можна згенерувати багато проксі різних локацій - старі при генерації нових проксі не перестануть працювати.
{% endhint %}

## Для яких завдань підходить

Соціальні мережі та мультиакаунтинг, криптобіржі (Binance, Bybit та інші), Polymarket, web scraping, SEO моніторинг, перевірка реклами (ad verification), e-commerce аналітика, моніторинг цін, геотаргетоване тестування сайтів.

## Плюси та мінуси Резидентських проксі

#### <mark style="color:green;">Плюси:</mark>

* **Гнучка тарифікація** — Pay as you go або безлімітна підписка (Unlimited)
* **Зміна IP** — ротація адрес за вимогою або за таймером (TTL)
* **Широкий геотаргетинг** — вибір країни, регіону, міста та оператора
* **Адреси домашнього походження** — IP зареєстровані на домашніх провайдерах
* **Підтримка UDP** — доступна на Standard та Unlimited (крім локації США)

#### <mark style="color:red;">Мінуси:</mark>

* **Можливі просідання швидкості** — залежить від якості інтернету на кінцевому пристрої, це специфіка продукту
* **Динамічний IP** — довільна зміна адреси можлива будь-якої миті; якщо потрібен статичний IP — дивіться [ISP](../isp-proxies.md) або [Datacenter](../datacenter-proxies.md)
* **Немає підтримки p0f** — у планах, стежте за оновленнями
* **UDP недоступний у локації США** на Standard та Unlimited

{% hint style="success" %}
Немає UDP чи потрібна статична адреса? [ISP проксі](../isp-proxies.md) закривають обидва пункти.
{% endhint %}

{% hint style="info" %}
Про те, як можна налаштувати проксі, ви можете у нашому розділі "[Інструкція з використання ](../../setup-guides/getting-started.md)"
{% endhint %}
