---
description: Сценарії автоматизації профілів ShardBrowser
icon: robot
---

# Automation

Розділ <mark style="color:purple;">**Automation**</mark> дає змогу створити сценарій із послідовності дій: відкрити сторінку, натиснути елемент, ввести текст, змінити проксі тощо. Натисніть <mark style="color:purple;">**+ New project**</mark>, щоб створити сценарій. Готовий проєкт можна завантажити кнопкою <mark style="color:purple;">**Import**</mark>.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/shardbrowser-automation-empty_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/shardbrowser-automation-empty_white.png" alt="Розділ Automation">
  </picture>
  <figcaption>Розділ Automation</figcaption>
</figure>

Сценарій збирається з кроків у вікні <mark style="color:purple;">**Add a step**</mark>. Кроки розбито на групи: <mark style="color:purple;">**Profile**</mark>, <mark style="color:purple;">**Proxy**</mark>, <mark style="color:purple;">**Navigation**</mark>, <mark style="color:purple;">**Touch**</mark>, <mark style="color:purple;">**Pointer**</mark>, <mark style="color:purple;">**Keyboard**</mark>, <mark style="color:purple;">**Flow**</mark>, <mark style="color:purple;">**Requests**</mark>, <mark style="color:purple;">**Traffic**</mark>, <mark style="color:purple;">**Data**</mark> та <mark style="color:purple;">**Database**</mark>. Потрібний крок можна знайти через пошук.

<figure>
  <picture>
    <source srcset="../../.gitbook/assets/shardbrowser-automation-add-step_black.png" media="(prefers-color-scheme: dark)">
    <img src="../../.gitbook/assets/shardbrowser-automation-add-step_white.png" alt="Вікно «Add a step»">
  </picture>
  <figcaption>Вікно «Add a step»</figcaption>
</figure>

Наприклад, у групі <mark style="color:purple;">**Profile**</mark> доступні кроки:

| Крок                   | Що робить                                       |
| ---------------------- | ----------------------------------------------- |
| Temporary profile      | Створює профіль, який буде видалено після виконання сценарію |
| Create profile         | Створює постійний профіль                       |
| Swap proxy (live)      | Змінює проксі без перезапуску браузера          |
| Use profile            | Використовує вже наявний профіль                |
| Keep profile           | Зберігає тимчасовий профіль після виконання сценарію |
| Read a profile setting | Читає значення налаштування профілю за назвою   |
| Delete profile         | Видаляє профіль                                 |

Кнопка <mark style="color:purple;">**Manage modules**</mark> керує підключеними модулями кроків.

{% hint style="info" %}
Профілями також можна керувати з власного коду через локальний HTTP API на `127.0.0.1:40325` - статус <mark style="color:purple;">**API on**</mark> показано внизу бічного меню.
{% endhint %}
