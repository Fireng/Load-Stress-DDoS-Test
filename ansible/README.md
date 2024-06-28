# [Ansible](https://docs.ansible.com/ansible/latest/getting_started/index.html)
система управления конфигурациями поможет нам для передачи команд множеству серверов

Ansible по умолчанию включает проверку ключей хоста. 
Проверка ключей хоста защищает от подмены сервера и атак "человек посередине".
Эту проверку можно выключить параметром host_key_checking = false в файле [ansible.cfg](https://github.com/Fireng/Load-Stress-DDoS-Test/blob/main/ansible/ansible.cfg)

В файлах:
1) [inventory.ini](https://github.com/Fireng/Load-Stress-DDoS-Test/blob/main/ansible/inventory.ini) хранятся айпи серверов с их входными данными, для передачи на них нужных нам файлов
2) [jmeter.yaml]() .yaml файлы описывают задачу, которую необходимо сделать при подключении к серверу(-ам). Именно этот файл отвечает за доставку jmeter

