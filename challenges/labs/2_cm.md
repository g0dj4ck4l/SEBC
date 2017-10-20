```
[root@bmst1-cdh ~]$ ls -ltr /etc/yum.repos.d/
total 44
-rw-r--r--. 1 root root 1952 Dec  9  2015 CentOS-Vault.repo
-rw-r--r--. 1 root root 1331 Dec  9  2015 CentOS-Sources.repo
-rw-r--r--. 1 root root  630 Dec  9  2015 CentOS-Media.repo
-rw-r--r--. 1 root root  290 Dec  9  2015 CentOS-fasttrack.repo
-rw-r--r--. 1 root root  649 Dec  9  2015 CentOS-Debuginfo.repo
-rw-r--r--. 1 root root 1309 Dec  9  2015 CentOS-CR.repo
-rw-r--r--. 1 root root 1664 Dec  9  2015 CentOS-Base.repo
-rw-r--r--  1 root root 1885 Apr 27 05:14 mysql-community-source.repo
-rw-r--r--  1 root root 1838 Oct 20 04:02 mysql-community.repo
-rw-r--r--  1 root root  206 Oct 20 04:40 cloudera-manager.repo.~1~
-rw-r--r--  1 root root  211 Oct 20 05:13 cloudera-manager.repo
```

```
[root@bmst1-cdh ~]# /usr/share/cmf/schema/scm_prepare_database.sh -h bedg1-cdh.hadoop mysql scm scm Scm_tai2017
JAVA_HOME=/usr/java/jdk1.8.0_131
Verifying that we can write to /etc/cloudera-scm-server
Creating SCM configuration file in /etc/cloudera-scm-server
Executing:  /usr/java/jdk1.8.0_131/bin/java -cp /usr/share/java/mysql-connector-java.jar:/usr/share/java/oracle-connector-java.jar:/usr/share/cmf/schema/../lib/* com.cloudera.enterprise.dbutil.DbCommandExecutor /etc/cloudera-scm-server/db.properties com.cloudera.cmf.db.
[                          main] DbCommandExecutor              INFO  Successfully connected to database.
All done, your SCM database is configured correctly!
```
