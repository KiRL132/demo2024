# demo2024
1. Выполните базовую настройку всех устройств:
     - a. Соберите тапологию согласно рисунку. Все устройства работают на ОС Linux - Debian
     - b. Присвоить имена в соответствии с топологией
     - c. Рассчитайте IP-адресацию IPv4 и IPv6. Необходимо заполнить таблицу №1. При необходимости отредактируйте таблицу.
     - d. Пул адресов для сети офиса BRANCH - не более 16. Для IPv6 пропустите этот пункт.
     - e. Пул адресов для сети офиса HQ - не более 64. Для IPv6 пропустите этот пункт.

Топология:
![alt text](https://imgur.com/a/oJC5Ble)

| Имя устройства | Интерфейс | IPv4/IPv6 | Маска/префикс | Шлюз |
| ----------- | ----------- | ----------- | ----------- | ----------- |
| ISP         | enn         | 10.10.12.10      | **24/** 255.255.255.0       |  10.12.12.254  |
|             | enn         | 192.168.0.162    | **30/** 255.255.255.252    |    |
|             | enn         | 192.168.0.166    | **30/** 255.255.255.252    |    |
| HQ-R        | enn         | 192.168.0.161    | **30/** 255.255.255.252    |  192.168.0.162  |
|             | enn         | 192.168.0.1      | **25/** 255.255.255.128    |    |
| BR-R        | enn         | 192.168.0.165    | **30/** 255.255.255.252    |  192.168.0.166  |
|             | enn         | 192.168.0.129    | **27/** 255.255.255.128    |    |
| HQ-SRV      | enn         | 192.168.0.126    | **25/** 255.255.255.128    |  192.168.0.1  |
| BR-SRV      | enn         | 192.168.0.158    | **27/** 255.255.255.224    |  192.168.0.129  |
