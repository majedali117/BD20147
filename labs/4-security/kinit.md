## Add new User with following command
```
[majed@vm1 ~]$ kadmin.local
Couldn't open log file /var/log/kadmind.log: Permission denied
Authenticating as principal majed/admin@MAJEDALI with password.
kadmin.local: Permission denied while initializing kadmin.local interface
[majed@vm1 ~]$ sudo kadmin.local
Authenticating as principal raffles/admin@MAJEDALI with password.
kadmin.local:  addprinc -pw majed majed@MAJEDALI
WARNING: no policy specified for majed@MAJEDALI; defaulting to no policy
Principal "majed@MAJEDALI" created.
kadmin.local:  exit
```
### listing credentials and ticket lifetime
```
[majed@vm1 ~]$ kinit majed
Password for majed@MAJEDALI:
[majed@vm1 ~]$ klist
Ticket cache: FILE:/tmp/krb5cc_500
Default principal: majed@MAJEDALI

Valid starting     Expires            Service principal
06/16/17 00:05:59  06/17/17 00:05:59  krbtgt/MAJEDALI@MAJEDALI
        renew until 06/16/17 00:05:59
[majed@vm1 ~]$
```
