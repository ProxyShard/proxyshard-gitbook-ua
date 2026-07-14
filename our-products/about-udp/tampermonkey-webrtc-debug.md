---
description: Встановлення Tampermonkey в Chrome і додавання скрипту користувача
icon: server
---

# Як встановити tampermonkey та скрипт для дебага WebRTC

## Установка Tampermonkey

Для запуску скриптів в Chrome зручно використовувати розширення **Tampermonkey**.

Перейдіть до магазину Chrome і встановіть розширення:

{% embed url="https://chromewebstore.google.com/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo" %}

Після встановлення натисніть на значок розширень праворуч зверху та закріпіть **Tampermonkey**.

{% hint style="info" %}
Розширення потрібно лише для запуску скрипта у браузері. Саме собою воно не усуває витоку WebRTC.
{% endhint %}

## Як додати скрипт вручну

Для цієї інструкції використовуйте скрипт із Gist:

* [Скрипт для дебагу WebRTC](https://gist.github.com/Kr1tos/26585898c08e5222d5edc3d6fad546be)

{% stepper %}
{% step %}
#### Відкрийте Gist зі скриптом

Перейдіть за посиланням на Gist.

Відкрийте файл зі скриптом та повністю скопіюйте його вміст.
{% endstep %}

{% step %}
#### Створіть новий скрипт у Tampermonkey

Натисніть на іконку **Tampermonkey** та виберіть **Create a new script**.

Видаліть стандартний шаблон, який відкриється в редакторі.
{% endstep %}

{% step %}
#### Вставте код скрипту

Вставте скопійований код із Gist у редактор Tampermonkey.

Збережіть зміни поєднанням Ctrl+S** або кнопкою File → Save**.
{% endstep %}

{% step %}
#### Перевірте, що скрипт увімкнено

Переконайтеся, що новий скрипт відображається у списку Tampermonkey та знаходиться у статусі **Enabled**.
{% endstep %}
{% endstepper %}

## Як перевірити, що скрипт працює

1. Переконайтеся, що перемикач скрипта увімкнено.
2. Відновіть потрібну сторінку.
3. Відкрийте DevTools через **F12**.
4. Перейдіть на вкладку **Console**.
5. Зручно фільтрувати висновок за мітками `\[TM]`, `\[WebRTC]` та `\[NET]`.

### Які логи повинні з'явитися

Відразу після запуску скрипта зазвичай з'являються службові повідомлення:

```
[TM] Network hooks installed
[TM] WebRTC hook installed
```

Якщо сторінка створює RTCPeerConnection, у консолі з'являться логи по WebRTC:

```
[WebRTC] created
config: { iceServers: [...] }
ICE servers: [...]
```

Під час збору кандидатів будуть видні локальні та віддалені кандидати:

```
[WebRTC] local candidate raw: candidate:...
[WebRTC] local candidate parsed: { ip: "192.168.1.10", port: "52344", type: "host" }

[WebRTC] remote candidate raw: candidate:...
[WebRTC] remote candidate parsed: { ip: "185.123.45.67", port: "3478", type: "srflx" }
```

Якщо з'єднання дійшло до вибору маршруту, скрипт покаже підсумковий шлях:

```
[WebRTC] SELECTED PATH (connectionstatechange)
candidate-pair: { ... }
local-candidate: { ip: "10.0.0.2", port: 54012, protocol: "udp", candidateType: "host" }
remote-candidate: { ip: "185.123.45.67", port: 3478, protocol: "udp", candidateType: "srflx" }
[WebRTC] REAL REMOTE ENDPOINT: { ip: "185.123.45.67", port: 3478, protocol: "udp", candidateType: "srflx" }
```

Якщо сайт відправляє WebRTC-дані через `fetch`, `xhr`, `WebSocket` або `sendBeacon`, скрипт також це покаже:

```
[NET][fetch] https://site.example/api
[NET] SDP detected
v=0
o=- 46117317 2 IN IP4 127.0.0.1
...

[NET][ws] wss://site.example/socket
[NET] ICE detected
{"candidate":"candidate:...","sdpMid":"0","sdpMLineIndex":0}
```

### На що дивитися в першу чергу

* `\[TM] WebRTC hook installed` - скрипт успішно завантажився.
* `\[WebRTC] created` - сторінка реально створила WebRTC-з'єднання.
* `\[WebRTC] local candidate parsed` - видно локальний кандидат.
* `\[WebRTC] remote candidate parsed` - видно віддалений кандидат.
* `\[WebRTC] REAL REMOTE ENDPOINT` - найкорисніший лог. Він показує кінцеву віддалену точку, яку вибрав WebRTC.

### Якщо логів мало

Цей скрипт додає дві ручні команди до консолі:

```javascript
__dumpAllWebRTCSelectedPaths()
__dumpAllWebRTCStats()
```

Перша команда повторно виводить вибрані шляхи.

Друга показує повний знімок `candidate-pair`, `local-candidate`, `remote-candidate` та `transport`.

## Корисно перевірити після встановлення

Після запуску скрипту можна перевірити поведінку WebRTC через послуги зі статті [Через що можна перевірити витік WebRTC](webrtc-leak-check-tools.md).

Якщо хочете зрозуміти сам механізм витоку, дивіться статтю [Як працює витік через WebRTC](how-webrtc-leak-works.md).
