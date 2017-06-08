### Cluster Name
```
[majedali@majednode1 ~]$ curl -u admin:admin'http://localhost:7180/api/v13/clusters'
{
  "items" : [ {
    "name" : "cluster",
    "displayName" : "Cluster 1",
    "version" : "CDH5",
    "fullVersion" : "5.11.0",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "clusterUrl" : "http://majednode1:7180/cmf/clusterRedirect/cluster",
    "hostsUrl" : "http://majednode1:7180/cmf/clusterRedirect/cluster/hosts",
    "entityStatus" : "BAD_HEALTH"
  } ]
}
```

### All Hive services
```
[majedali@majednode1 ~]$ curl -u admin:admin http://localhost:7180/api/v13/clusters/cluster/services/hive
{
  "name" : "hive",
  "type" : "HIVE",
  "clusterRef" : {
    "clusterName" : "cluster"
  },
  "serviceUrl" : "http://majednode1:7180/cmf/serviceRedirect/hive",
  "roleInstancesUrl" : "http://majednode1:7180/cmf/serviceRedirect/hive/instances",
  "serviceState" : "STARTED",
  "healthSummary" : "BAD",
  "healthChecks" : [ {
    "name" : "HIVE_HIVEMETASTORES_HEALTHY",
    "summary" : "BAD",
    "suppressed" : false
  }, {
    "name" : "HIVE_HIVESERVER2S_HEALTHY",
    "summary" : "GOOD",
    "suppressed" : false
  } ],
  "configStalenessStatus" : "FRESH",
  "clientConfigStalenessStatus" : "FRESH",
  "maintenanceMode" : false,
  "maintenanceOwners" : [ ],
  "displayName" : "Hive",
  "entityStatus" : "BAD_HEALTH"
}
```
### Stop Hive service
```
[majedali@majednode1 ~]$ curl -X POST -u admin:admin 'http://localhost:7180/api/v13/clusters/cluster/services/hive/comma
nds/stop'
{
  "id" : 91,
  "name" : "Stop",
  "startTime" : "2017-05-25T15:57:35.293Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }
}
```
### Hive service start
```
[majedali@majednode1 ~]$ curl -X POST -u admin:admin 'http://localhost:7180/api/v13/clusters/cluster/services/hive/comma
nds/start'
{
  "id" : 95,
  "name" : "Start",
  "startTime" : "2017-05-25T16:03:23.380Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }
}
```
