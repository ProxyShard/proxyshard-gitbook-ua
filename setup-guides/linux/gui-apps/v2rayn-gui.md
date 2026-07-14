# v2rayN GUI

{% hint style="success" %}
Дане рішення підтримує тунелювання UDP!
{% endhint %}

## Налаштування v2rayN.

Перейдіть по [посиланню](https://github.com/2dust/v2rayN/releases) для завантаження V2rayN

{% embed url="https://github.com/2dust/v2rayN/releases" %}

<figure><img src="../../../.gitbook/assets/image (244).png" alt=""><figcaption></figcaption></figure>

Або скачайте пакет через консоль

```bash
wget https://github.com/2dust/v2rayN/releases/download/7.14.12/v2rayN-linux-64.deb
```



## **Установка та запуск**

Виконайте установку завантаженого пакета через "<mark style="color:purple;">Discover</mark>" або встановіть через командний рядок

<figure><img src="../../../.gitbook/assets/Image00001 (11).PNG" alt=""><figcaption></figcaption></figure>

```bash
apt install ./v2rayN-linux-64.deb
```

Потім запустіть програму через "<mark style="color:purple;">Пуск</mark>" або командний рядок

<figure><img src="../../../.gitbook/assets/Image00002 (12).PNG" alt=""><figcaption></figcaption></figure>

{% code fullWidth="false" %}
```
v2ray
```
{% endcode %}

## **Налаштування профілю**

Створіть нову конфігурацію, вказавши SOCKS / HTTP як протокол підключення

<figure><img src="../../../.gitbook/assets/image (246).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
**З прикладом налаштування проксі ви можете ознайомитись у розділі [Інструкція з налаштування](../../getting-started.md)**
{% endhint %}

## **Налаштування профілю підключення**

Вставте скопійовані проксі із замовлення у відповідні поля, обов'язково вкажіть ядро ​​конфігурації (<mark style="color:purple;">Xray</mark> або <mark style="color:purple;">SingBox</mark>) та збережіть налаштування.

<figure><img src="../../../.gitbook/assets/Image00003 (6).PNG" alt=""><figcaption></figcaption></figure>

## Запуск клієнта

Запустіть клієнт, увімкнувши режим <mark style="color:purple;">Tun</mark>.

<figure><img src="../../../.gitbook/assets/image (245).png" alt=""><figcaption></figcaption></figure>

**Готово! Тепер ви можете повноцінно використовувати проксі, тунелюючи весь трафік на проксі.**
