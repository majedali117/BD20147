Microsoft Windows [Version 10.0.14393]
(c) 2016 Microsoft Corporation. All rights reserved.
C:\windows\system32>bash
majedalibash@WINDOWS-BSP279E:/mnt/c/Windows/System32$ ssh majedali@52.166.5.224
The authenticity of host '52.166.5.224 (52.166.5.224)' can't be established.
RSA key fingerprint is 16:ce:c8:df:15:d6:79:81:36:6d:36:c1:56:b3:1c:0a.
Are you sure you want to continue connecting (yes/no)? yes
Warning: Permanently added '52.166.5.224' (RSA) to the list of known hosts.
majedali@52.166.5.224's password:
Last login: Sun May 21 00:12:38 2017 from 141.44.198.92
[majedali@majednode2 ~]$ sudo iptables -I INPUT -p tcp --dport 7180 --syn -j ACCEPT
[sudo] password for majedali:
[majedali@majednode2 ~]$ service iptables save
[majedali@majednode2 ~]$ nmap -sT -O localhost
-bash: nmap: command not found
[majedali@majednode2 ~]$ cloudera-scm-server --help
-bash: cloudera-scm-server: command not found
[majedali@majednode2 ~]$ cd /etc/yum.
yum.conf     yum.repos.d/
[majedali@majednode2 ~]$ cd /etc/yum.repos.d/
[majedali@majednode2 yum.repos.d]$ ls
CentOS-Base.repo       CentOS-Media.repo  cloudera-manager.repo  mysql-community-source.repo
CentOS-Debuginfo.repo  CentOS-Vault.repo  mysql-community.repo   OpenLogic.repo
[majedali@majednode2 yum.repos.d]$ cat cloudera-manager.repo
[cloudera-manager]
# Packages for Cloudera Manager, Version 5, on RedHat or CentOS 6 x86_64
name=Cloudera Manager
baseurl=https://archive.cloudera.com/cm5/redhat/6/x86_64/cm/5.8.3/
gpgkey =https://archive.cloudera.com/cm5/redhat/6/x86_64/cm/RPM-GPG-KEY-cloudera
gpgcheck = 1

[majedali@majednode2 yum.repos.d]$ ifconfig
eth0      Link encap:Ethernet  HWaddr 00:0D:3A:22:BC:52
          inet addr:10.0.1.4  Bcast:10.0.1.255  Mask:255.255.255.0
          inet6 addr: fe80::20d:3aff:fe22:bc52/64 Scope:Link
          UP BROADCAST RUNNING MULTICAST  MTU:1500  Metric:1
          RX packets:3784 errors:0 dropped:0 overruns:0 frame:0
          TX packets:4887 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:1000
          RX bytes:1485437 (1.4 MiB)  TX bytes:1702503 (1.6 MiB)

lo        Link encap:Local Loopback
          inet addr:127.0.0.1  Mask:255.0.0.0
[majedali@majednode2 yum.repos.d]$ cd
[majedali@majednode2 ~]$ exit
logout
There are stopped jobs.
[majedali@majednode2 ~]$ exit
logout
Connection to 52.166.5.224 closed.
[majedali@majednode2 ~]$ sudo passwd root
[sudo] password for majedali:
Changing password for user root.
New password:
Retype new password:
passwd: all authentication tokens updated successfully.
[majedali@majednode2 ~]$ su
Password:
[root@majednode2 majedali]# exit
exit
[majedali@majednode2 ~]$ sudo perl -p -i -e "s/^PasswordAuthentication no/PasswordAuthentication yes/g" /etc/ssh/sshd_config
[sudo] password for majedali:
[majedali@majednode2 ~]$ sudo service sshd restart
Stopping sshd:                                             [  OK  ]
Starting sshd:                                             [  OK  ]
[majedali@majednode2 ~]$ sudo su
[root@majednode2 majedali]# passwd majedali
Changing password for user majedali.
New password:
BAD PASSWORD: it is based on a dictionary word
Retype new password:
passwd: all authentication tokens updated successfully.
[root@majednode2 majedali]# sudo su
[root@majednode2 majedali]# sudo nano /etc/hosts
[root@majednode2 majedali]# sudo nano /etc/hosts
[root@majednode2 majedali]# service nscd status
nscd (pid 1295) is running...
[root@majednode2 majedali]# service ntpd status
ntpd (pid  1373) is running...
[root@majednode2 majedali]# sudo nano /etc/hosts
[root@majednode2 majedali]# ifconfig
eth0      Link encap:Ethernet  HWaddr 00:0D:3A:22:BC:52
          inet addr:10.0.1.4  Bcast:10.0.1.255  Mask:255.255.255.0
          inet6 addr: fe80::20d:3aff:fe22:bc52/64 Scope:Link
          UP BROADCAST RUNNING MULTICAST  MTU:1500  Metric:1
          RX packets:1180750 errors:0 dropped:0 overruns:0 frame:0
          TX packets:49213 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:1000
          RX bytes:1724538299 (1.6 GiB)  TX bytes:9863742 (9.4 MiB)

lo        Link encap:Local Loopback
          inet addr:127.0.0.1  Mask:255.0.0.0
          inet6 addr: ::1/128 Scope:Host
          UP LOOPBACK RUNNING  MTU:16436  Metric:1
          RX packets:151525 errors:0 dropped:0 overruns:0 frame:0
          TX packets:151525 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:0
          RX bytes:158766661 (151.4 MiB)  TX bytes:158766661 (151.4 MiB)

[root@majednode2 majedali]# sudo nano /etc/hosts
[root@majednode2 majedali]# sudo nano /etc/hosts
[root@majednode2 majedali]# hostname -f
majid.westeurope.cloudapp.azure.com
[root@majednode2 majedali]# sudo nano /etc/sysctl.conf
[root@majednode2 majedali]# cat /proc/sys/vm/swappiness
60
[root@majednode2 majedali]# sudo sysctl -w vm.swappiness=1
vm.swappiness = 1
[root@majednode2 majedali]# sudo nano /etc/hosts
[root@majednode2 majedali]# sudo service cloudera-scm-manager stop
cloudera-scm-manager: unrecognized service
[root@majednode2 majedali]# sudo service cloudera-scm-server stop
Stopping cloudera-scm-server:                              [  OK  ]
[root@majednode2 majedali]# sudo service cloudera-scm-agent stop
Stopping cloudera-scm-agent:                               [  OK  ]
[root@majednode2 majedali]# sudo service cloudera-scm-daemons stop
cloudera-scm-daemons: unrecognized service
[root@majednode2 majedali]# sudo yum remove cloudera-*
Loaded plugins: fastestmirror, security
Setting up Remove Process
No Match for argument: cloudera-manager-installer.bin
Loading mirror speeds from cached hostfile
No Match for argument: cloudera-manager.repo
No Packages marked for removal
[root@majednode2 majedali]# sudo yum remove cloudera-scm-server
Loaded plugins: fastestmirror, security
Setting up Remove Process
No Match for argument: cloudera-scm-server
Loading mirror speeds from cached hostfile
No Packages marked for removal
[root@majednode2 majedali]# sudo yum remove cloudera-manager-server
Loaded plugins: fastestmirror, security
Setting up Remove Process
Resolving Dependencies
--> Running transaction check
---> Package cloudera-manager-server.x86_64 0:5.8.3-1.cm583.p0.8.el6 will be erased
--> Processing Dependency: cloudera-manager-server = 5.8.3 for package: cloudera-manager-server-db-2-5.8.3-1.cm583.p0.8.el6.x86_64
--> Running transaction check
---> Package cloudera-manager-server-db-2.x86_64 0:5.8.3-1.cm583.p0.8.el6 will be erased
--> Finished Dependency Resolution

Dependencies Resolved

======================================================================================================================== Package                               Arch            Version                         Repository                  Size
========================================================================================================================Removing:
 cloudera-manager-server               x86_64          5.8.3-1.cm583.p0.8.el6          @cloudera-manager           12 k
Removing for dependencies:
 cloudera-manager-server-db-2          x86_64          5.8.3-1.cm583.p0.8.el6          @cloudera-manager           18 k

Transaction Summary
========================================================================================================================Remove        2 Package(s)

Installed size: 30 k
Is this ok [y/N]: y
Downloading Packages:
Running rpm_check_debug
Running Transaction Test
Transaction Test Succeeded
Running Transaction
  Erasing    : cloudera-manager-server-db-2-5.8.3-1.cm583.p0.8.el6.x86_64                                           1/2
  Erasing    : cloudera-manager-server-5.8.3-1.cm583.p0.8.el6.x86_64                                                2/2
warning: /etc/cloudera-scm-server/db.properties saved as /etc/cloudera-scm-server/db.properties.rpmsave
  Verifying  : cloudera-manager-server-5.8.3-1.cm583.p0.8.el6.x86_64                                                1/2
  Verifying  : cloudera-manager-server-db-2-5.8.3-1.cm583.p0.8.el6.x86_64                                           2/2

Removed:
  cloudera-manager-server.x86_64 0:5.8.3-1.cm583.p0.8.el6

Dependency Removed:
  cloudera-manager-server-db-2.x86_64 0:5.8.3-1.cm583.p0.8.el6

Complete!
[root@majednode2 majedali]# sudo yum remove cloudera-manager-daemons
Loaded plugins: fastestmirror, security
Setting up Remove Process
Resolving Dependencies
--> Running transaction check
---> Package cloudera-manager-daemons.x86_64 0:5.8.3-1.cm583.p0.8.el6 will be erased
--> Processing Dependency: cloudera-manager-daemons = 5.8.3 for package: cloudera-manager-agent-5.8.3-1.cm583.p0.8.el6.x86_64
--> Running transaction check
---> Package cloudera-manager-agent.x86_64 0:5.8.3-1.cm583.p0.8.el6 will be erased
--> Finished Dependency Resolution

Dependencies Resolved

======================================================================================================================== Package                            Arch             Version                          Repository                   Size
========================================================================================================================Removing:
 cloudera-manager-daemons           x86_64           5.8.3-1.cm583.p0.8.el6           @cloudera-manager           678 M
Removing for dependencies:
 cloudera-manager-agent             x86_64           5.8.3-1.cm583.p0.8.el6           @cloudera-manager            69 M

Transaction Summary
========================================================================================================================Remove        2 Package(s)

Installed size: 748 M
Is this ok [y/N]: y
Downloading Packages:
Running rpm_check_debug
Running Transaction Test
Transaction Test Succeeded
Running Transaction
  Erasing    : cloudera-manager-agent-5.8.3-1.cm583.p0.8.el6.x86_64                                                 1/2
warning: /etc/default/cloudera-scm-agent saved as /etc/default/cloudera-scm-agent.rpmsave
warning: /etc/cloudera-scm-agent/config.ini saved as /etc/cloudera-scm-agent/config.ini.rpmsave
  Erasing    : cloudera-manager-daemons-5.8.3-1.cm583.p0.8.el6.x86_64                                               2/2
  Verifying  : cloudera-manager-daemons-5.8.3-1.cm583.p0.8.el6.x86_64                                               1/2
  Verifying  : cloudera-manager-agent-5.8.3-1.cm583.p0.8.el6.x86_64                                                 2/2

Removed:
  cloudera-manager-daemons.x86_64 0:5.8.3-1.cm583.p0.8.el6

Dependency Removed:
  cloudera-manager-agent.x86_64 0:5.8.3-1.cm583.p0.8.el6

Complete!
[root@majednode2 majedali]# sudo yum clear all
Loaded plugins: fastestmirror, security
No such command: clear. Please use /usr/bin/yum --help
[root@majednode2 majedali]# sudo yum install -y oracle-j2sdk1.7
Loaded plugins: fastestmirror, security
Loading mirror speeds from cached hostfile
Setting up Install Process
Package oracle-j2sdk1.7-1.7.0+update67-1.x86_64 already installed and latest version
Nothing to do
[root@majednode2 majedali]# sudo yum install cloudera-manager-daemons cloudera-manager-server
Loaded plugins: fastestmirror, security
Loading mirror speeds from cached hostfile
Setting up Install Process
Resolving Dependencies
--> Running transaction check
---> Package cloudera-manager-daemons.x86_64 0:5.8.3-1.cm583.p0.8.el6 will be installed
---> Package cloudera-manager-server.x86_64 0:5.8.3-1.cm583.p0.8.el6 will be installed
--> Finished Dependency Resolution

Dependencies Resolved

======================================================================================================================== Package                            Arch             Version                           Repository                  Size
========================================================================================================================Installing:
 cloudera-manager-daemons           x86_64           5.8.3-1.cm583.p0.8.el6            cloudera-manager           529 M
 cloudera-manager-server            x86_64           5.8.3-1.cm583.p0.8.el6            cloudera-manager           8.2 k

Transaction Summary
========================================================================================================================Install       2 Package(s)

Total download size: 529 M
Installed size: 678 M
Is this ok [y/N]: y
Downloading Packages:
(1/2): cloudera-manager-daemons-5.8.3-1.cm583.p0.8.el6.x86_64.rpm                                | 529 MB     00:15
(2/2): cloudera-manager-server-5.8.3-1.cm583.p0.8.el6.x86_64.rpm                                 | 8.2 kB     00:00
------------------------------------------------------------------------------------------------------------------------Total                                                                                    35 MB/s | 529 MB     00:15
Running rpm_check_debug
Running Transaction Test
Transaction Test Succeeded
Running Transaction
  Installing : cloudera-manager-daemons-5.8.3-1.cm583.p0.8.el6.x86_64                                               1/2
  Installing : cloudera-manager-server-5.8.3-1.cm583.p0.8.el6.x86_64                                                2/2
  Verifying  : cloudera-manager-server-5.8.3-1.cm583.p0.8.el6.x86_64                                                1/2
  Verifying  : cloudera-manager-daemons-5.8.3-1.cm583.p0.8.el6.x86_64                                               2/2

Installed:
  cloudera-manager-daemons.x86_64 0:5.8.3-1.cm583.p0.8.el6    cloudera-manager-server.x86_64 0:5.8.3-1.cm583.p0.8.el6

Complete!
[root@majednode2 majedali]# sudo /usr/share/cmf/schema/scm_prepare_database.sh mysql scm scm scm_password
JAVA_HOME=/usr/java/jdk1.7.0_67-cloudera
Verifying that we can write to /etc/cloudera-scm-server
Creating SCM configuration file in /etc/cloudera-scm-server
Executing:  /usr/java/jdk1.7.0_67-cloudera/bin/java -cp /usr/share/java/mysql-connector-java.jar:/usr/share/java/oracle-connector-java.jar:/usr/share/cmf/schema/../lib/* com.cloudera.enterprise.dbutil.DbCommandExecutor /etc/cloudera-scm-server/db.properties com.cloudera.cmf.db.
log4j:ERROR Could not find value for key log4j.appender.A
log4j:ERROR Could not instantiate appender named "A".
[2017-05-21 15:04:28,894] INFO     0[main] - com.cloudera.enterprise.dbutil.DbCommandExecutor.parseSqlState(DbCommandExecutor.java) - Unable to login using supplied username/password.
[2017-05-21 15:04:28,910]ERROR    16[main] - com.cloudera.enterprise.dbutil.DbCommandExecutor$DbConnectionTestException.logError(DbCommandExecutor.java) - Error when connecting to database.
[majedali@majednode2 ~]$ sudo /usr/share/cmf/schema/scm_prepare_database.sh mysql scm scm scm_password
[sudo] password for majedali:
[majedali@majednode2 ~]$ sudo /usr/share/cmf/schema/scm_prepare_database.sh mysql scm scm scm_password
[sudo] password for majedali:
JAVA_HOME=/usr/java/jdk1.7.0_67-cloudera
Verifying that we can write to /etc/cloudera-scm-server
Creating SCM configuration file in /etc/cloudera-scm-server
[majedali@majednode2 ~]$ clear
[majedali@majednode2 ~]$ ls
cloudera-manager-installer.bin  log4j.log                                 mysql-connector-java-5.1.42.tar.gz
cloudera-manager.repo           mysql-community-release-el6-7.noarch.rpm
jdk-8u102-linux-x64.rpm         mysql-connector-java-5.1.42
[majedali@majednode2 ~]$ chmod u+x cloudera-manager-installer.bin
[majedali@majednode2 ~]$ sudo ./cloudera-manager-installer.bin
[majedali@majednode2 ~]$ sudo ./cloudera-manager-installer.bin
[majedali@majednode2 ~]$ sudo /usr/share/cmf/cloudera
cloudera/                        cloudera-navigator-audit-server/ cloudera-navigator-server/
[majedali@majednode2 ~]$ sudo /usr/share/cmf/uninstall-cloudera-manager.sh
[majedali@majednode2 ~]$ sudo yum install cloudera-manager-daemons cloudera-manager-server
Loaded plugins: fastestmirror, security
Loading mirror speeds from cached hostfile
Setting up Install Process
Resolving Dependencies
--> Running transaction check
---> Package cloudera-manager-daemons.x86_64 0:5.8.3-1.cm583.p0.8.el6 will be installed
---> Package cloudera-manager-server.x86_64 0:5.8.3-1.cm583.p0.8.el6 will be installed
--> Finished Dependency Resolution

Dependencies Resolved

======================================================================================================================== Package                            Arch             Version                           Repository                  Size
========================================================================================================================Installing:
 cloudera-manager-daemons           x86_64           5.8.3-1.cm583.p0.8.el6            cloudera-manager           529 M
 cloudera-manager-server            x86_64           5.8.3-1.cm583.p0.8.el6            cloudera-manager           8.2 k

Transaction Summary
========================================================================================================================Install       2 Package(s)

Total download size: 529 M
Installed size: 678 M
Is this ok [y/N]: y
Downloading Packages:
(1/2): cloudera-manager-daemons-5.8.3-1.cm583.p0.8.el6.x86_64.rpm                                | 529 MB     00:15
(2/2): cloudera-manager-server-5.8.3-1.cm583.p0.8.el6.x86_64.rpm                                 | 8.2 kB     00:00
------------------------------------------------------------------------------------------------------------------------Total                                                                                    34 MB/s | 529 MB     00:15
majedalibash@WINDOWS-BSP279E:/mnt/c/Windows/System32$ ssh majedali@52.233.140.151
The authenticity of host '52.233.140.151 (52.233.140.151)' can't be established.
RSA key fingerprint is f8:03:10:1f:15:4e:9c:79:68:58:90:dd:c0:8b:a3:d5.
Are you sure you want to continue connecting (yes/no)? yes
[majedali@majednode1 ~]$ sudo nano /etc/hosts
[majedali@majednode1 ~]$ hostname
majednode1
[majedali@majednode1 ~]$ sudo nano /etc/hosts
[majedali@majednode1 ~]$ getent majednode1
Unknown database: majednode1
Try `getent --help' or `getent --usage' for more information.
[majedali@majednode1 ~]$ getent hosts majednode1
10.0.1.5        majednode1
[majedali@majednode1 ~]$ sudo yum install nscd
Loaded plugins: fastestmirror, security
Setting up Install Process
Determining fastest mirrors
base                                                        | 3.7 kB     00:00
base/primary_db                                             | 4.7 MB     00:00

extras                                                      | 3.4 kB     00:00
extras/primary_db                                           |  29 kB     00:00
openlogic                                                   | 2.9 kB     00:00
openlogic/primary_db                                        | 551 kB     00:00
updates                                                     | 3.4 kB     00:00
updates/primary_db                                          | 828 kB     00:00
Resolving Dependencies
--> Running transaction check
---> Package nscd.x86_64 0:2.12-1.209.el6_9.1 will be installed
--> Finished Dependency Resolution

Dependencies Resolved

===================================================================================
 Package       Arch            Version                      Repository        Size
===================================================================================
Installing:
 nscd          x86_64          2.12-1.209.el6_9.1           updates          232 k

Transaction Summary
===================================================================================
Install       1 Package(s)

Total download size: 232 k
Installed size: 185 k
Is this ok [y/N]: Exiting on user Command
Your transaction was saved, rerun it with:
 yum load-transaction /tmp/yum_save_tx-2017-05-21-16-08NHluZf.yumtx
[majedali@majednode1 ~]$ service nscd start
nscd: unrecognized service
[majedali@majednode1 ~]$ sudo service nscd start
nscd: unrecognized service
[majedali@majednode1 ~]$ sudo yum install nscd
Loaded plugins: fastestmirror, security
Setting up Install Process
Loading mirror speeds from cached hostfile
Resolving Dependencies
--> Running transaction check
---> Package nscd.x86_64 0:2.12-1.209.el6_9.1 will be installed
--> Finished Dependency Resolution

Dependencies Resolved

===================================================================================
 Package       Arch            Version                      Repository        Size
===================================================================================
Installing:
 nscd          x86_64          2.12-1.209.el6_9.1           updates          232 k

Transaction Summary
===================================================================================
Install       1 Package(s)

Total download size: 232 k
Installed size: 185 k
Is this ok [y/N]: y
Downloading Packages:
nscd-2.12-1.209.el6_9.1.x86_64.rpm                          | 232 kB     00:00
Running rpm_check_debug
Running Transaction Test
Transaction Test Succeeded
Running Transaction
  Installing : nscd-2.12-1.209.el6_9.1.x86_64                                  1/1
  Verifying  : nscd-2.12-1.209.el6_9.1.x86_64                                  1/1

Installed:
  nscd.x86_64 0:2.12-1.209.el6_9.1

Complete!
[majedali@majednode1 ~]$ sudo service nscd start
Starting nscd:                                             [  OK  ]
[majedali@majednode1 ~]$ service nscd status
nscd (pid 24698) is running...
[majedali@majednode1 ~]$ service ntpd start
[majedali@majednode1 ~]$ chkconfig ntpd on
You do not have enough privileges to perform this operation.
[majedali@majednode1 ~]$ sudo chkconfig ntpd on
[majedali@majednode1 ~]$ service ntpd status
ntpd (pid  1635) is running...
[majedali@majednode1 ~]$ sudo reboot
