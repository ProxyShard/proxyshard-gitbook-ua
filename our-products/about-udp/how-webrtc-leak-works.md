---
description: Принцип роботи WebRTC
icon: wave-square
---

# Як працює витік через WebRTC

1. Сайт надсилає звичайний TCP-запит від браузера (або антидетект браузера).
2. Антифрод-система відповідає та підсовує скрипт для STUN-запиту.
3. Браузер робить STUN-запит по UDP, минаючи проксі з цієї адреси, оскільки пам'ятаємо, що проксі чи антидетект браузер може підтримувати UDP.
4. Якщо IP у TCP з'єднання та UDP розрізняються – користувача викривають у використанні проксі.<br>

    <figure><img src="../../.gitbook/assets/image (181).png" alt=""><figcaption><p>Зображення та інформація взята та перекладена зі статті <a href="https://telegra.ph/Zachem-nuzhny-proksi-s-UDP-i-pri-chyom-tut-protechka-WrbRTC-v-Antike-12-19"> ZloyTeam</a></p></figcaption></figure>
