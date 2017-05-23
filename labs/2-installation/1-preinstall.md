<b>System Configuration Checks</b></br>
[root@majednode2 majedali]# cat /proc/sys/vm/swappiness</br>
60</br>
[root@majednode2 majedali]# sudo sysctl -w vm.swappiness=1</br>
vm.swappiness = 1</br>
<b>Show the mount attributes of all volumes</b></br>
[majedali@majednode1 ~]$ df -h</br>
Filesystem      Size  Used Avail Use% Mounted on</br>
/dev/sda1        30G   11G   18G  37% /</br>
tmpfs           6.9G     0  6.9G   0% /dev/shm</br>
/dev/sdb1        28G  308M   26G   2% /mnt/resource</br>
cm_processes    6.9G   14M  6.9G   1% /var/run/cloudera-scm-agent/process</br>

#!/bin/sh</br>
echo never > /sys/kernel/mm/transparent_hugepage/defrag</br>
echo never > /sys/kernel/mm/transparent_hugepage/enabled</br>
touch /var/lock/subsys/local</br>
<b>Show the mount attributes of all volumes</b>
</br>
<b>List your network interface configuration</b></br>
[root@majednode2 majedali]# ifconfig</br>
eth0      Link encap:Ethernet  HWaddr 00:0D:3A:22:BC:52</br>
          inet addr:10.0.1.4  Bcast:10.0.1.255  Mask:255.255.255.0</br>
          inet6 addr: fe80::20d:3aff:fe22:bc52/64 Scope:Link</br>
          UP BROADCAST RUNNING MULTICAST  MTU:1500  Metric:1</br>
          RX packets:1180750 errors:0 dropped:0 overruns:0 frame:0</br>
          TX packets:49213 errors:0 dropped:0 overruns:0 carrier:0</br>
          collisions:0 txqueuelen:1000</br>
          RX bytes:1724538299 (1.6 GiB)  TX bytes:9863742 (9.4 MiB)</br>
</br>
lo        Link encap:Local Loopback</br>
          inet addr:127.0.0.1  Mask:255.0.0.0</br>
          inet6 addr: ::1/128 Scope:Host</br>
          UP LOOPBACK RUNNING  MTU:16436  Metric:1</br>
          RX packets:151525 errors:0 dropped:0 overruns:0 frame:0</br>
          TX packets:151525 errors:0 dropped:0 overruns:0 carrier:0</br>
          collisions:0 txqueuelen:0</br>
          RX bytes:158766661 (151.4 MiB)  TX bytes:158766661 (151.4 MiB)</br>
          
<b>List your network interface configuration</b></br>
 127.0.0.1   localhost localhost.localdomain localhost4 localhost4.localdomain4</br>
::1         localhost localhost.localdomain localhost6 localhost6.localdomain6</br>
10.0.1.5    majednode1         </br>
<b>orward and reverse host lookups</b></br>
[majedali@majednode1 ~]$ sudo nano /etc/hosts </br>
[majedali@majednode1 ~]$ getent majednode1 </br>
Unknown database: majednode1 </br>
Try `getent --help' or `getent --usage' for more information. </br>
[majedali@majednode1 ~]$ getent hosts majednode1 </br>
10.0.1.5        majednode1 </br>
<b> Nscd and Ntdp service </b>
[majedali@majednode1 ~]$ sudo service nscd start</br>
Starting nscd:                                             [  OK  ]</br>
[majedali@majednode1 ~]$ service nscd status</br>
nscd (pid 24698) is running...</br>
[majedali@majednode1 ~]$ service ntpd start</br>
[majedali@majednode1 ~]$ chkconfig ntpd on</br>
You do not have enough privileges to perform this operation.</br>
[majedali@majednode1 ~]$ sudo chkconfig ntpd on</br>
[majedali@majednode1 ~]$ service ntpd status</br>
ntpd (pid  1635) is running...</br>
[majedali@majednode1 ~]$ sudo reboot</br>
