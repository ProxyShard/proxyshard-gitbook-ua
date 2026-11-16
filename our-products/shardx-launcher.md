---
description: Встановлення, налаштування та можливості антидетект-браузера ShardBrowser
icon: browser
---

# ShardBrowser

<figure>
  <picture>
    <source srcset="../.gitbook/assets/shardbrowser-cover_black.svg" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/shardbrowser-cover_white.svg" alt="Логотип ShardBrowser">
  </picture>
</figure>

{% hint style="info" %}
ShardBrowser - антидетект-браузер на базі Chromium від команди ShardX. Кожен профіль отримує власний відбиток (fingerprint) реального пристрою та свій проксі, тому сайти бачать профілі як різні комп'ютери. Програма розповсюджується безкоштовно і постачається «як є». У разі серйозних проблем створіть баг-репорт на [GitHub](https://github.com/ProxyShard/ShardBrowser/issues).
{% endhint %}

Офіційний сайт ShardBrowser: [shardbrowser.com](https://shardbrowser.com/).

<figure><img src="../.gitbook/assets/shardbrowser-website.png" alt="Офіційний сайт ShardBrowser"><figcaption>Офіційний сайт ShardBrowser</figcaption></figure>

## Встановлення та налаштування

### Системні вимоги для Windows

| Компонент          | Мінімум                                | Рекомендовано                                  |
| ------------------ | -------------------------------------- | ---------------------------------------------- |
| ОС                 | Windows 10 22H2 або Windows 11, 64-біт | Windows 11 64-біт                              |
| Архітектура        | x64 / x86\_64                          | x64                                            |
| Процесор           | Двоядерний 64-біт, підтримка SSE3      | Чотириядерний і вище                           |
| ОЗП                | 4 ГБ                                   | 8 ГБ (16 ГБ при роботі з великою кількістю профілів) |
| Місце на диску     | 1 ГБ                                   | Від 5 ГБ                                       |
| Середовище виконання | Microsoft Edge WebView2              | Остання версія                                 |

---

### Встановлення на Windows

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

### Встановлення на macOS

У розділі <mark style="color:purple;">**Assets**</mark> завантажте <mark style="color:purple;">`ShardBrowser.Launcher_<версія>_aarch64.dmg`</mark>. Ця збірка призначена для комп'ютерів Mac із процесорами Apple Silicon.

Відкрийте файл `.dmg` і перетягніть <mark style="color:purple;">**ShardBrowser Launcher**</mark> до <mark style="color:purple;">**Applications**</mark>. Застосунок підписаний сертифікатом Apple Developer ID і нотаризований, тому відкривається як звичайний застосунок macOS.

### Встановлення на Linux

У розділі <mark style="color:purple;">**Assets**</mark> доступні збірки `.AppImage`, `.deb` і `.rpm`. Щоб запустити AppImage, надайте файлу право на виконання:

```bash
chmod +x ShardBrowser.Launcher_<версія>_amd64.AppImage
./ShardBrowser.Launcher_<версія>_amd64.AppImage
```

Встановити пакет `.deb` можна командою:

```bash
sudo apt install ./ShardBrowser.Launcher_<версія>_amd64.deb
```

### Перший запуск

Після встановлення та запуску відкриється головний екран <mark style="color:purple;">**All profiles**</mark>. Ліворуч розташоване меню розділів: профілі, проксі, відбитки, розширення, закладки, автоматизація та кабінет ShardX.

<figure>
  <picture>
    <source srcset="../.gitbook/assets/shardbrowser-profiles-empty_black.png" media="(prefers-color-scheme: dark)">
    <img src="../.gitbook/assets/shardbrowser-profiles-empty_white.png" alt="Головний екран ShardBrowser">
  </picture>
  <figcaption>Головний екран ShardBrowser</figcaption>
</figure>

---

### Додаємо проксі

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

Проксі з міткою <mark style="color:purple;">**UDP**</mark> підтримують <mark style="color:purple;">SOCKS5 UDP</mark>, а отже і <mark style="color:purple;">WebRTC</mark>, що дуже корисно під час роботи із серйозними антифрод-системами. Якщо мітки <mark style="color:purple;">**UDP**</mark> немає, профіль переходить у режим <mark style="color:purple;">**TCP-only**</mark>: IP не витече, однак трафік може виглядати підозріло для просунутих антифрод-систем. Ми наполегливо радимо використовувати [проксі з підтримкою UDP](about-udp/).

Кнопка <mark style="color:purple;">**Select working only**</mark> залишить вибраними лише робочі проксі. Натисніть <mark style="color:purple;">**Add 1 proxy**</mark> - проксі з'явиться у списку.

---

### Створюємо перший профіль

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

### Запуск профілю

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

### Можливі проблеми

#### Застосунок не запускається

Найімовірніше, не встановлено <mark style="color:purple;">Microsoft Edge WebView2 Runtime</mark>. Завантажте та встановіть його:

{% embed url="https://developer.microsoft.com/en-us/microsoft-edge/webview2/consumer" %}

В оригінальних образах Windows 10/11 WebView2 вже є. У полегшених збірках його можуть видалити.

## Можливості

ShardBrowser створює окремі профілі з унікальними відбитками, дає змогу призначати кожному профілю свій проксі та керувати десятками акаунтів як різними користувачами на різних пристроях. Локальне **API автоматизації** підтримує створення, запуск і керування профілями через Puppeteer / Playwright.

#### Що вміє ShardBrowser

* Генерує унікальні відбитки для <mark style="color:purple;">Windows</mark>, <mark style="color:purple;">macOS</mark> і <mark style="color:purple;">Linux</mark> (navigator, screen, client hints, WebGL / WebGPU тощо)
* Додає шум до окремих векторів: <mark style="color:purple;">canvas, WebGL, audio, client rects, шрифти, сенсори</mark>
* Підтримує необмежену кількість профілів, розкладених по папках
* Прив'язує проксі до профілю (<mark style="color:purple;">SOCKS5 / HTTP / HTTPS</mark>) та автоматично перевіряє його під час додавання
* Надає локальний **HTTP API** для повної автоматизації
* Підтримує керування через **CDP** (Chrome DevTools Protocol) у Puppeteer, Playwright та аналогах
* Дає змогу експортувати й імпортувати cookies між профілями
* Містить окремий **MCP-сервер**, через який профілем може керувати ШІ-агент

### Відбитки й антидетект

Для кожного профілю ShardBrowser підставляє узгоджений набір параметрів: User-Agent, платформу, кількість ядер та обсяг пам'яті (ніколи не більше реальної машини), роздільну здатність екрана, Sec-CH-UA тощо. Зверху накладається **шум** на окремі вектори: canvas, WebGL, audio, client rects, шрифти та сенсори. Кожен блок шуму вмикається незалежно, тому відбиток профілю стабільний у межах сесій, але відрізняється від інших профілів і від вашого реального пристрою.

{% hint style="info" %}
Відбиток генерується унікалізованим і не прив'язаний до заліза: кількість ядер CPU та обсяг RAM підганяються під хост і не завищуються, а екран обмежується розміром реального дисплея. Це знижує ризик виявлення через невідповідність параметрів.
{% endhint %}

### Проксі, QUIC та WebRTC

Під час **кожного** запуску профілю, ще до старту браузера, ShardBrowser у реальному часі перевіряє прив'язаний проксі на підтримку UDP-relay (SOCKS5 UDP\_ASSOCIATE):

* якщо UDP працює, вмикається <mark style="color:purple;">QUIC</mark>, а WebRTC використовує проксований UDP-relay;
* якщо UDP недоступний, QUIC вимикається, а WebRTC примусово переходить у режим **TCP-only**, щоб реальний IP не витік.

Поля часового поясу, локалі та геолокації в режимі `auto` також визначаються через проксі під час запуску.

{% hint style="success" %}
ShardBrowser разом із нашими [**проксі з UDP**](about-udp/) закриває витік WebRTC на рівні браузера: UDP-трафік іде через проксі, а не напряму з вашого IP. Детальніше читайте в розділі [**Про протокол UDP**](about-udp/).
{% endhint %}

### Автоматизація: локальний API

Усередині застосунку працює локальний HTTP-сервер на <mark style="color:purple;">**127.0.0.1**</mark> (порт за замовчуванням **40325**, змінюється в _Settings → Automation API_). Він доступний лише з вашого комп'ютера.

Усі запити, крім `GET /health`, вимагають **Bearer-токен** (постійний JWT із налаштувань):

```
Authorization: Bearer <token>
```

Кнопка **Regenerate token** у налаштуваннях миттєво змінює секрет: новий токен починає працювати одразу, а всі старі стають недійсними.

Типовий сценарій автоматизації:

1. `GET /fingerprint/new/{platform}` - отримати готовий унікалізований відбиток без збереження.
2. За потреби змінити відбиток, наприклад увімкнути шум для шрифтів або змінити режим WebRTC.
3. `POST /profiles` - створити профіль із цим відбитком і прив'язати проксі.
4. `POST /profiles/{id}/start` - запустити профіль і отримати **CDP-ендпоінт**.
5. Підключитися в Puppeteer / Playwright через `browserWSEndpoint = cdp.web_socket_debugger_url`.
6. `POST /profiles/{id}/stop` - закрити профіль.

{% hint style="info" %}
**Тимчасові профілі.** `POST /profiles/temporary` створює профіль із прапором `temporary`: він прихований із загального списку та інтерфейсу, а після закриття браузера видаляється автоматично разом із папкою даних. Це зручно для одноразових завдань.
{% endhint %}

Повний опис методів, моделей даних і прикладів дивіться у [специфікації API ShardX Launcher](https://docs.shardx.com/ua/shardx-launcher-api/binding-and-lifecycle).

### MCP-сервер для ШІ-агентів

Окремий **MCP-сервер** (Model Context Protocol) дає змогу ШІ-клієнту керувати лаунчером через API, а браузером профілю - через CDP. Це окремий Node-процес, а не частина HTTP API.

Завантажити його можна з лаунчера (_Settings → MCP server → Download MCP server_). Для налаштування потрібні `SHARDX_API` (базовий URL API) та `SHARDX_TOKEN` (Bearer-токен). MCP-сервер надає:

* **API-інструменти** для профілів, відбитків, проксі, папок, cookies, запуску та зупинки;
* **браузерні інструменти** поверх CDP для навігації, виконання JS, скриншотів, кліків, введення тексту, роботи з вкладками та очікування.

{% hint style="warning" %}
CDP (remote debugging) вмикається **лише** під час запуску профілю через API. Запуски з інтерфейсу залишаються без порту налагодження, тому антидетект не страждає.
{% endhint %}
