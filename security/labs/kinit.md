**Show the kinit command you use to authenticate your test user**
```
[root@aedg1-cdh58 ~]# kinit cloudera-scm
Password for cloudera-scm@HADOOP.COM:
```

**Show The output from a klist command listing your credentials and ticket lifetime**
```
[root@aedg1-cdh58 ~]# klist
Ticket cache: FILE:/tmp/krb5cc_0
Default principal: cloudera-scm@HADOOP.COM

Valid starting       Expires              Service principal
10/19/2017 10:25:41  10/20/2017 10:25:41  krbtgt/HADOOP.COM@HADOOP.COM
        renew until 10/26/2017 10:25:41
```
