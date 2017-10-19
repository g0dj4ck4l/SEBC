**Sentry Lab: Verify user privileges**
```
[root@aedg1-cdh58 ~]# kinit g0dj4ck4l
Password for g0dj4ck4l@HADOOP.COM:
[root@aedg1-cdh58 ~]# beeline -u 'jdbc:hive2://aedg1-cdh58:10000/default;principal=hive/aedg1-cdh58.hadoop@HADOOP.COM'
scan complete in 3ms
Connecting to jdbc:hive2://aedg1-cdh58:10000/default;principal=hive/aedg1-cdh58.hadoop@HADOOP.COM
Connected to: Apache Hive (version 1.1.0-cdh5.8.3)
Driver: Hive JDBC (version 1.1.0-cdh5.8.3)
Transaction isolation: TRANSACTION_REPEATABLE_READ
Beeline version 1.1.0-cdh5.8.3 by Apache Hive
0: jdbc:hive2://aedg1-cdh58:10000/default> SHOW TABLES;
INFO  : Compiling command(queryId=hive_20171019111515_9aa71080-adec-462b-8891-a80565dbc206): SHOW TABLES
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20171019111515_9aa71080-adec-462b-8891-a80565dbc206); Time taken: 0.689 seconds
INFO  : Executing command(queryId=hive_20171019111515_9aa71080-adec-462b-8891-a80565dbc206): SHOW TABLES
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171019111515_9aa71080-adec-462b-8891-a80565dbc206); Time taken: 0.172 seconds
INFO  : OK
+-----------+--+
| tab_name  |
+-----------+--+
+-----------+--+
No rows selected (2.073 seconds)
0: jdbc:hive2://aedg1-cdh58:10000/default>
```

**Sentry Lab: create a Sentry role with full authorization**
```
0: jdbc:hive2://aedg1-cdh58:10000/default> CREATE ROLE sentry_admin;
INFO  : Compiling command(queryId=hive_20171019111616_82db7bd8-5a4f-4edf-80dd-77fd4e62e7e8): CREATE ROLE sentry_admin
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20171019111616_82db7bd8-5a4f-4edf-80dd-77fd4e62e7e8); Time taken: 0.074 seconds
INFO  : Executing command(queryId=hive_20171019111616_82db7bd8-5a4f-4edf-80dd-77fd4e62e7e8): CREATE ROLE sentry_admin
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171019111616_82db7bd8-5a4f-4edf-80dd-77fd4e62e7e8); Time taken: 0.635 seconds
INFO  : OK
No rows affected (0.721 seconds)
0: jdbc:hive2://aedg1-cdh58:10000/default> GRANT ALL ON SERVER server1 TO ROLE sentry_admin;
INFO  : Compiling command(queryId=hive_20171019111616_0e802a71-7a7a-4413-be13-af85de96f023): GRANT ALL ON SERVER server1 TO ROLE sentry_admin
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20171019111616_0e802a71-7a7a-4413-be13-af85de96f023); Time taken: 0.084 seconds
INFO  : Executing command(queryId=hive_20171019111616_0e802a71-7a7a-4413-be13-af85de96f023): GRANT ALL ON SERVER server1 TO ROLE sentry_admin
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171019111616_0e802a71-7a7a-4413-be13-af85de96f023); Time taken: 0.095 seconds
INFO  : OK
No rows affected (0.187 seconds)
0: jdbc:hive2://aedg1-cdh58:10000/default> GRANT ROLE sentry_admin TO GROUP g0dj4ck4l;
INFO  : Compiling command(queryId=hive_20171019111616_580ba91d-05de-4f06-a894-e48913b3b2a1): GRANT ROLE sentry_admin TO GROUP g0dj4ck4l
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20171019111616_580ba91d-05de-4f06-a894-e48913b3b2a1); Time taken: 0.061 seconds
INFO  : Executing command(queryId=hive_20171019111616_580ba91d-05de-4f06-a894-e48913b3b2a1): GRANT ROLE sentry_admin TO GROUP g0dj4ck4l
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171019111616_580ba91d-05de-4f06-a894-e48913b3b2a1); Time taken: 0.075 seconds
INFO  : OK
No rows affected (0.145 seconds)
0: jdbc:hive2://aedg1-cdh58:10000/default> SHOW TABLES;
INFO  : Compiling command(queryId=hive_20171019111616_6106eba7-1306-4c23-b90b-4793e8e46519): SHOW TABLES
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20171019111616_6106eba7-1306-4c23-b90b-4793e8e46519); Time taken: 0.061 seconds
INFO  : Executing command(queryId=hive_20171019111616_6106eba7-1306-4c23-b90b-4793e8e46519): SHOW TABLES
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171019111616_6106eba7-1306-4c23-b90b-4793e8e46519); Time taken: 0.155 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| customers  |
| sample_07  |
| sample_08  |
| web_logs   |
+------------+--+
4 rows selected (0.271 seconds)
```

**Sentry Lab: kinit as george, then login to beeline**
```
[root@aedg1-cdh58 ~]# kinit george
Password for george@HADOOP.COM:
[root@aedg1-cdh58 ~]# beeline -u 'jdbc:hive2://aedg1-cdh58:10000/default;principal=hive/aedg1-cdh58.hadoop@HADOOP.COM'
scan complete in 3ms
Connecting to jdbc:hive2://aedg1-cdh58:10000/default;principal=hive/aedg1-cdh58.hadoop@HADOOP.COM
Connected to: Apache Hive (version 1.1.0-cdh5.8.3)
Driver: Hive JDBC (version 1.1.0-cdh5.8.3)
Transaction isolation: TRANSACTION_REPEATABLE_READ
Beeline version 1.1.0-cdh5.8.3 by Apache Hive
0: jdbc:hive2://aedg1-cdh58:10000/default> SHOW TABLES;
INFO  : Compiling command(queryId=hive_20171019113131_a0f03240-70d8-4f38-8ca8-55a00f3d0fe2): SHOW TABLES
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20171019113131_a0f03240-70d8-4f38-8ca8-55a00f3d0fe2); Time taken: 0.084 seconds
INFO  : Executing command(queryId=hive_20171019113131_a0f03240-70d8-4f38-8ca8-55a00f3d0fe2): SHOW TABLES
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171019113131_a0f03240-70d8-4f38-8ca8-55a00f3d0fe2); Time taken: 0.138 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| customers  |
| sample_07  |
| sample_08  |
| web_logs   |
+------------+--+
4 rows selected (0.342 seconds)
```

**Sentry Lab: kinit as ferdinand, then login to beeline**
```
[root@aedg1-cdh58 ~]# kinit ferdinand
Password for ferdinand@HADOOP.COM:
[root@aedg1-cdh58 ~]# beeline -u 'jdbc:hive2://aedg1-cdh58:10000/default;principal=hive/aedg1-cdh58.h
adoop@HADOOP.COM'
scan complete in 2ms
Connecting to jdbc:hive2://aedg1-cdh58:10000/default;principal=hive/aedg1-cdh58.hadoop@HADOOP.COM
Connected to: Apache Hive (version 1.1.0-cdh5.8.3)
Driver: Hive JDBC (version 1.1.0-cdh5.8.3)
Transaction isolation: TRANSACTION_REPEATABLE_READ
Beeline version 1.1.0-cdh5.8.3 by Apache Hive
0: jdbc:hive2://aedg1-cdh58:10000/default> SHOW TABLES;
INFO  : Compiling command(queryId=hive_20171019113333_16c789a5-3e4c-4046-b862-1f1cee2ec5bf): SHOW TABLES
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20171019113333_16c789a5-3e4c-4046-b862-1f1cee2ec5bf); Time taken: 0.066 seconds
INFO  : Executing command(queryId=hive_20171019113333_16c789a5-3e4c-4046-b862-1f1cee2ec5bf): SHOW TABLES
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171019113333_16c789a5-3e4c-4046-b862-1f1cee2ec5bf); Time taken: 0.13 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| sample_07  |
+------------+--+
1 row selected (0.325 seconds)
```
