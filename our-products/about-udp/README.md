---
description: >-
  Навіщо потрібна підтримка UDP у проксі та як це допомагає обходити
  антифрод-системи
icon: shield-exclamation
---

# Про протокол UDP

### **Зміст**

* [Як працює детект через WebRTC](how-webrtc-leak-works.md)
* [Через що можна перевірити витік або працездатність WebRTC](webrtc-leak-check-tools.md)
* [Чому одного TCP-проксі недостатньо! ](why-tcp-proxy-not-enough.md)
* [Програмні рішення для включення WebRTC](webrtc-software-solutions.md)
* [Чому блокування WebRTC не рятує від виявлення ](why-blocking-webrtc-doesnt-help.md)
* [Результати наших польових тестів](field-test-results.md)
* [FAQ (Часті питання)](../../faq-and-support/faq/)



### **Вступна теорія**

Сучасні антифрод-системи стають все більш наполегливими до визначення вашої реальної адреси або виявлення факту використання інструментів для приховання адреси. Навіть якщо ви використовуєте проксі або <mark style="color:purple;">VPN</mark>, вони можуть визначити, що ви не справжній користувач за багатьма параметрами.

Одним із найчастіших механізмів виявлення став <mark style="color:purple;">WebRTC</mark>, технологія, яка може надсилати запити повз проксі і тим самим «виявляти» ваш реальний IP, якщо немає блокування <mark style="color:purple;">WebRTC</mark> браузером.<br>

Рішення? Двостороння підтримка протоколу <mark style="color:purple;">UDP</mark> на проксі та програмних продуктах

{% hint style="info" %}
<sup>_Джерелом натхнення стала стаття від_</sup> [<sup>_Zl0yTeam_</sup>](https://t.me/Zl0yTeam)<sup>_._</sup> [<sup>_«Навіщо потрібні проксі з UDP і при чому тут WebRTC»_</sup>](https://telegra.ph/Zachem-nuzhny-proksi-s-UDP-i-pri-chyom-tut-protechka-WrbRTC-v-Antike-12-19)<sup>_ допомогла нам краще зрозуміти, як працює_</sup> <sup>_<mark style="color:purple;">WebRTC</mark>_</sup><sup>_, і написати цю статтю._</sup>
{% endhint %}

&#x20;
