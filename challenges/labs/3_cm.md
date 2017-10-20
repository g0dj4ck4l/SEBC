```
[hdfs@bmst1-cdh ~]$ hdfs dfs -ls /user
Found 6 items
drwx------   - ernest  ernest           0 2017-10-20 05:29 /user/ernest
drwxrwxrwx   - mapred  hadoop           0 2017-10-20 05:28 /user/history
drwxrwxr-t   - hive    hive             0 2017-10-20 05:29 /user/hive
drwxrwxr-x   - hue     hue              0 2017-10-20 05:30 /user/hue
drwxrwxr-x   - oozie   oozie            0 2017-10-20 05:30 /user/oozie
drwx------   - siwicki siwicki          0 2017-10-20 05:29 /user/siwicki
```

```
[root@bmst1-cdh ~]# curl -u 'admin:admin' 'http://bmst1-cdh:7180/api/v14/hosts'
{
  "items" : [ {
    "hostId" : "i-09a20ae39a1c554d7",
    "ipAddress" : "172.31.27.173",
    "hostname" : "bedg1-cdh.hadoop",
    "rackId" : "/default",
    "hostUrl" : "http://bmst1-cdh.hadoop:7180/cmf/hostRedirect/i-09a20ae39a1c554d7",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 15332311040
  }, {
    "hostId" : "i-078248550aaff06de",
    "ipAddress" : "172.31.21.70",
    "hostname" : "bmst1-cdh.hadoop",
    "rackId" : "/default",
    "hostUrl" : "http://bmst1-cdh.hadoop:7180/cmf/hostRedirect/i-078248550aaff06de",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 15332311040
  }, {
    "hostId" : "i-09f7498e812ccc39e",
    "ipAddress" : "172.31.19.112",
    "hostname" : "bwrk1-cdh.hadoop",
    "rackId" : "/default",
    "hostUrl" : "http://bmst1-cdh.hadoop:7180/cmf/hostRedirect/i-09f7498e812ccc39e",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 15332311040
  }, {
    "hostId" : "i-0a8090c725ea2d00e",
    "ipAddress" : "172.31.29.6",
    "hostname" : "bwrk2-cdh.hadoop",
    "rackId" : "/default",
    "hostUrl" : "http://bmst1-cdh.hadoop:7180/cmf/hostRedirect/i-0a8090c725ea2d00e",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 15332311040
  }, {
    "hostId" : "i-0c1141500a2ee57fc",
    "ipAddress" : "172.31.25.105",
    "hostname" : "bwrk3-cdh.hadoop",
    "rackId" : "/default",
    "hostUrl" : "http://bmst1-cdh.hadoop:7180/cmf/hostRedirect/i-0c1141500a2ee57fc",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 15332311040
  } ]
}
```
