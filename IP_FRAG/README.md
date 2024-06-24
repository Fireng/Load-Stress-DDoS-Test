# IP_FRAG Attack

Тип атаки, при которой злоумышленник отправляет фрагментированные IP-пакеты, занимающие значительные ресурсы для их сборки и обработки. Проведение нагрузочного тестирования с использованием IP FRAG ATTACK позволяет выявить уязвимости в обработке фрагментированных пакетов системой, оценить ее степень устойчивости к такого рода атакам и принять меры по усилению защиты.

#### Методы реализации
Для эмуляции IP FRAG Attack можно использовать такие инструменты, как hping3, Scapy, nmap, metasploit:
```
hping3 TARGET_IP --icmp --frag 16
```

```
rom scapy.all import * 
 
# Создание фрагментированного IP-пакета 
ip = IP(dst="192.168.1.1", flags=1, frag=0, id=1000)  # Устанавливаем флаг DF (Don't Fragment) и идентификатор 
icmp = ICMP()  # Создаем ICMP пакет для вложения в IP-пакет 
 
packet = ip/icmp  # Собираем IP пакет с ICMP заголовком 
 
# Фрагментирование пакета 
fragments = fragment(packet, fragsize=100) 
 
# Отправка фрагментированных пакетов 
send(fragments) 
```

```
nmap -sS -p 80 -f 192.168.1.1
```

В Jmeter описан метод с использованием nmap
![IP Frag Attack example img](https://github.com/Fireng/Load-Stress-DDoS-Test/blob/main/assets/images/IP_FRAG_Exmp.png)