## Пакет контента для NGINX

Правила корреляции, входящие в пакет:

|Название|Источник событий|Тактика MITRE|Техника MITRE|Реализация|Версия KUMA|
|:----|:----|:----|:----|:----|:----|
|P520;NGINX;Попытки обойти механизм аутентификации API|nginx -> nginx_access|TA0001 (Initial Access)|T1190 (Exploit Public-Facing Application)|Для работы правила не требуется дополнительных настроек.|3.2.0.305|
|P521;NGINX;Обнаружена SQL-инъекция|nginx -> nginx_access|TA0001 (Initial Access)|T1190 (Exploit Public-Facing Application)|Для работы правила не требуется дополнительных настроек.|3.2.0.305|
|P522;NGINX;Обнаружен обход каталогов|nginx -> nginx_access|TA0001 (Initial Access)|T1190 (Exploit Public-Facing Application)|Для работы правила не требуется дополнительных настроек.|3.2.0.305|
|P523;NGINX;Атака форматирования строки|nginx -> nginx_access|TA0001 (Initial Access)|T1190 (Exploit Public-Facing Application)|Для работы правила не требуется дополнительных настроек.|3.2.0.305|
|P524;NGINX;Обнаружено внедрение кода|nginx -> nginx_access|TA0001 (Initial Access)|T1190 (Exploit Public-Facing Application)|Для работы правила не требуется дополнительных настроек.|3.2.0.305|

---

Нормализаторы, входящие в пакет:
|Название|Тип|Версия KUMA|Ресурсы|Последнее обновление|
|:----|:----|:----|:----|:----|
|NGINX Content Pack|regexp|Нормализатор: Nginx Regexp|3.2.0.305|02.08.2024|
