---
icon: lock-keyhole-open
---

Чому одного TCP-проксі недостатньо!

Навіть якщо ваш SOCKS5-проксі підтримує <mark style="color:purple;">UDP</mark>, більшість антидетект-браузерів (зокрема, на базі Chromium) не вміють передавати <mark style="color:purple;">WebRTC</mark>-трафік через проксі. Причина – технічні обмеження ядра браузера.

\
На сьогоднішній день капчі-системи вже вводять посилену перевірку на наявність <mark style="color:purple;">WebRTC</mark>, як приклад може виступити <mark style="color:purple;">Discord</mark>, вони підключили "<mark style="color:purple;">Hcaptcha-enterprise</mark>", де вже включена перевірка <mark style="color:purple;">WebRTC</mark> у користувача.
