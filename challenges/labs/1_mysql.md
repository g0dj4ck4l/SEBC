**The hostname of your MySQL node**
```
[root@bedg1-cdh ~]# hostname -f
bedg1-cdh.hadoop
```

**The command and output for mysql --version**
```
[root@bedg1-cdh ~]# mysql --version
mysql  Ver 14.14 Distrib 5.5.58, for Linux (x86_64) using readline 5.1
```

**The command and output for listing MySQL databases**
```
[root@bedg1-cdh ~]# mysql -p -e "show databases"
Enter password:
+--------------------+
| Database           |
+--------------------+
| information_schema |
| hive               |
| hue                |
| mysql              |
| oozie              |
| performance_schema |
| rman               |
| scm                |
| sentry             |
+--------------------+
```
