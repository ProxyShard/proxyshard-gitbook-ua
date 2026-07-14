# ClashX

{% hint style="success" %}
Дане рішення підтримує тунелювання UDP!
{% endhint %}

## Налаштування **ClashX**

Вам необхідно перейти на офіційний GitHub проекту ClashX та завантажити необхідну версію архіву для вашої ОС. У прикладі наведено налаштування на Windows ([Clash.for.Windows-0.20.39-win.7z](https://github.com/lantongxue/clash_for_windows_pkg/releases/download/0.20.39/Clash.for.Windows-0.20.39-win.7z)).

{% embed url="https://github.com/lantongxue/clash_for_windows_pkg/releases" %}

<figure><img src="../../.gitbook/assets/image (170).png" alt=""><figcaption></figcaption></figure>

## **Запуск ClashX**

Потім необхідно розпакувати архів і запустити від імені _<mark style="color:red;">**адміністратора**</mark>_ "Clash for Windows.exe" як наведено на прикладі нижче:

<figure><img src="../../.gitbook/assets/image (172).png" alt="" width="563"><figcaption><p>Розпакування архіву на робочий стіл</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (162).png" alt="" width="375"><figcaption><p>Запуск від імені адміністратора</p></figcaption></figure>

## **Налаштування програми**

Після запуску програми необхідно перейти в "<mark style="color:purple;">Profiles</mark>" та відкрити редактор файлу <mark style="color:purple;">config.yaml</mark>

<figure><img src="../../.gitbook/assets/image (159).png" alt="" width="375"><figcaption></figcaption></figure>

## **Налаштування конфігураційного файлу**

Наведіть конфігурацію файлу як у прикладі нижче, вказавши ваші проксі із замовлення:

```yaml
proxies:
  - name: "ProxyShard-Germany-testname"
    type: socks5
    server: 123.123.123.123
    port: 1234
    username: proxy_login
    password: password_login
    udp: true

proxy-groups:
  - name: "Auto"
    type: select
    proxies:
      - ProxyShard-Germany-testname

rules:
  - PROCESS-NAME,chrome.exe,Auto
  - MATCH,DIRECT
```

Зрештою у вас має вийде приблизно так:

<figure><img src="../../.gitbook/assets/image (158).png" alt="" width="563"><figcaption><p>Приклад конфігурації</p></figcaption></figure>

{% hint style="info" %}
**З прикладом налаштування проксі ви можете ознайомитись у розділі [Інструкція з налаштування](../getting-started.md)**
{% endhint %}

<pre><code>proxies:
  - name: "ProxyShard-Germany-testname" | Тут ви задаєте ім'я проксі
    тип: socks5 | Тип протоколу
    server: 123.123.123.123 | Адреса або домен проксі
    port: 1234 | Порт проксі
    username: proxy_login | Логін проксі
    password: password_login | Пароль проксі
    udp: true                                  
proxy-groups:
  - name: "Auto"
    type: select
    proxies:
      - ProxyShard-Germany-testname              

rules:
  - PROCESS-NAME,<a data-footnote-ref href="#user-content-fn-1">chrome.exe</a>,Auto | Вибір певної програми для проксування
  - MATCH,DIRECT | У нашому прикладі використовується браузер хрому,
                      | але це може бути будь-яка ваша програма, наприклад discord.exe
                      | - MATCH,DIRECT : Вказує, що весь трафік який не є хромом
                      | буде перенаправлено не на проксі, а на ваш основний інтерфейс
</code></pre>

## **Перевірка конфігурації**

Після налаштування конфігурації, вам необхідно відкрити Proxies і вибрати опцію Global і провести перевірку вашого налаштованого конфігу з 4 пункту.

<figure><img src="../../.gitbook/assets/image (160).png" alt="" width="563"><figcaption></figcaption></figure>

Якщо перевірка не пройшла і у вас "Failed", звіртеся з конфігураційним файлом і переконайтеся, що всі вказані дані від проксі вірно введені. Якщо налаштування правильні, ви отримаєте успішне виведення перевірки як на скріншоті знизу.

<figure><img src="../../.gitbook/assets/image (161).png" alt=""><figcaption></figcaption></figure>

## **Встановлення та включення TAP-інтерфейсу**

Далі перейдіть на "General" і здійсніть встановлення TAP-інтерфейсу на свій комп'ютер, він створить новий інтерфейс, до якого буде прив'язана проксі.

Після встановлення TUN-інтерфейсу вам необхідно включити TUN Mode, як на скріншоті у 4-й рамці

<figure><img src="../../.gitbook/assets/image (163).png" alt="" width="563"><figcaption></figcaption></figure>

## **Перевірка працездатності**

Якщо все успішно запустилося, ви можете відкрити вашу цікаву програму, для якої ви налаштовували конфіг (4 пункт) і можна радіти роботі ваших програм з можливістю проксування UDP трафіку! <br>

У нашому прикладі проксіювання виконувалося для Chrome, і результат можна перевірити на [чекерах](../../our-products/about-udp/webrtc-leak-check-tools.md).

<figure><img src="../../.gitbook/assets/image (164).png" alt="" width="563"><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (165).png" alt="" width="563"><figcaption></figcaption></figure>

Якщо перевірка або проксіювання [не працює ](../../faq-and-support/faq/proxy-not-working.md), переконайтеся, що ви точно запустили ClashX від імені адміністратора і з 4 по 6 пункт виконано правильно.

## **Додатково. Додавання безлічі проксі та перемикання між ними**

Вам необхідно, для можливості швидкого перемикання між проксі, доповнити новими конфігурацію проксі з пункту 4. Імена "ProxyShard-DE-testname1" є довільними і можна вказати на ваш вибір.

Головним моментом після додавання є вказівка ​​проксі також і для "proxy-group", як показано нижче:

```yaml
proxies:
  - name: "ProxyShard-DE-testname1"
    type: socks5
    server: 123.123.123.123
    port: 42651
    username: LOgin
    password: pasSSWORD
    udp: true
    
  - name: "ProxyShard-NL-testname2"
    type: socks5
    server: 123.123.123.123
    port: 42651
    username: LOgin
    password: pasSSWORD
    udp: true

  - name: "ProxyShard-RO-testname3"
    type: socks5
    server: 123.123.123.123
    port: 42651
    username: LOgin
    password: pasSSWORD
    udp: true

proxy-groups:
  - name: "Auto"
    type: select
    proxies:
      - ProxyShard-DE-testname1
      - ProxyShard-NL-testname2
      - ProxyShard-RO-testname3

rules:
  - PROCESS-NAME,chrome.exe,Auto
  - MATCH,DIRECT
```

Якщо ви всі вірно вказали, у вас з'являться додаткові точки підключення в "Proxies" і в залежності від вибраного профілю налаштувань (просто натиснути на будь-яку), буде здійснено підключення.

<figure><img src="../../.gitbook/assets/image (166).png" alt=""><figcaption></figcaption></figure>

[^1]: додаток для проксування
