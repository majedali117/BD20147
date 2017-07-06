### full teragen command and job output
```
[neymar@ip-172-31-14-244 ec2-user]$ time hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar teragen -Ddfs.blocksize=16M -Dmapred.map.tasks=8 655360 /user/neymar/tgen640
17/07/06 12:21:16 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-14-244/172.31.14.244:8032
17/07/06 12:21:17 INFO terasort.TeraGen: Generating 655360 using 8
17/07/06 12:21:17 INFO mapreduce.JobSubmitter: number of splits:8
17/07/06 12:21:17 INFO Configuration.deprecation: mapred.map.tasks is deprecated. Instead, use mapreduce.job.maps
17/07/06 12:21:17 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1499356670440_0001
17/07/06 12:21:17 INFO impl.YarnClientImpl: Submitted application application_1499356670440_0001
17/07/06 12:21:17 INFO mapreduce.Job: The url to track the job: http://ip-172-31-14-244:8088/proxy/application_1499356670440_0001/
17/07/06 12:21:17 INFO mapreduce.Job: Running job: job_1499356670440_0001
17/07/06 12:21:26 INFO mapreduce.Job: Job job_1499356670440_0001 running in uber mode : false
17/07/06 12:21:26 INFO mapreduce.Job:  map 0% reduce 0%
17/07/06 12:21:35 INFO mapreduce.Job:  map 25% reduce 0%
17/07/06 12:21:36 INFO mapreduce.Job:  map 38% reduce 0%
17/07/06 12:21:37 INFO mapreduce.Job:  map 88% reduce 0%
17/07/06 12:21:38 INFO mapreduce.Job:  map 100% reduce 0%
17/07/06 12:21:38 INFO mapreduce.Job: Job job_1499356670440_0001 completed successfully
17/07/06 12:21:38 INFO mapreduce.Job: Counters: 33
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=1017640
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=677
                HDFS: Number of bytes written=65536000
                HDFS: Number of read operations=32
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=16
        Job Counters
                Launched map tasks=8
                Other local map tasks=8
                Total time spent by all maps in occupied slots (ms)=67327
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=67327
                Total vcore-milliseconds taken by all map tasks=67327
                Total megabyte-milliseconds taken by all map tasks=68942848
        Map-Reduce Framework
                Map input records=655360
                Map output records=655360
                Input split bytes=677
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=673
                CPU time spent (ms)=19970
                Physical memory (bytes) snapshot=1613398016
                Virtual memory (bytes) snapshot=12507418624
                Total committed heap usage (bytes)=2373976064
                Peak Map Physical memory (bytes)=245555200
                Peak Map Virtual memory (bytes)=1574899712
        org.apache.hadoop.examples.terasort.TeraGen$Counters
                CHECKSUM=1408100361519672
        File Input Format Counters
                Bytes Read=0
        File Output Format Counters
                Bytes Written=65536000

real    0m24.914s
user    0m6.105s
sys     0m0.315s
[neymar@ip-172-31-14-244 ec2-user]$
```
### result of the time command
```
17/07/06 12:21:16 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-14-244/172.31.14.244:8032
17/07/06 12:21:17 INFO terasort.TeraGen: Generating 655360 using 8
17/07/06 12:21:17 INFO mapreduce.JobSubmitter: number of splits:8
17/07/06 12:21:17 INFO Configuration.deprecation: mapred.map.tasks is deprecated. Instead, use mapreduce.job.maps
17/07/06 12:21:17 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1499356670440_0001
17/07/06 12:21:17 INFO impl.YarnClientImpl: Submitted application application_1499356670440_0001
17/07/06 12:21:17 INFO mapreduce.Job: The url to track the job: http://ip-172-31-14-244:8088/proxy/application_1499356670440_0001/
17/07/06 12:21:17 INFO mapreduce.Job: Running job: job_1499356670440_0001
17/07/06 12:21:26 INFO mapreduce.Job: Job job_1499356670440_0001 running in uber mode : false
17/07/06 12:21:26 INFO mapreduce.Job:  map 0% reduce 0%
17/07/06 12:21:35 INFO mapreduce.Job:  map 25% reduce 0%
17/07/06 12:21:36 INFO mapreduce.Job:  map 38% reduce 0%
17/07/06 12:21:37 INFO mapreduce.Job:  map 88% reduce 0%
17/07/06 12:21:38 INFO mapreduce.Job:  map 100% reduce 0%
17/07/06 12:21:38 INFO mapreduce.Job: Job job_1499356670440_0001 completed successfully
17/07/06 12:21:38 INFO mapreduce.Job: Counters: 33
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=1017640
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=677
                HDFS: Number of bytes written=65536000
                HDFS: Number of read operations=32
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=16
        Job Counters
                Launched map tasks=8
                Other local map tasks=8
                Total time spent by all maps in occupied slots (ms)=67327
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=67327
                Total vcore-milliseconds taken by all map tasks=67327
                Total megabyte-milliseconds taken by all map tasks=68942848
        Map-Reduce Framework
                Map input records=655360
                Map output records=655360
                Input split bytes=677
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=673
                CPU time spent (ms)=19970
                Physical memory (bytes) snapshot=1613398016
                Virtual memory (bytes) snapshot=12507418624
                Total committed heap usage (bytes)=2373976064
                Peak Map Physical memory (bytes)=245555200
                Peak Map Virtual memory (bytes)=1574899712
        org.apache.hadoop.examples.terasort.TeraGen$Counters
                CHECKSUM=1408100361519672
        File Input Format Counters
                Bytes Read=0
        File Output Format Counters
                Bytes Written=65536000

real    0m24.914s
user    0m6.105s
sys     0m0.315s
[neymar@ip-172-31-14-244 ec2-user]$

```
### The command and output of hdfs dfs -ls /user/neymar/tgen640
```
[neymar@ip-172-31-14-244 ec2-user]$ hdfs dfs -ls /user/neymar/tgen640
Found 9 items
-rw-r--r--   3 neymar supergroup          0 2017-07-06 12:21 /user/neymar/tgen640/_SUCCESS
-rw-r--r--   3 neymar supergroup    8192000 2017-07-06 12:21 /user/neymar/tgen640/part-m-00000
-rw-r--r--   3 neymar supergroup    8192000 2017-07-06 12:21 /user/neymar/tgen640/part-m-00001
-rw-r--r--   3 neymar supergroup    8192000 2017-07-06 12:21 /user/neymar/tgen640/part-m-00002
-rw-r--r--   3 neymar supergroup    8192000 2017-07-06 12:21 /user/neymar/tgen640/part-m-00003
-rw-r--r--   3 neymar supergroup    8192000 2017-07-06 12:21 /user/neymar/tgen640/part-m-00004
-rw-r--r--   3 neymar supergroup    8192000 2017-07-06 12:21 /user/neymar/tgen640/part-m-00005
-rw-r--r--   3 neymar supergroup    8192000 2017-07-06 12:21 /user/neymar/tgen640/part-m-00006
-rw-r--r--   3 neymar supergroup    8192000 2017-07-06 12:21 /user/neymar/tgen640/part-m-00007
[neymar@ip-172-31-14-244 ec2-user]$

```
### show how many blocks are stored

```
[neymar@ip-172-31-14-244 ec2-user]$ hadoop fsck /user/neymar
DEPRECATED: Use of this script to execute hdfs command is deprecated.
Instead use the hdfs command for it.

Connecting to namenode via http://ip-172-31-14-244:50070
FSCK started by neymar (auth:SIMPLE) from /172.31.14.244 for path /user/neymar at Thu Jul 06 12:24:44 EDT 2017
.........Status: HEALTHY
 Total size:    65536000 B
 Total dirs:    3
 Total files:   9
 Total symlinks:                0
 Total blocks (validated):      8 (avg. block size 8192000 B)
 Minimally replicated blocks:   8 (100.0 %)
 Over-replicated blocks:        0 (0.0 %)
 Under-replicated blocks:       0 (0.0 %)
 Mis-replicated blocks:         0 (0.0 %)
 Default replication factor:    3
 Average block replication:     3.0
 Corrupt blocks:                0
 Missing replicas:              0 (0.0 %)
 Number of data-nodes:          5
 Number of racks:               1
FSCK ended at Thu Jul 06 12:24:44 EDT 2017 in 5 milliseconds


The filesystem under path '/user/neymar' is HEALTHY
[neymar@ip-172-31-14-244 ec2-user]$

```
