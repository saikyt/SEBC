# Check status
```
[root@master ec2-user]# curl -u saikyt:cloudera 'http://localhost:7180/api/v1/clusters/saikyt/services/hive'
{
  "name" : "hive",
  "type" : "HIVE",
  "clusterRef" : {
    "clusterName" : "cluster"
  },
  "serviceUrl" : "http://master:7180/cmf/serviceRedirect/hive",
  "serviceState" : "STARTED",
  "healthSummary" : "GOOD",
  "healthChecks" : [ {
    "name" : "HIVE_HIVEMETASTORES_HEALTHY",
    "summary" : "GOOD"
  }, {
    "name" : "HIVE_HIVESERVER2S_HEALTHY",
    "summary" : "GOOD"
  }, {
    "name" : "HIVE_WEBHCATS_HEALTHY",
    "summary" : "GOOD"
  } ],
  "configStale" : false
}[root@master ec2-user]#

```

# Stop hive
```
[root@master ec2-user]# curl -X POST -u saikyt:cloudera 'http://localhost:7180/api/v1/clusters/saikyt/services/hive/commands/stop'
{
  "id" : 692,
  "name" : "Stop",
  "startTime" : "2017-06-23T00:23:42.514Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }
  
}
```
# Start hive
[root@master ec2-user]# curl -X POST -u saikyt:cloudera 'http://localhost:7180/api/v1/clusters/saikyt/services/hive/commands/start'
{
  "id" : 699,
  "name" : "Start",
  "startTime" : "2017-06-23T00:23:59.751Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }
}


