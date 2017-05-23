<b>System Configuration Checks</b></br>
[root@majednode2 majedali]# cat /proc/sys/vm/swappiness</br>
60</br>
[root@majednode2 majedali]# sudo sysctl -w vm.swappiness=1</br>
vm.swappiness = 1</br>
