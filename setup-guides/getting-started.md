---
icon: clipboard-list
---

# Інструкція з налаштування

## **Додавання списку проксі із замовлення в програми**

Щоб додати проксі в різні програми, відкрийте своє [замовлення](https://dashboard.proxyshard.com/products) на сайті та скопіюйте проксі:

{% hint style="warning" %}
**Зверніть увагу: в усіх прикладах підключення виконується через** <mark style="color:purple;">**SOCKS5**</mark>.\
\
**Для того щоб дізнатися порт підключення для:**\
\
<mark style="color:purple;">**Datacenter\ISP**</mark> - встановіть перемикач на <mark style="color:purple;">SOCKS5</mark> у полі <mark style="color:purple;">Proxy list</mark>

<p align="center"><img src="../.gitbook/assets/image (40).png" alt=""></p>

<mark style="color:purple;">**Residential proxy**</mark> - У налаштуваннях замовлення вказати "<mark style="color:purple;">Protocol</mark>" - <mark style="color:purple;">SOCKS5</mark>

<p align="center"><img src="../.gitbook/assets/image (42).png" alt="" data-size="original"></p>

<mark style="color:purple;">**Mobile proxy**</mark> - додаткові дії в замовленні не потрібні: один порт працює і через <mark style="color:purple;">HTTP</mark>, і через <mark style="color:purple;">SOCKS5</mark>
{% endhint %}

## Приклад для <mark style="color:purple;">Датацентр/ISP</mark> проксі

Відкрийте [замовлення](https://dashboard.proxyshard.com/products) та скопіюйте проксі з <mark style="color:purple;">Proxy List</mark>.

<figure><img src="../.gitbook/assets/image (35).png" alt=""><figcaption></figcaption></figure>

212.14.123.184 - IP адреса підключення до проксі

22334 - Port підключення до проксі

KDKKKEI - Login підключення проксі

KDKKEIID3 - Password проксі



## Приклад для <mark style="color:purple;">Резидентських проксі</mark>:

Вкажіть потрібні параметри проксі, наприклад країну/протокол, і натисніть "<mark style="color:purple;">Generate proxy</mark>"

<figure><img src="../.gitbook/assets/image (260).png" alt=""><figcaption></figcaption></figure>

Скопіюйте отримані проксі з <mark style="color:purple;">Proxy List</mark> або скопіюйте окремі поля підключення, якщо програма не підтримує вставку рядком.

Нижче наведено скріншот, де показано, які поля відповідають за "Server":"Port":"Login":"Password"

<figure><img src="../.gitbook/assets/image (36).png" alt=""><figcaption></figcaption></figure>
