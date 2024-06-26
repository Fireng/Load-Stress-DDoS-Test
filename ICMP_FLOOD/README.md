# ICMP FLOOD
Нацелена на приведение сервера к отказу за счет конкретного приложения — утилиты PING и ее аналогов. Во время Ping Flood на сервер-жертву приходит большое количество ICMP Echo-Request пакетов с широкого диапазона IP-адресов, что ведет к падению производительности сервера и занятию полосы пропускания. Это также может служить причиной недоступности сети.
Поскольку поток запросов идет с широкого диапазона IP-адресов (как реальных, так и поддельных) идентифицировать легитимные ICMP Echo-Request пакеты становится почти невозможно. Способ защиты от данной атаки идентичен защите от ICMP Flood. Также можно заблокировать на маршрутизаторе только ICMP-ECHO или установить ограничения по числу пакетов в единицу времени.
```
ping -f -l ${__P(byte_count)} ${__P(target_ip)}
```

![icmp_flood](https://github.com/Fireng/Load-Stress-DDoS-Test/blob/main/assets/images/ICMP_Exmp.png)
