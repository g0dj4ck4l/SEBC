**Write curl statements that stop, start, and check the current state of your Hive service.**
```
[root@aedg1-cdh58 centos]# curl -u 'g0dj4ck4l:cloudera' 'http://aedg1-cdh58:7180/api/v2/clusters/g0dj4ck4l/services/hive'
{
  "name" : "hive",
  "type" : "HIVE",
  "clusterRef" : {
    "clusterName" : "cluster"
  },
  "serviceUrl" : "http://aedg1-cdh58.hadoop:7180/cmf/serviceRedirect/hive",
  "serviceState" : "STARTED",
  "healthSummary" : "GOOD",
  "healthChecks" : [ {
    "name" : "HIVE_HIVEMETASTORES_HEALTHY",
    "summary" : "GOOD"
  }, {
    "name" : "HIVE_HIVESERVER2S_HEALTHY",
    "summary" : "GOOD"
  } ],
  "configStale" : false,
  "maintenanceMode" : false,
  "maintenanceOwners" : [ ],
  "displayName" : "Hive"
}


[root@aedg1-cdh58 centos]# curl -X POST -u 'g0dj4ck4l:cloudera' 'http://aedg1-cdh58:7180/api/v2/clusters/g0dj4ck4l/services/hive/commands/stop'
{
  "id" : 873,
  "name" : "Stop",
  "startTime" : "2017-10-18T13:50:00.994Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }
}

[root@aedg1-cdh58 centos]# curl -X POST -u 'g0dj4ck4l:cloudera' 'http://aedg1-cdh58:7180/api/v2/clusters/g0dj4ck4l/services/hive/commands/start'
{
  "id" : 877,
  "name" : "Start",
  "startTime" : "2017-10-18T13:52:06.684Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }
}
```
