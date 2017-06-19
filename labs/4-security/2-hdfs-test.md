### Add Principle raffles 
```
kadmin.local:  addprinc -pw cloudera raffles@MAJEDALI
WARNING: no policy specified for raffles@MAJEDALI; defaulting to no policy
Principal "raffles@MAJEDALI" created.
kadmin.local:  exit
[root@majedvm1 majed]# adduser raffles
[root@majedvm1 majed]# exit
```
### Run teragen test
```
time hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar teragen -Ddfs.blocksize=16M -Dmapred.map.tasks=6 50000000 /user/raffles/terasort/terasort-input
```
### Results of teragen test
```
[majed@majedvm1 ~]$  time hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar teragen -Ddfs.blocksize=16M -Dmapred.map.tasks=6 50000000 /user/raffles/terasort/terasort-input
17/06/19 21:56:12 INFO client.RMProxy: Connecting to ResourceManager at majedvm1/10.0.0.4:8032
17/06/19 21:56:12 INFO hdfs.DFSClient: Created token for raffles: HDFS_DELEGATION_TOKEN owner=raffles@MAJEDALI, renewer=yarn, realUser=, issueDate=1497909372809, maxDate=1498514172809, sequenceNumber=24, masterKeyId=4 on 10.0.0.4:8020
17/06/19 21:56:12 INFO security.TokenCache: Got dt for hdfs://majedvm1:8020; Kind: HDFS_DELEGATION_TOKEN, Service: 10.0.0.4:8020, Ident: (token for raffles: HDFS_DELEGATION_TOKEN owner=raffles@MAJEDALI, renewer=yarn, realUser=, issueDate=1497909372809, maxDate=1498514172809, sequenceNumber=24, masterKeyId=4)
17/06/19 21:56:13 INFO terasort.TeraSort: Generating 50000000 using 6
17/06/19 21:56:13 INFO mapreduce.JobSubmitter: number of splits:6
17/06/19 21:56:13 INFO Configuration.deprecation: mapred.map.tasks is deprecated. Instead, use mapreduce.job.maps
17/06/19 21:56:13 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1497908890538_0001
17/06/19 21:56:13 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: 10.0.0.4:8020, Ident: (token for raffles: HDFS_DELEGATION_TOKEN owner=raffles@MAJEDALI, renewer=yarn, realUser=, issueDate=1497909372809, maxDate=1498514172809, sequenceNumber=24, masterKeyId=4)
17/06/19 21:56:14 INFO impl.YarnClientImpl: Submitted application application_1497908890538_0001
17/06/19 21:56:14 INFO mapreduce.Job: The url to track the job: http://majedvm1:8088/proxy/application_1497908890538_0001/
17/06/19 21:56:14 INFO mapreduce.Job: Running job: job_1497908890538_0001
17/06/19 21:56:23 INFO mapreduce.Job: Job job_1497908890538_0001 running in uber mode : false
17/06/19 21:56:23 INFO mapreduce.Job:  map 0% reduce 0%
17/06/19 21:56:35 INFO mapreduce.Job:  map 8% reduce 0%
...
17/06/19 21:59:02 INFO mapreduce.Job:  map 100% reduce 0%
17/06/19 21:59:02 INFO mapreduce.Job: Job job_1497908890538_0001 completed successfully
17/06/19 21:59:02 INFO mapreduce.Job: Counters: 31
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=739260
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=510
                HDFS: Number of bytes written=5000000000
                HDFS: Number of read operations=24
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=12
        Job Counters
                Launched map tasks=6
                Other local map tasks=6
                Total time spent by all maps in occupied slots (ms)=145444
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=145444
                Total vcore-seconds taken by all map tasks=145444
                Total megabyte-seconds taken by all map tasks=148934656
        Map-Reduce Framework
                Map input records=50000000
                Map output records=50000000
                Input split bytes=510
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=622
                CPU time spent (ms)=75410
                Physical memory (bytes) snapshot=1961967616
                Virtual memory (bytes) snapshot=9341112320
                Total committed heap usage (bytes)=1979711488
        org.apache.hadoop.examples.terasort.TeraGen$Counters
                CHECKSUM=107387891658806101
        File Input Format Counters
                Bytes Read=0
        File Output Format Counters
                Bytes Written=5000000000

real    2m52.208s
user    0m4.729s
sys     0m0.253s
```
### Run terasort test
```
 time hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar terasort /user/raffles/terasort/terasort-input /user/raffles/terasort/terasort-output
```

### results of terasort test
```
[majed@majedvm1 ~]$  time hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar terasort /user/raffles/terasort/terasort-input /user/raffles/terasort/terasort-output
17/06/19 21:59:59 INFO terasort.TeraSort: starting
17/06/19 22:00:00 INFO hdfs.DFSClient: Created token for raffles: HDFS_DELEGATION_TOKEN owner=raffles@MAJEDALI, renewer=yarn, realUser=, issueDate=1497909600883, maxDate=1498514400883, sequenceNumber=25, masterKeyId=4 on 10.0.0.4:8020
17/06/19 22:00:00 INFO security.TokenCache: Got dt for hdfs://majedvm1:8020; Kind: HDFS_DELEGATION_TOKEN, Service: 10.0.0.4:8020, Ident: (token for raffles: HDFS_DELEGATION_TOKEN owner=raffles@MAJEDALI, renewer=yarn, realUser=, issueDate=1497909600883, maxDate=1498514400883, sequenceNumber=25, masterKeyId=4)
17/06/19 22:00:01 INFO input.FileInputFormat: Total input paths to process : 6
Spent 337ms computing base-splits.
Spent 4ms computing TeraScheduler splits.
Computing input splits took 342ms
Sampling 10 splits of 300
Making 1 from 100000 sampled records
Computing parititions took 690ms
Spent 1034ms computing partitions.
17/06/19 22:00:01 INFO client.RMProxy: Connecting to ResourceManager at majedvm1/10.0.0.4:8032
17/06/19 22:00:02 INFO mapreduce.JobSubmitter: number of splits:300
17/06/19 22:00:02 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1497908890538_0002
17/06/19 22:00:02 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: 10.0.0.4:8020, Ident: (token for raffles: HDFS_DELEGATION_TOKEN owner=raffles@MAJEDALI, renewer=yarn, realUser=, issueDate=1497909600883, maxDate=1498514400883, sequenceNumber=25, masterKeyId=4)
17/06/19 22:00:02 INFO impl.YarnClientImpl: Submitted application application_1497908890538_0002
17/06/19 22:00:02 INFO mapreduce.Job: The url to track the job: http://majedvm1:8088/proxy/application_1497908890538_0002/
17/06/19 22:00:02 INFO mapreduce.Job: Running job: job_1497908890538_0002
17/06/19 22:00:20 INFO mapreduce.Job: Job job_1497908890538_0002 running in uber mode : false
17/06/19 22:00:20 INFO mapreduce.Job:  map 0% reduce 0%
17/06/19 22:00:33 INFO mapreduce.Job:  map 1% reduce 0%
...
17/06/19 22:27:12 INFO mapreduce.Job:  map 99% reduce 0%
17/06/19 22:27:27 INFO mapreduce.Job:  map 100% reduce 0%
17/06/19 22:27:42 INFO mapreduce.Job:  map 100% reduce 6%
...
17/06/19 22:31:41 INFO mapreduce.Job:  map 100% reduce 99%
17/06/19 22:31:47 INFO mapreduce.Job:  map 100% reduce 100%
17/06/19 22:32:00 INFO mapreduce.Job: Job job_1497908890538_0002 completed successfully
17/06/19 22:32:00 INFO mapreduce.Job: Counters: 49
        File System Counters
                FILE: Number of bytes read=2241053714
                FILE: Number of bytes written=4463850061
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=5000040500
                HDFS: Number of bytes written=5000000000
                HDFS: Number of read operations=903
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=2
        Job Counters
                Launched map tasks=300
                Launched reduce tasks=1
                Data-local map tasks=300
                Total time spent by all maps in occupied slots (ms)=1359123
                Total time spent by all reduces in occupied slots (ms)=255099
                Total time spent by all map tasks (ms)=1359123
                Total time spent by all reduce tasks (ms)=255099
                Total vcore-seconds taken by all map tasks=1359123
                Total vcore-seconds taken by all reduce tasks=255099
                Total megabyte-seconds taken by all map tasks=1391741952
                Total megabyte-seconds taken by all reduce tasks=261221376
        Map-Reduce Framework
                Map input records=50000000
                Map output records=50000000
                Map output bytes=5100000000
                Map output materialized bytes=2185277767
                Input split bytes=40500
                Combine input records=0
                Combine output records=0
                Reduce input groups=50000000
                Reduce shuffle bytes=2185277767
                Reduce input records=50000000
                Reduce output records=50000000
                Spilled Records=100000000
                Shuffled Maps =300
                Failed Shuffles=0
                Merged Map outputs=300
                GC time elapsed (ms)=13255
                CPU time spent (ms)=722970
                Physical memory (bytes) snapshot=145708281856
                Virtual memory (bytes) snapshot=470213496832
                Total committed heap usage (bytes)=165150720000
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters
                Bytes Read=5000000000
        File Output Format Counters
                Bytes Written=5000000000
17/06/19 22:32:00 INFO terasort.TeraSort: done

real    32m1.855s
user    0m11.225s
sys     0m0.776s
```
