```
[ernest@bedg1-cdh ~]$ beeline
Java HotSpot(TM) 64-Bit Server VM warning: ignoring option MaxPermSize=512M; support was removed in 8.0
Java HotSpot(TM) 64-Bit Server VM warning: ignoring option MaxPermSize=512M; support was removed in 8.0
Beeline version 1.1.0-cdh5.9.3 by Apache Hive
beeline> !connect jdbc:hive2://localhost:10000/default;principal=hive/bedg1-cdh@G0DJ4CK4L.CO.UK
scan complete in 2ms
Connecting to jdbc:hive2://localhost:10000/default;principal=hive/bedg1-cdh@G0DJ4CK4L.CO.UK
Connected to: Apache Hive (version 1.1.0-cdh5.9.3)
Driver: Hive JDBC (version 1.1.0-cdh5.9.3)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://localhost:10000/default> SHOW TABLES;
INFO  : Compiling command(queryId=hive_20171020063232_b62ee3a9-98fe-4b35-a753-3950abfafe21): SHOW TABLES
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20171020063232_b62ee3a9-98fe-4b35-a753-3950abfafe21); Time taken: 0.059 seconds
INFO  : Executing command(queryId=hive_20171020063232_b62ee3a9-98fe-4b35-a753-3950abfafe21): SHOW TABLES
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171020063232_b62ee3a9-98fe-4b35-a753-3950abfafe21); Time taken: 0.107 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| customers  |
| sample_07  |
| sample_08  |
| web_logs   |
+------------+--+
4 rows selected (0.266 seconds)
```

```
[siwicki@bedg1-cdh ~]$ beeline
Java HotSpot(TM) 64-Bit Server VM warning: ignoring option MaxPermSize=512M; support was removed in 8.0
Java HotSpot(TM) 64-Bit Server VM warning: ignoring option MaxPermSize=512M; support was removed in 8.0
Beeline version 1.1.0-cdh5.9.3 by Apache Hive
beeline> !connect jdbc:hive2://localhost:10000/default;principal=hive/bedg1-cdh@G0DJ4CK4L.CO.UK
scan complete in 3ms
Connecting to jdbc:hive2://localhost:10000/default;principal=hive/bedg1-cdh@G0DJ4CK4L.CO.UK
Connected to: Apache Hive (version 1.1.0-cdh5.9.3)
Driver: Hive JDBC (version 1.1.0-cdh5.9.3)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://localhost:10000/default> SHOW TABLES;
INFO  : Compiling command(queryId=hive_20171020063737_d52e1156-e799-4216-80e1-c8a7bd3ebb5c): SHOW TABLES
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20171020063737_d52e1156-e799-4216-80e1-c8a7bd3ebb5c); Time taken: 0.06 seconds
INFO  : Executing command(queryId=hive_20171020063737_d52e1156-e799-4216-80e1-c8a7bd3ebb5c): SHOW TABLES
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171020063737_d52e1156-e799-4216-80e1-c8a7bd3ebb5c); Time taken: 0.135 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| sample_07  |
| sample_08  |
+------------+--+
2 rows selected (0.294 seconds)
```
