# Пакет контента для Mail
Правила корреляции, входящие в пакет Exchange:
|Название|Механизм обнаружения|Источник событий|Тактика MITRE|Техника MITRE|Реализация|Change log|Дата последнего изменения|Версия KUMA|
|---|---|---|---|---|---|---|---|---|
|P110;Exchange;Add mails to list|События от Exchange MTL с множеством получателей для одной темы письма|Exchange MTL|NA|NA|Для работы правила требуется в соответствующем нормализаторе настроить мапинг получателей на поле SA.DestinationUserName. Правило наполняет контекстную таблицу для правила P111||27.06.2024|3.2.0.305|
|P111;Exchange;Alerts by mails in list|Правило срабатывает при обнаружении большого количества получателей письма с одной темой от одного отправителя. Лимит получаетелей задается в словаре. Лимит по умолчанию в переменных.|Exchange MTL|||Для работы правила требуется в соответствующем нормализаторе настроить мапинг получателей на поле SA.DestinationUserName. Требуется включение правила P110. Требуется заполнение словаря адресами почт и их лимитами.||27.06.2024|3.2.0.305|