---
description: Встановлення ShardBrowser, додавання проксі та запуск першого профілю
icon: browser
---

# ShardBrowser

<figure>
  <picture>
    <source srcset="../.gitbook/assets/shardx-cover_black.svg" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/shardx-cover_white.svg" alt="Логотип ShardBrowser">
  </picture>
</figure>

{% hint style="info" %}
ShardBrowser - антидетект-браузер на базі Chromium від команди ProxyShard. Кожен профіль отримує власний відбиток (fingerprint) реального пристрою та свій проксі, тому сайти бачать профілі як різні комп'ютери. Програма розповсюджується безкоштовно і постачається «як є». У разі серйозних проблем створіть баг-репорт на [GitHub](https://github.com/ProxyShard/ShardBrowser/issues).
{% endhint %}

## Системні вимоги для Windows

| Компонент          | Мінімум                                | Рекомендовано                                  |
| ------------------ | -------------------------------------- | ---------------------------------------------- |
| ОС                 | Windows 10 22H2 або Windows 11, 64-біт | Windows 11 64-біт                              |
| Архітектура        | x64 / x86\_64                          | x64                                            |
| Процесор           | Двоядерний 64-біт, підтримка SSE3      | Чотириядерний і вище                           |
| ОЗП                | 4 ГБ                                   | 8 ГБ (16 ГБ при роботі з великою кількістю профілів) |
| Місце на диску     | 1 ГБ                                   | Від 5 ГБ                                       |
| Середовище виконання | Microsoft Edge WebView2              | Остання версія                                 |

---

## Встановлення на Windows

Завантажте останню версію:

{% embed url="https://github.com/ProxyShard/ShardBrowser/releases/latest" %}

У розділі <mark style="color:purple;">**Assets**</mark> виберіть інсталятор <mark style="color:purple;">`ShardBrowser.Launcher_<версія>_x64-setup.exe`</mark>. Якщо потрібна версія без встановлення, завантажте <mark style="color:purple;">`ShardBrowser-Launcher-portable-win-x64.exe`</mark>.

<figure>
  <picture>
    <source srcset="../.gitbook/assets/shardbrowser-github-release-assets_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/shardbrowser-github-release-assets_white.png" alt="Виберіть x64-setup.exe у розділі Assets">
  </picture>
  <figcaption>Виберіть x64-setup.exe у розділі Assets</figcaption>
</figure>

Запустіть завантажений файл. <mark style="color:purple;">Windows SmartScreen</mark> може показати попередження. Натисніть <mark style="color:purple;">**More info**</mark>, а потім <mark style="color:purple;">**Run anyway**</mark>.

<figure>
  <picture>
    <source srcset="../.gitbook/assets/shardbrowser-windows-smartscreen_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/shardbrowser-windows-smartscreen_white.png" alt="SmartScreen: натисніть Run anyway">
  </picture>
  <figcaption>SmartScreen: натисніть Run anyway</figcaption>
</figure>

## Встановлення на macOS

У розділі <mark style="color:purple;">**Assets**</mark> завантажте <mark style="color:purple;">`ShardBrowser.Launcher_<версія>_aarch64.dmg`</mark>. Ця збірка призначена для комп'ютерів Mac із процесорами Apple Silicon.

Відкрийте файл `.dmg` і перетягніть <mark style="color:purple;">**ShardBrowser Launcher**</mark> до <mark style="color:purple;">**Applications**</mark>. Збірка не нотаризована, тому macOS може заблокувати перший запуск. Відкрийте Terminal і виконайте команду:

```bash
xattr -dr com.apple.quarantine "/Applications/ShardBrowser Launcher.app"
```

Також застосунок можна дозволити в <mark style="color:purple;">**System Settings**</mark> → <mark style="color:purple;">**Privacy & Security**</mark> → <mark style="color:purple;">**Open Anyway**</mark>.

## Встановлення на Linux

У розділі <mark style="color:purple;">**Assets**</mark> доступні збірки `.AppImage`, `.deb` і `.rpm`. Щоб запустити AppImage, надайте файлу право на виконання:

```bash
chmod +x ShardBrowser.Launcher_<версія>_amd64.AppImage
./ShardBrowser.Launcher_<версія>_amd64.AppImage
```

Встановити пакет `.deb` можна командою:

```bash
sudo apt install ./ShardBrowser.Launcher_<версія>_amd64.deb
```

## Перший запуск

Після встановлення та запуску відкриється головний екран <mark style="color:purple;">**All profiles**</mark>. Ліворуч розташоване меню розділів: профілі, проксі, відбитки, розширення, закладки, автоматизація та кабінет ProxyShard.

<figure>
  <picture>
    <source srcset="../.gitbook/assets/shardbrowser-profiles-empty_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/shardbrowser-profiles-empty_white.png" alt="Головний екран ShardBrowser">
  </picture>
  <figcaption>Головний екран ShardBrowser</figcaption>
</figure>

---

## Додаємо проксі

Перейдіть до розділу <mark style="color:purple;">**Proxies**</mark> і натисніть <mark style="color:purple;">**+ Add proxies**</mark>.

<figure>
  <picture>
    <source srcset="../.gitbook/assets/shardbrowser-proxies-empty_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/shardbrowser-proxies-empty_white.png" alt="Розділ Proxies">
  </picture>
  <figcaption>Розділ Proxies</figcaption>
</figure>

У вікні <mark style="color:purple;">**Add proxies**</mark> виберіть тип у полі <mark style="color:purple;">**Type for lines without one**</mark> (за замовчуванням <mark style="color:purple;">SOCKS5</mark>) і вставте проксі по одному в рядок. Підтримувані формати:

```
host:port
host:port:user:pass
user:pass@host:port
socks5://user:pass@host:port
```

Рядки, що починаються з `#`, ігноруються. Проксі, які вже є у списку (той самий тип, хост, порт, логін і пароль), будуть пропущені.

<figure>
  <picture>
    <source srcset="../.gitbook/assets/shardbrowser-add-proxies-paste_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/shardbrowser-add-proxies-paste_white.png" alt="Вставте проксі по одному в рядок і натисніть «Preview»">
  </picture>
  <figcaption>Вставте проксі по одному в рядок і натисніть «Preview»</figcaption>
</figure>

Натисніть <mark style="color:purple;">**Preview**</mark>. У вікні попереднього перегляду натисніть <mark style="color:purple;">**Test all**</mark>, щоб перевірити проксі перед додаванням. Після тесту кожен проксі отримає статус і країну.

<figure>
  <picture>
    <source srcset="../.gitbook/assets/shardbrowser-add-proxies-preview_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/shardbrowser-add-proxies-preview_white.png" alt="Натисніть «Test all», потім «Add 1 proxy»">
  </picture>
  <figcaption>Натисніть «Test all», потім «Add 1 proxy»</figcaption>
</figure>

Проксі з міткою <mark style="color:purple;">**UDP**</mark> підтримують <mark style="color:purple;">SOCKS5 UDP</mark>, а отже і <mark style="color:purple;">WebRTC</mark>, що дуже корисно під час роботи із серйозними антифрод-системами. Якщо мітки <mark style="color:purple;">**UDP**</mark> немає, профіль переходить у режим <mark style="color:purple;">**TCP-only**</mark>: IP не витече, однак трафік може виглядати підозріло для просунутих антифрод-систем. Ми наполегливо радимо використовувати [проксі з підтримкою UDP](../our-products/about-udp/).

Кнопка <mark style="color:purple;">**Select working only**</mark> залишить вибраними лише робочі проксі. Натисніть <mark style="color:purple;">**Add 1 proxy**</mark> - проксі з'явиться у списку.

---

## Створюємо перший профіль

Перейдіть до розділу <mark style="color:purple;">**All profiles**</mark> і натисніть <mark style="color:purple;">**+ New profile**</mark>. Профіль також можна імпортувати з буфера обміну кнопкою <mark style="color:purple;">**Import from clipboard**</mark>.

<figure>
  <picture>
    <source srcset="../.gitbook/assets/shardbrowser-new-profile-button_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/shardbrowser-new-profile-button_white.png" alt="Розділ All profiles">
  </picture>
  <figcaption>Розділ All profiles</figcaption>
</figure>

Відкриється вікно <mark style="color:purple;">**New profile**</mark> із вкладками <mark style="color:purple;">**Basics**</mark>, <mark style="color:purple;">**Proxy**</mark>, <mark style="color:purple;">**Fingerprint**</mark> та <mark style="color:purple;">**Extensions**</mark>. На вкладці <mark style="color:purple;">**Basics**</mark> вкажіть ім'я профілю. Тут же можна вибрати папку, теги, колір, додати нотатку та завантажити файл cookies.

<figure>
  <picture>
    <source srcset="../.gitbook/assets/shardbrowser-new-profile-basics_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/shardbrowser-new-profile-basics_white.png" alt="Вкажіть ім'я профілю">
  </picture>
  <figcaption>Вкажіть ім'я профілю</figcaption>
</figure>

На вкладці <mark style="color:purple;">**Proxy**</mark> виберіть збережений проксі зі списку. Через <mark style="color:purple;">**+ Add a new proxy**</mark> можна одразу додати новий.

<figure>
  <picture>
    <source srcset="../.gitbook/assets/shardbrowser-new-profile-proxy_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/shardbrowser-new-profile-proxy_white.png" alt="Виберіть проксі для профілю">
  </picture>
  <figcaption>Виберіть проксі для профілю</figcaption>
</figure>

На вкладці <mark style="color:purple;">**Fingerprint**</mark> параметри змінювати не обов'язково - ShardBrowser сам підбере відбиток під вибрану ОС. За бажання виберіть <mark style="color:purple;">операційну систему</mark> (macOS, Windows, Linux, Android), конкретний відбиток, відеокарту, кількість ядер, пам'ять, частоту оновлення та роздільну здатність екрана.

<figure>
  <picture>
    <source srcset="../.gitbook/assets/shardbrowser-new-profile-fingerprint_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/shardbrowser-new-profile-fingerprint_white.png" alt="Налаштування відбитка профілю">
  </picture>
  <figcaption>Налаштування відбитка профілю</figcaption>
</figure>

Натисніть <mark style="color:purple;">**Create profile**</mark>.

---

## Запуск профілю

Профіль з'явиться у списку. Праворуч відкривається картка профілю: проксі, розширення, нотатки, параметри відбитка, часовий пояс і мова (за замовчуванням визначаються за проксі). Натисніть <mark style="color:purple;">**Start**</mark>.

<figure>
  <picture>
    <source srcset="../.gitbook/assets/shardbrowser-profile-start_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/shardbrowser-profile-start_white.png" alt="Натисніть «Start», щоб запустити профіль">
  </picture>
  <figcaption>Натисніть «Start», щоб запустити профіль</figcaption>
</figure>

Браузер запуститься з ізольованим відбитком і проксі. На стартовій сторінці `chrome://shardx` перелічено захисти профілю.

<figure>
  <picture>
    <source srcset="../.gitbook/assets/shardbrowser-profile-browser-started_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/shardbrowser-profile-browser-started_white.png" alt="Профіль запущено">
  </picture>
  <figcaption>Профіль запущено</figcaption>
</figure>

---

## Можливі проблеми

### Застосунок не запускається

Найімовірніше, не встановлено <mark style="color:purple;">Microsoft Edge WebView2 Runtime</mark>. Завантажте та встановіть його:

{% embed url="https://developer.microsoft.com/en-us/microsoft-edge/webview2/consumer" %}

В оригінальних образах Windows 10/11 WebView2 вже є. У полегшених збірках його можуть видалити.
