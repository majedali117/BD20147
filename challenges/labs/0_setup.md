### Add user
```
[ec2-user@ip-172-31-8-65 ~]$ sudo adduser neymar -u 2010
[ec2-user@ip-172-31-8-65 ~]$ sudo adduser ronaldo -u 2016
```
#Add Group
```
[ec2-user@ip-172-31-8-65 ~]$ sudo groupadd barca
[ec2-user@ip-172-31-8-65 ~]$ sudo groupadd merengues
```
### Add user to Group
```
[ec2-user@ip-172-31-8-65 ~]$ sudo usermod -a -G merengues neymar
```
### List password 
```
[ec2-user@ip-172-31-8-65 ~]$ cat /etc/passwd | grep neymar
neymar:x:2010:2010::/home/neymar:/bin/bash
[ec2-user@ip-172-31-8-65 ~]$ cat /etc/passwd | grep ronaldo
ronaldo:x:2016:2016::/home/ronaldo:/bin/bash
```
### List group entires
```
[ec2-user@ip-172-31-8-65 ~]$ cat /etc/group | grep barca
barca:x:2017:
[ec2-user@ip-172-31-8-65 ~]$ cat /etc/group | grep merengues
merengues:x:2018:neymar
[ec2-user@ip-172-31-8-65 ~]$

```
