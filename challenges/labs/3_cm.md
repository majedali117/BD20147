###command and output for hdfs dfs -ls /user
```
[ec2-user@ip-172-31-14-244 ~]$ sudo -u hdfs hadoop fs -mkdir /user/ronaldo
[ec2-user@ip-172-31-14-244 ~]$ sudo -u hdfs hadoop fs -mkdir /user/neymar
[ec2-user@ip-172-31-14-244 ~]$ sudo -u hdfs hadoop fs -ls /user/
Found 6 items
drwxrwxrwx   - mapred hadoop              0 2017-07-06 11:38 /user/history
drwxrwxr-t   - hive   hive                0 2017-07-06 11:38 /user/hive
drwxrwxr-x   - hue    hue                 0 2017-07-06 11:39 /user/hue
drwxr-xr-x   - hdfs   supergroup          0 2017-07-06 11:45 /user/neymar
drwxrwxr-x   - oozie  oozie               0 2017-07-06 11:39 /user/oozie
drwxr-xr-x   - hdfs   supergroup          0 2017-07-06 11:45 /user/ronaldo
```
###output from the CM API call ../api/v14/hosts
```
{
  "items" : [ {
    "hostId" : "80e92cb0-4a63-4a01-a25b-68c60c60c805",
    "ipAddress" : "172.31.14.244",
    "hostname" : "ip-172-31-14-244",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-14-244:7180/cmf/hostRedirect/80e92cb0-4a63-4a01-a25b-68c60c60c805",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 15664758784
  }, {
    "hostId" : "48e0eb8d-2f43-4a62-97f1-59ce5079f6b5",
    "ipAddress" : "172.31.15.144",
    "hostname" : "ip-172-31-15-144",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-14-244:7180/cmf/hostRedirect/48e0eb8d-2f43-4a62-97f1-59ce5079f6b5",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 15664758784
  }, {
    "hostId" : "7ce47245-81b2-4ac0-95cc-5a12f3d5500a",
    "ipAddress" : "172.31.2.233",
    "hostname" : "ip-172-31-2-233",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-14-244:7180/cmf/hostRedirect/7ce47245-81b2-4ac0-95cc-5a12f3d5500a",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 15664758784
  }, {
    "hostId" : "db19f107-4c38-4eee-8a20-bd71e6b901af",
    "ipAddress" : "172.31.8.65",
    "hostname" : "ip-172-31-8-65",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-14-244:7180/cmf/hostRedirect/db19f107-4c38-4eee-8a20-bd71e6b901af",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 15664758784
  }, {
    "hostId" : "30190bf9-5935-4578-a456-799225fef161",
    "ipAddress" : "172.31.9.15",
    "hostname" : "ip-172-31-9-15",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-14-244:7180/cmf/hostRedirect/30190bf9-5935-4578-a456-799225fef161",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 15664758784
  } ]
}

```
