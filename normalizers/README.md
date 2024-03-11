## Описание
Данный раздел содержит все нормализаторы для KUMA, разработанные и поддерживаемые сообществом KUMA.

Рекомендуется использовать данный раздел в качестве справочного. Для отслеживания изменений, а также загрузки одиночных нормализаторов используйте соответствующие подразделы.

## Содержание

### Файлы:

`normalizers.xlsx` - таблица с описанием нормализаторов (продублирована ниже в md формате)

`All Normalizers` - файл ресурсов со всеми нормализаторами для импорта в KUMA

### Директории:

[**Microsoft**](https://github.com/KUMA-Community/kuma_content/tree/main/normalizers/Microsoft) - нормализаторы для продуктов Microsoft

[**Linux**](https://github.com/KUMA-Community/kuma_content/tree/main/normalizers/Linux) - нормализаторы для Unix систем

[**Firewall**](https://github.com/KUMA-Community/kuma_content/tree/main/normalizers/Firewall) - нормализаторы для межсетевых экранов, NGFW и UTM

[**Network**](https://github.com/KUMA-Community/kuma_content/tree/main/normalizers/Network) - нормализаторы для сетевых устройств (коммутаторы, маршрутизаторы и т.п.), а также NTA-решений

[**Kaspersky**](https://github.com/KUMA-Community/kuma_content/tree/main/normalizers/Kaspersky) - нормализаторы для продуктов ЛК

[**Web**](https://github.com/KUMA-Community/kuma_content/tree/main/normalizers/Web) - нормализаторы для веб-серверов, а также WAF

[**Cloud + VM**](https://github.com/KUMA-Community/kuma_content/tree/main/normalizers/Cloud%20%2B%20VM) - нормализаторы для облачных решений и гипервизоров

[**Endpoint**](https://github.com/KUMA-Community/kuma_content/tree/main/normalizers/Endpoint) - нормализаторы для продуктов по защите конечных точек

[**Other**](https://github.com/KUMA-Community/kuma_content/tree/main/normalizers/Other) - нормализаторы для продуктов, не попавших в другие классификации (например, 1С)

## Нормализаторы

|Название                                   |Тип   |Версия KUMA|Ресурсы                                                                                                                                                                         |Последнее обновление|
|-------------------------------------------|------|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|
|VMware vCenter v7 (Syslog)                 |Syslog|2.1.1.73   |Нормализатор:  VMware vCenter v7 (Syslog)                                                                                                                                       |07.07.2023          |
|VMware vCenter (Syslog)                    |Syslog|2.1.1.73   |Нормализатор:  VMware vCenter (Syslog)                                                                                                                                          |07.08.2023          |
|zVirt + oVirt (Syslog)                     |regexp|2.1.1.73   |Нормализатор:  zVirt + oVirt (Syslog)                                                                                                                                           |11.01.2022          |
|[Deprecated] VMware ESXi (Syslog)          |Syslog|2.1.1.73   |Нормализатор:  [Deprecated] VMware ESXi (Syslog)                                                                                                                                |22.09.2023          |
|Yandex Cloud k8s (Syslog-JSON)             |Syslog|2.1.1.73   |Нормализатор: Yandex Cloud K8S (Syslog-JSON)                                                                                                                                    |25.07.2023          |
|Symantec Endpoint Protection (SQL)         |sql   |2.1.1.73   |Нормализатор: Symantec Endpoint Protection (SQL); Словари: SEP agent-behavior severity map, SEP_db.agent.name.map                                                               |07.02.2023          |
|SecretNet (SQL)                            |sql   |2.1.1.73   |Нормализатор: SecretNet (SQL)                                                                                                                                                   |18.09.2023          |
|Dallas Lock (KV)                           |regexp|2.1.1.73   |Нормализатор: Dallas Lock (KV)                                                                                                                                                  |22.09.2022          |
|Dr.Web Antivirus (SQL)                     |regexp|2.1.1.73   |Нормализатор: Dr.Web Antivirus (SQL)                                                                                                                                            |22.09.2022          |
|Dr.Web Other (SQL)                         |sql   |2.1.1.73   |Нормализатор: Dr.Web Other (SQL)                                                                                                                                                |22.09.2022          |
|Minerva EDR (Syslog-CEF)                   |regexp|2.1.1.73   |Нормализатор: Minerva EDR (Syslog-CEF)                                                                                                                                          |22.09.2022          |
|Citrix NetScaler (Syslog-KV)               |regexp|2.1.1.73   |Нормализатор: Citrix NetScaler (Syslog-KV)                                                                                                                                      |01.12.2022          |
|Sonicwall FW (CEF)                         |regexp|2.1.1.73   |Нормализатор: Sonicwall FW (CEF)                                                                                                                                                |04.07.2023          |
|WatchGuard Firebox (Syslog)                |Syslog|2.1.1.73   |Нормализатор: WatchGuard Firebox (Syslog)                                                                                                                                       |04.07.2023          |
|Check Point Quantum Spark 1800 (Syslog)    |Syslog|2.1.1.73   |Нормализатор: Check Point Quantum Spark 1800 (Syslog), Словари: IANAProtocol Numbers                                                                                            |04.07.2023          |
|HPE ArubaAP 8.11 (Syslog)                  |Syslog|2.1.1.73   |Нормализатор: HPE ArubaAP 8.11 (Syslog)                                                                                                                                         |07.07.2023          |
|Huawei USG (Syslog-KV)                     |regexp|2.1.1.73   |Нормализатор: Huawei USG Syslog                                                                                                                                                 |13.12.2023          |
|UserGate NGFW (CEF)                        |regexp|2.1.1.73   |Нормализатор: UserGate NGFW (CEF)                                                                                                                                               |27.09.2023          |
|Huawei Eudemon (Syslog-KV)                 |regexp|2.1.1.73   |Нормализатор: Huawei Eudemon (Syslog-KV)                                                                                                                                        |22.09.2022          |
|Kerio Control (Syslog)                     |Syslog|2.1.1.73   |Нормализатор: Kerio Control (Syslog)                                                                                                                                            |22.09.2022          |
|Интернет Контроль Сервер (Syslog)          |regexp|2.1.1.73   |Нормализатор: Интернет Контроль Сервер (Syslog)                                                                                                                                 |22.09.2022          |
|Palo Alto Global Protect (LEEF)            |regexp|2.1.1.73   |Нормализатор: Palo Alto Global Protect (LEEF)                                                                                                                                   |25.07.2023          |
|Sophos XG Firewall + UTM (KV)              |regexp|2.1.1.73   |Нормализатор: Sophos XG Firewall + UTM (KV)                                                                                                                                     |28.06.2023          |
|Check Point (Syslog-KV)                    |regexp|2.1.1.73   |Нормализатор: Check Point (Syslog-KV)                                                                                                                                           |28.10.2022          |
|КриптоПро NGate (JSON)                     |json  |2.1.1.73   |Нормализатор: КриптоПро NGate (JSON)                                                                                                                                            |29.11.2022          |
|KEDR (JSON)                                |json  |2.1.1.73   |Нормализатор: KEDR (JSON); Словари: KEDR.FileAttributes, KEDR.FileType, KEDR.FileOperatiomType, KEDR.RegistryOperationType, KEDR.AccountType, KEDR.Protocol, KEDR.IntegrityLevel|03.11.2022          |
|KSE (SQL)                                  |sql   |2.1.1.73   |Нормализатор: KSE (SQL)                                                                                                                                                         |07.11.2022          |
|KSC (SQL)                                  |sql   |2.1.1.73   |Нормализатор: KSC (SQL)                                                                                                                                                         |17.01.2022          |
|KSC Cloud Console (KV)                     |regexp|2.1.1.73   |Нормализатор: KSC Cloud Console (KV)                                                                                                                                            |20.10.2022          |
|KCS (Syslog-CEF)                           |regexp|2.1.1.73   |Нормализатор: KCS (Syslog-CEF)                                                                                                                                                  |09.10.2023          |
|Unix Logstash (Syslog-JSON)                |regexp|2.1.1.73   |Нормализатор: Unix Logstash (Syslog-JSON)                                                                                                                                       |04.08.2023          |
|auditd (Regexp)                            |Syslog|2.1.1.73   |Нормализатор: auditd (Regexp); Словари: sesact, AuditD Sycall types for x64                                                                                                     |07.07.2023          |
|auditd Beats Agent (JSON)                  |json  |2.1.1.73   |Нормализатор: auditd Beats Agent (JSON)                                                                                                                                         |20.10.2022          |
|auditd (Syslog-Regexp)                     |regexp|2.1.1.73   |Нормализатор: auditd (Syslog-Regexp); Словари: sesact, AuditD Sycall types for x64                                                                                              |16.02.2024          |
|Windows Events + Sysmon (XML)              |xml   |2.1.1.73   |Нормализатор: Windows Events + Sysmon (XML); Словари: MS Event_IDs-Names, MS (ImpersonationLevels - 4624), MS (ResultCodes - 4768 and 4769), MS (FailureCodes - 4625)           |03.07.2023          |
|Windows Firewall (Regexp)                  |regexp|2.1.1.73   |Нормализатор: Windows Firewall (Regexp)                                                                                                                                         |07.07.2023          |
|Windows PowerShell (Regexp)                |regexp|2.1.1.73   |Нормализатор: Windows PowerShell (Regexp)                                                                                                                                       |07.07.2023          |
|Windows DNS-Server (Regexp)                |regexp|2.1.1.73   |Нормализатор: Windows DNS-Server (Regexp); Словарь: DNS_Opcodes                                                                                                                 |09.01.2023          |
|IIS Exchange Log File Format (CSV)         |csv   |2.1.1.73   |Нормализатор: IIS Exchange Log File Format (CSV)                                                                                                                                |12.05.2023          |
|Windows Server Essentials Experience (JSON)|regexp|2.1.1.73   |Нормализатор: Windows Server Essentials Experience (JSON)                                                                                                                       |22.09.2022          |
|Windows Logstash (JSON)                    |json  |2.1.1.73   |Нормализатор: Windows Logstash (JSON)                                                                                                                                           |30.11.2022          |
|PTsecurity NAD (JSON)                      |regexp|2.1.1.73   |Нормализатор: PTsecurity NAD (JSON)                                                                                                                                             |03.07.2023          |
|PTsecurity NAD 11 (Syslog)                 |regexp|2.1.1.73   |Нормализатор: PTsecurity NAD 11 (Syslog)                                                                                                                                        |07.07.2023          |
|Mikrotik (Syslog)                          |regexp|2.1.1.73   |Нормализатор: Mikrotik (Syslog)                                                                                                                                                 |12.05.2023          |
|Biforcom MCR (Regexp)                      |regexp|2.1.1.73   |Нормализатор: Biforcom MCR (Regexp)                                                                                                                                             |20.12.2022          |
|Гарда Монитор (Regexp)                     |syslog|2.1.1.73   |Нормализатор: Гарда Монитор (Regexp)                                                                                                                                            |30.01.2024          |
|Cisco Universal (Syslog)                   |regexp|2.1.1.73   |Нормализатор: Cisco Universal (Syslog)                                                                                                                                          |26.02.2024          |
|AhnLab AIPS (CSV)                          |regexp|2.1.1.73   |Нормализатор: AhnLab AIPS (CSV)                                                                                                                                                 |22.09.2022          |
|sFlow Logstash (JSON)                      |json  |2.1.1.73   |Нормализатор: sFlow Logstash (JSON)                                                                                                                                             |22.09.2022          |
|Eltex MES (Regexp)                         |regexp|2.1.1.73   |Нормализатор: Eltex MES (Regexp)                                                                                                                                                |23.11.2022          |
|Fudo Security PAM (Syslog)                 |regexp|2.1.1.73   |Нормализатор: Fudo Security PAM (Syslog)                                                                                                                                        |01.12.2022          |
|InfoWatch Traffic Monitor (SQL)            |sql   |2.1.1.73   |Нормализатор: InfoWatch Traffic Monitor (SQL)                                                                                                                                   |03.11.2022          |
|NetApp ONTAP (XML)                         |regexp|2.1.1.73   |Нормализатор: NetApp ONTAP (XML)                                                                                                                                                |07.02.2023          |
|SAP (Regexp)                               |regexp|2.1.1.73   |Нормализатор: SAP (Regexp)                                                                                                                                                      |07.02.2023          |
|Стахановец DLP (SQL)                       |sql   |2.1.1.73   |Нормализатор: Стахановец DLP (SQL)                                                                                                                                              |25.09.2023          |
|BIND (Syslog)                              |Syslog|2.1.1.73   |Нормализатор: BIND (Syslog); Словарь: DNS Request Types                                                                                                                         |15.02.2024          |
|FortiMail (KV)                             |regexp|2.1.1.73   |Нормализатор: FortiMail (KV)                                                                                                                                                    |22.09.2022          |
|MITIGATOR (KV)                             |regexp|2.1.1.73   |Нормализатор: MITIGATOR (KV)                                                                                                                                                    |22.09.2022          |
|Nokia VitalQIP (Syslog)                    |regexp|2.1.1.73   |Нормализатор: Nokia VitalQIP (Syslog)                                                                                                                                           |22.09.2022          |
|OpenVAS (CSV)                              |csv   |2.1.1.73   |Нормализатор: OpenVAS (CSV)                                                                                                                                                     |22.09.2022          |
|Radware DefensePro (Regexp)                |regexp|2.1.1.73   |Нормализатор: Radware DefensePro (Regexp)                                                                                                                                       |22.09.2022          |
|Windchill FRACAS (Regexp)                  |regexp|2.1.1.73   |Нормализатор: Windchill FRACAS (Regexp)                                                                                                                                         |22.09.2022          |
|OWA,EAS,MAPI (CSV)                         |csv   |2.1.1.73   |Нормализатор: OWA,EAS,MAPI (CSV)                                                                                                                                                |24.01.2023          |
|1C (JSON)                                  |json  |2.1.1.73   |Нормализатор: 1C (JSON)                                                                                                                                                         |25.07.2023          |
|PTsecurity ISIM (CSV)                      |regexp|2.1.1.73   |Нормализатор: PTsecurity ISIM (CSV)                                                                                                                                             |27.02.2023          |
|PTsecurity Sandbox (JSON)                  |regexp|2.1.1.73   |Нормализатор: PTsecurity Sandbox (JSON)                                                                                                                                         |31.10.2022          |
|PTsecurity AF 3.7 (CEF)                    |regexp|2.1.1.73   |Нормализатор: PTsecurity AF 3.7 (CEF)                                                                                                                                           |07.07.2023          |
|McAfee Web Gateway (CEF)                   |regexp|2.1.1.73   |Нормализатор: McAfee Web Gateway (CEF)                                                                                                                                          |21.09.2023          |
|Blue Coat ProxySG (Syslog)                 |regexp|2.1.1.73   |Нормализатор: Blue Coat ProxySG (Syslog)                                                                                                                                        |27.11.2023          |
|Blue Coat ProxySG (CSV)                    |regexp|2.1.1.73   |Нормализатор: Blue Coat ProxySG (CSV)                                                                                                                                           |22.09.2022          |
|Blue Coat ProxySG (KV)                     |regexp|2.1.1.73   |Нормализатор: Blue Coat ProxySG (KV)                                                                                                                                            |22.09.2022          |
|Zecurion SWG (CEF)                         |regexp|2.1.1.73   |Нормализатор: Zecurion SWG (CEF)                                                                                                                                                |28.07.2023          |
