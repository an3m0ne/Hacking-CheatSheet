# AV Bypass
## Windows Defender
```powershell
Set-MpPreference -DisableRealtimeMonitoring $true  
Set-MpPreference -MAPSReporting Disable

Set-MpPreference -ExclusionPath /PATH/TO/FOLDER
```
