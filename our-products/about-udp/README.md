---
description: >-
  Навіщо проксі потрібна підтримка UDP і як вона допомагає уникати виявлення
  антифрод-системами
icon: shield-exclamation
---

# Про протокол UDP

### **Зміст**

* [Як працює виявлення через WebRTC](how-webrtc-leak-works.md)
* [Як перевірити витік або працездатність WebRTC](webrtc-leak-check-tools.md)
* [Чому блокування WebRTC не рятує від виявлення](why-blocking-webrtc-doesnt-help.md)
* [Як встановити Tampermonkey і скрипт для налагодження WebRTC](tampermonkey-webrtc-debug.md)
* [Результати наших польових тестів](field-test-results.md)
* [Програмні рішення для ввімкнення WebRTC](webrtc-software-solutions.md)
* [Доступність UDP за продуктами](#dostupnist-udp-za-produktami)
* [FAQ (Часті запитання)](../../faq-and-support/faq/)

### **Вступна теорія**

Сучасні антифрод-системи використовують дедалі більше способів визначити реальну IP-адресу та виявити інструменти, які маскують мережевий трафік. Навіть якщо ви використовуєте проксі або <mark style="color:purple;">VPN</mark>, сайт може виявити таке маскування за іншими ознаками.

Один із таких механізмів пов'язаний із <mark style="color:purple;">WebRTC</mark>. Ця технологія може надсилати запити через UDP і розкривати реальну IP-адресу користувача, якщо проксі або клієнтська програма не підтримує UDP чи неправильно спрямовує такий трафік.

## Доступність UDP за продуктами

| Продукт | Підтримка UDP |
| --- | --- |
| [Datacenter](../datacenter-proxies.md) | ✓ У всіх локаціях |
| [ISP](../isp-proxies.md) | ✓ У всіх локаціях |
| [Mobile](../mobile-proxies.md) | ✓ |
| [Standard Residential](../residential-proxies/standard-residential.md) | ✓ Крім США; діють [обмеження портів](../restrictions.md) |
| [Unlimited Residential](../residential-proxies/unlimited-residential-proxy.md) | ✓ Крім США; діють [обмеження портів](../restrictions.md) |
| [Premium Residential](../residential-proxies/premium-residential.md) | ✓ У всіх локаціях, [крім окремих міст і пристроїв macOS/iOS](../restrictions.md) |

Для передавання UDP використовуйте SOCKS5 і програму з підтримкою `UDP ASSOCIATE`. Сумісні варіанти перелічені в розділі [Програмні рішення для ввімкнення WebRTC](webrtc-software-solutions.md).

Повний список винятків і закритих портів наведений на сторінці [Обмеження](../restrictions.md).
