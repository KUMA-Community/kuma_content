# Пакет контента для General Rules
Правила корреляции, входящие в пакет:
|Название                                                                  |Механизм обнаружения                                                                                                                                                                         |Источник событий                                       |Тактика MITRE     |Техника MITRE                    |Реализация                                                                                                                                                                                                                    |Change log                                                                                                                                    |Дата последнего изменения|Версия KUMA|
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|------------------|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|-----------|
|P100;General;Запуск потенциального ВПО (на основе имени файла)            |Запуск файла с подозрительным именем (проверка фильтром по более 700 регулярным выражениям)                                                                                                  |All events -> File Name                                |-                 |-                                |Для работы правила не требуется дополнительных настроек.                                                                                                                                                                      |                                                                                                                                              |16.06.2023               |2.1.1.73   |
|P101;General;Обнаружено сканирование портов (Вертикальное)                |Правило позволяет обнаруживать перебор уникальных 30 портов на одном хосте в течение 60 сек.                                                                                                 |FW -> Traffic log  Check Point Palo Alto Fortinet Cisco|TA0007 (Discovery)|T1046 (Network Service Discovery)|Для работы правила необходимо наполнить словарь "Exclusion;General port Scan (Vertical)"  IP-адресами хостов, которые выполняют функционал сканирования и инвентаризации сети для исключения ложных срабатываний.             |В условиях правила активный лист "Exclusion;General port Scan (Vertical)" заменен на словарь "Exclusion;General port Scan (Vertical)"         |16.06.2023               |2.1.1.73   |
|P102;General;Обнаружено сканирование портов (Горизонтальное)              |Правило позволяет обнаруживать перебор уникальных 30 хостов по одному порту в течение 60 сек.                                                                                                |FW -> Traffic log  Check Point Palo Alto Fortinet Cisco|TA0007 (Discovery)|T1046 (Network Service Discovery)|Для работы правила необходимо наполнить словарь "Exclusion;General port Scan (Horizontal)"  IP-адресами хостов, которые выполняют функционал сканирования и инвентаризации сети для исключения ложных срабатываний.           |В условиях правила активный лист "Exclusion;General port Scan (Horizontal)" заменен на словарь "Exclusion;General port Scan (Horizontal)"     |16.06.2023               |2.1.1.73   |
|P103;General;Обращение к домену 3-го уровня и выше                        |Правило обнаруживает доменные имена 3 и более уровней (вложенности) на любом языке. Предварительно нужно настроить значение DeviceVendor в селекторе.                                        |URL -> Regex                                           |-                 |-                                |Для работы правила не требуется дополнительных настроек.                                                                                                                                                                      |                                                                                                                                              |16.06.2023               |2.1.1.73   |
|P104;General; Netflow подключения к портам - Баз данных                   |Правило позволяет обнаруживать подключения внутренних IP-адресов к серверам баз данных, расположенных за пределами организации, по портам: 1433, 1434, 1521, 3306, 5432, 9200                |Netflow                                                |-                 |-                                |Для работы правила необходимо наполнить словарь "Database servers" внешними IP-адресами серверов баз данных, расположенных за пределами организации и к которым разрешено подключение, с целью исключения ложных срабатываний.|В условиях правила активный лист "Database servers" заменен на словарь "Database servers"                                                     |                         |2.1.1.73   |
|P105;General; Netflow подключения к портам - Почтовые сервера             |Правило позволяет обнаруживать подключения внутренних IP-адресов к почтовым серверам, расположенных за пределами организации, по портам: 25, 465, 587, 143, 993, 110, 995                    |Netflow                                                |-                 |-                                |Для работы правила необходимо наполнить словарь "Mail servers" внешними IP-адресами почтовых серверов, расположенных за пределами организации и к которым разрешено подключение, с целью исключения ложных срабатываний.      |В условиях правила активный лист "Mail servers" заменен на словарь "Mail servers"                                                             |                         |2.1.1.73   |
|P106;General; Netflow подключение извне по RDP,SSH,FTP                    |Правило обнаруживает подключения извне (белый IP) во внутреннюю сеть по Netflow по портам 22, 3389, 20                                                                                       |Netflow                                                |-                 |-                                |Для работы правила не требуется дополнительных настроек.                                                                                                                                                                      |                                                                                                                                              |                         |2.1.1.73   |
|P107;General; Netflow подключение из внутренеей сети наружу по RDP,SSH,FTP|Правило обнаруживает подключения  из внутренеей сети на белый IP во внутреннюю сеть по Netflow по портам 22, 3389, 20                                                                        |Netflow                                                |-                 |-                                |Для работы правила не требуется дополнительных настроек.                                                                                                                                                                      |                                                                                                                                              |                         |2.1.1.73   |
|P108;General; Netflow Входящее соединение на адрес из черного списка      |Правило позволяет обнаруживать подключения внешнего вредоносного IP-адреса, находящего в "черном списке" или в репутационном списке ЛК (KL_IP_Reputation), к хостам защищаемой инфраструктуры|Любой                                                  |-                 |-                                |Для работы правила необходимо настроить обогащение событий информацией об индикаторах компрометации CyberTrace и/или наполнить словарь "IP Blacklist" вредоносными IP-адресами.                                               |*Переименован активный лист "IP black list" в "IP Blacklist" В условиях правила активный лист "IP Blacklist" заменен на словарь "IP Blacklist"|                         |2.1.1.73   |
|P109;General; Netflow Исходящее соединение на адрес из черного списка     |Правило позволяет обнаруживать подключения внутренних хостов к внешнему вредоносному IP-адресу, находящемуся в "черном списке" или в репутационном списке ЛК (KL_IP_Reputation)              |Любой                                                  |-                 |-                                |Для работы правила необходимо настроить обогащение событий информацией об индикаторах компрометации CyberTrace и/или наполнить словарь "IP Blacklist" вредоносными IP-адресами.                                               |*Переименован активный лист "IP black list" в "IP Blacklist" В условиях правила активный лист "IP Blacklist" заменен на словарь "IP Blacklist"|                         |2.1.1.73   |