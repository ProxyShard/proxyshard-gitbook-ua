# Proxychain

## Налаштування Proxychains4

Встановіть пакет proxychains4 з репозиторію

```bash
apt install proxychains4
```

## **Налаштування конфігурації**

Відкрийте конфігурацію на шляху <mark style="color:$info;">**/etc/proxychains4.conf**</mark>, в ньому вкажіть протокол та дані для підключення до проксі

<figure><img src="../../../.gitbook/assets/image (247).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
**З прикладом налаштування проксі ви можете ознайомитись у розділі [Інструкція з налаштування](../../getting-started.md)**
{% endhint %}

## **Перевірка роботи**

Після вказівки налаштувань підключення ви перевірите працездатність через звернення на сайт ifconfig.me

```
proxychains curl ifconfig.me
```

**Якщо перевірка підтвердила зміну вашої IP-адреси, то тепер ви можете розпочати використання ваших проксі!**
