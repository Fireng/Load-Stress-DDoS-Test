# NTP FLOOD
Один из вариантов UDP-флуда, DoS-атака на серверы, использующие протокол NTP (Network Time Protocol), применяемый для синхронизации внутренних часов компьютеров. Чрезмерная нагрузка на NTP-сервер создается путем отправки множества поддельных NTP-запросов с большого количества разных IP-адресов.

#### Метод реализации
Запустите командную строку и введите **w32tm /stripchart /computer:${your_domain}** и нажмите Enter. Чтобы остановить отображение времени, нажмите Ctrl + C.
![w32tm_example](https://github.com/Fireng/Load-Stress-DDoS-Test/blob/main/assets/images/w32tm_check_time.png)

Вернитесь в Wireshark, чтобы просмотреть запросы NTP и ответы на них.
Скопируйте данные шестнадцатеричного потока из запроса NTP и вставьте их в запрос JMeter UDP. На рисунке ниже представлен запрос NTP для time.windows.com.
![ntp_flood_code](https://github.com/Fireng/Load-Stress-DDoS-Test/blob/main/assets/images/NTP_FLOOD_Exmp.png)

Сформируйте запрос JMeter UDP 
![ntp_jmeter](https://github.com/Fireng/Load-Stress-DDoS-Test/blob/main/assets/images/NTP_Jmeter.png)

Если вы продолжите выполнять запросы NTP, вы увидите, что данные ответа меняются. Это потому, что в каждом экземпляре меняется текущая временная метка. Все ответы будут даны в формате UTC.

[Пример готового кода](https://github.com/Fireng/Load-Stress-DDoS-Test/blob/main/NTP_FLOOD/NTP_FLOOD.jmx)

Доп. Материал: https://ab57.ru/cmdlist/w32tm.html
