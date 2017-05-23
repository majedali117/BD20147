System Configuration Checks
[root@majednode2 majedali]# cat /proc/sys/vm/swappiness
60
[root@majednode2 majedali]# sudo sysctl -w vm.swappiness=1
vm.swappiness = 1
