# DNS FLOOD
Атака, направленная на перегрузку сервера DNS-запросами, что может привести к невозможности проведения нормального разрешения DNS-имен. При проведении нагрузочного тестирования DNS FLOOD, система анализируется на способность эффективно обрабатывать высокий объем DNS-запросов, поддерживать доступность и предотвращать отказ в обслуживании.
Для проведения атаки DNS FLOOD в рамках нагрузочного тестирования, можно использовать инструменты, способные отправлять большое количество DNS-запросов к серверу. Например, инструменты как [dnsperf](https://github.com/DNS-OARC/dnsperf) или [dnsblast](https://github.com/jedisct1/dnsblast) могут быть использованы для генерации высокой нагрузки на DNS-сервер.

#### Метод реализации
Через сервис [whois](https://www.nic.ru/whois/) узнаем какой у домена dns сервер 

Пример реализации через [jmeter](https://github.com/Fireng/Load-Stress-DDoS-Test/blob/main/DNS_FLOOD/DNS_FLOOD.jmx)
![dns_jmeter](https://github.com/Fireng/Load-Stress-DDoS-Test/blob/main/assets/images/DNS_Jmeter.png)
