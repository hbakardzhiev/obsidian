## WiFi with Iwd
#### Eduroam
`/etc/iwd/eduroam.8021x`: 
```
[Security]
EAP-Method=TTLS
EAP-Identity=anonymous@<uni.tld>
EAP-TTLS-Phase2-Method=Tunneled-PAP
EAP-TTLS-Phase2-Identity=<id>@<uni.tld>
EAP-TTLS-Phase2-Password=<password>

[Settings]
Autoconnect=true
```

### WPA2 Enterprise
`/etc/iwd/ssid.8021x`
```
[Security]
EAP-Method=PEAP
EAP-Identity=<anonymous identity>
EAP-PEAP-Phase2-Method=MSCHAPV2
EAP-PEAP-Phase2-Identity=<username>
EAP-PEAP-Phase2-Password=<password>

[Settings]
Autoconnect=true
```
