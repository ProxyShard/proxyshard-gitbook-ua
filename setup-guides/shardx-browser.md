---
description: Встановлення ShardX Launcher, налаштування проксі та запуск першого профілю
icon: browser
---

# ShardX Launcher

{% hint style="info" %}
ShardX Launcher поширюється за ліцензією MIT як безкоштовний інструмент для особистого використання. Програма надається «як є». Ми регулярно випускаємо оновлення, але підтримку в лайв-чаті не надаємо - за серйозних проблем, будь ласка, створіть баг-репорт на [GitHub](https://github.com/ProxyShard/ShardBrowser/issues).
{% endhint %}

## Системні вимоги

### Windows

| Компонент       | Мінімум                                           | Рекомендується                                      |
| --------------- | ------------------------------------------------- | --------------------------------------------------- |
| ОС              | Windows 10 22H2 або Windows 11, 64-бит            | Windows 11 64-бит                                   |
| Архітектура     | x64 / x86\_64                                     | x64                                                 |
| Процесор        | Двоядерний 64-бит, підтримка SSE3                 | Чотириядерний і вище                                |
| ОЗП             | 4 ГБ                                              | 8 ГБ (16 ГБ при роботі з багатьма профілями)        |
| Місце на диску  | 1 ГБ                                              | 5 ГБ+                                               |
| Середовище      | Microsoft Edge WebView2                           | -                                                   |

### macOS

| Компонент      | Мінімум                             | Рекомендується              |
| -------------- | ----------------------------------- | --------------------------- |
| ОС             | macOS 11 Big Sur або новіше         | Остання стабільна версія    |
| Процесор       | Apple Silicon M1 або новіше         | Apple M2 або новіше         |
| ОЗП            | 4 ГБ                                | 8 ГБ і більше               |
| Місце на диску | 1 ГБ                                | 5 ГБ+                       |

{% hint style="warning" %}
Поточна збірка скомпільована під `aarch64-apple-darwin`. Mac на Intel не підтримується.
{% endhint %}

---

## Встановлення на Windows

Завантажте останню версію:

{% embed url="https://github.com/ProxyShard/ShardBrowser/releases/latest" %}

У розділі <mark style="color:purple;">**Assets**</mark> виберіть файл <mark style="color:purple;">`.exe`</mark> або <mark style="color:purple;">`.msi`</mark>.

<figure><img src="../.gitbook/assets/shardx-win-download.png" alt=""><figcaption>Виберіть .exe або .msi у розділі Assets</figcaption></figure>

Запустіть завантажений файл. <mark style="color:purple;">Windows SmartScreen</mark> може показати попередження - натисніть <mark style="color:purple;">**Докладніше**</mark>, потім <mark style="color:purple;">**Виконати в будь-якому разі**</mark>.

<figure><img src="../.gitbook/assets/shardx-win-smartscreen.png" alt=""><figcaption>SmartScreen - натисніть «Run anyway»</figcaption></figure>

Встановлювач завершить роботу за кілька секунд.

<figure><img src="../.gitbook/assets/shardx-win-install-done.png" alt=""><figcaption>Встановлення завершено</figcaption></figure>

---

## Встановлення на macOS

Завантажте останню версію:

{% embed url="https://github.com/ProxyShard/ShardBrowser/releases/latest" %}

У розділі <mark style="color:purple;">**Assets**</mark> виберіть файл <mark style="color:purple;">`aarch64.dmg`</mark>.

<figure><img src="../.gitbook/assets/shardx-mac-download.png" alt=""><figcaption>Виберіть aarch64.dmg у розділі Assets</figcaption></figure>

Відкрийте завантажений `.dmg` і перетягніть <mark style="color:purple;">**ShardX Launcher**</mark> до папки <mark style="color:purple;">**Applications**</mark>.

<figure><img src="../.gitbook/assets/shardx-mac-install-dmg.png" alt=""><figcaption>Перетягніть іконку до Applications</figcaption></figure>

### Зняття блокування Gatekeeper

{% hint style="warning" %}
Цей крок обов'язковий. macOS блокує всі непідписані застосунки - без нього програма не відкриється.
{% endhint %}

Відкрийте <mark style="color:purple;">**Термінал**</mark> одним із двох способів:

- <mark style="color:purple;">**Spotlight:**</mark> натисніть `⌘ + Пробіл`, введіть `terminal`, виберіть застосунок

<figure><img src="../.gitbook/assets/shardx-mac-find-terminal.png" alt=""><figcaption>Пошук Терміналу через Spotlight</figcaption></figure>

- <mark style="color:purple;">**Finder:**</mark> Програми (Applications) -> Службові програми (Utilities) -> Термінал

Вставте команду і натисніть <mark style="color:purple;">**Enter:**</mark>

```bash
xattr -dr com.apple.quarantine "/Applications/ShardX Launcher.app"
```

<figure><img src="../.gitbook/assets/shardx-mac-xattr-command.png" alt=""><figcaption>Команда виконається без виводу - це нормально</figcaption></figure>

Після цього відкрийте застосунок через <mark style="color:purple;">Spotlight</mark> (`⌘ + Пробіл` → `shardx`) або з папки <mark style="color:purple;">Applications</mark>.

<figure><img src="../.gitbook/assets/shardx-mac-open-spotlight.png" alt=""><figcaption>Запуск ShardX через Spotlight</figcaption></figure>

---

## Перший запуск

При першому запуску ShardX завантажить браузерний рушій із CDN (близько 198 МБ, один раз). Зачекайте завершення завантаження.

<figure><img src="../.gitbook/assets/shardx-win-first-run.png" alt=""><figcaption>Завантаження рушія при першому запуску</figcaption></figure>

Після завантаження відкриється головний екран <mark style="color:purple;">**Browsers**</mark>.

<figure><img src="../.gitbook/assets/shardx-win-ready.png" alt=""><figcaption>Головний екран ShardX Launcher</figcaption></figure>

---

## Додаємо проксі

Перейдіть до розділу <mark style="color:purple;">**Proxies**</mark> і натисніть <mark style="color:purple;">**+ New proxy**</mark>.

<figure><img src="../.gitbook/assets/shardx-setup-proxy-empty.png" alt=""><figcaption>Розділ Proxies</figcaption></figure>

У вікні <mark style="color:purple;">**Bulk import proxies**</mark> вставте проксі по одному на рядок. Підтримувані формати:

```
host:port
host:port:user:pass
scheme://host:port
scheme://user:pass@host:port
```

<figure><img src="../.gitbook/assets/shardx-setup-add-proxy.png" alt=""><figcaption>Вставте проксі по одному на рядок</figcaption></figure>

Натисніть <mark style="color:purple;">**Test all**</mark>, щоб перевірити проксі перед імпортом.

<figure><img src="../.gitbook/assets/shardx-setup-check-proxy.png" alt=""><figcaption>Натисніть «Test all» для перевірки, потім «Import»</figcaption></figure>

Після тесту кожен проксі отримає статус. Проксі з міткою <mark style="color:purple;">**UDP**</mark> підтримують <mark style="color:purple;">SOCKS5 UDP</mark>, а отже і <mark style="color:purple;">WebRTC</mark> - що дуже корисно при роботі з серйозними антифрод-системами. Якщо мітки <mark style="color:purple;">**UDP**</mark> немає, профіль браузера автоматично переходить у режим <mark style="color:purple;">**TCP-only**</mark>: IP не витече, однак трафік може виглядати підозріло для просунутих антифрод-систем. Ми наполегливо рекомендуємо використовувати [проксі з підтримкою UDP](../our-products/about-udp/).

Натисніть <mark style="color:purple;">**Import**</mark> - проксі з'явиться у списку зі статусом <mark style="color:purple;">**Active**</mark>.

<figure><img src="../.gitbook/assets/shardx-setup-proxy-done.png" alt=""><figcaption>Проксі додано</figcaption></figure>

---

## Створюємо перший профіль

Перейдіть до розділу <mark style="color:purple;">**Browsers**</mark> і натисніть <mark style="color:purple;">**+ New profile**</mark>.

<figure><img src="../.gitbook/assets/shardx-setup-profiles-empty.png" alt=""><figcaption>Розділ Browsers</figcaption></figure>

Параметри за замовчуванням змінювати не потрібно - ShardX сам згенерує унікальний <mark style="color:purple;">відбиток (fingerprint)</mark>. Обов'язково виберіть проксі у полі <mark style="color:purple;">**Proxy**</mark> внизу форми.

<figure><img src="../.gitbook/assets/shardx-setup-new-profile.png" alt=""><figcaption>Виберіть проксі і натисніть «Create profile»</figcaption></figure>

Натисніть <mark style="color:purple;">**Create profile**</mark>.

<figure><img src="../.gitbook/assets/shardx-setup-profile-proxy-check.png" alt=""><figcaption>Профіль створено</figcaption></figure>

---

## Запуск профілю

Натисніть <mark style="color:purple;">**Start**</mark> - браузер запуститься з ізольованим відбитком і проксі.

<figure><img src="../.gitbook/assets/shardx-setup-done.png" alt=""><figcaption>Профіль запущено</figcaption></figure>

---

## Можливі проблеми

### Windows: застосунок не запускається

Найімовірніше, не встановлено <mark style="color:purple;">Microsoft Edge WebView2 Runtime</mark>. Завантажте та встановіть його:

{% embed url="https://developer.microsoft.com/en-us/microsoft-edge/webview2/consumer" %}

На оригінальних образах Windows 10/11 WebView2 вже включено. На урізаних збірках його може бути видалено.

### macOS: «ShardX Launcher пошкоджено і не можна відкрити»

Стандартне блокування <mark style="color:purple;">Gatekeeper</mark>. Дотримуйтесь кроків у розділі [Зняття блокування Gatekeeper](#znyattya-blokuvannya-gatekeeper) - там описані обидва способи відкрити Термінал і команда для зняття карантину.

---

## Що далі?

- **Автоматизація:** керуйте профілями через [локальний HTTP API](../our-products/shardx-launcher.md) на `127.0.0.1:40325`
- **MCP-сервер:** завантажте з налаштувань (<mark style="color:purple;">Settings -> MCP server</mark>) для керування профілями через AI-агента
