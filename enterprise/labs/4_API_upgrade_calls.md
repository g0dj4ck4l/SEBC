**Report the latest available version of the API**
```
[root@aedg1-cdh58 centos]# curl -u 'g0dj4ck4l:cloudera' 'http://aedg1-cdh58:7180/api/version'
v14
```

**Report the CM version**
```
[root@aedg1-cdh58 centos]# curl -u 'g0dj4ck4l:cloudera' 'http://aedg1-cdh58:7180/api/v14/cm/version'
{
  "version" : "5.9.3",
  "buildUser" : "jenkins",
  "buildTimestamp" : "20170627-1506",
  "gitHash" : "23506bb4e114dd460bdac64c57a672e6be631907",
  "snapshot" : false
}
```

**List all CM users**
```
[root@aedg1-cdh58 centos]# curl -u 'g0dj4ck4l:cloudera' 'http://aedg1-cdh58:7180/api/v14/users'
{
  "items" : [ {
    "name" : "admin",
    "roles" : [ "ROLE_LIMITED" ]
  }, {
    "name" : "g0dj4ck4l",
    "roles" : [ "ROLE_ADMIN" ]
  }, {
    "name" : "minotaur",
    "roles" : [ "ROLE_CONFIGURATOR" ]
  } ]
}
```

**Report the database server in use by CM**
```
[root@aedg1-cdh58 centos]# curl -u 'g0dj4ck4l:cloudera' 'http://aedg1-cdh58:7180/api/v14/cm/scmDbInfo'
{
  "scmDbType" : "MYSQL",
  "embeddedDbUsed" : false
}
```
