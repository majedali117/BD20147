### Run terasort test
```
time hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar teragen
-Ddfs.blocksize=16M -Dmapred.map.tasks=6 50000000 /user/raffles/terasort/terasort-input
```
