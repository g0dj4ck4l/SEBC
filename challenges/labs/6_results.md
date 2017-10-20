```
0: jdbc:hive2://localhost:10000/default> SHOW TABLES;
INFO  : Compiling command(queryId=hive_20171020061717_09bc3f2d-d8c2-43ba-b520-254f6e388d63): SHOW TABLES
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20171020061717_09bc3f2d-d8c2-43ba-b520-254f6e388d63); Time taken: 1.624 seconds
INFO  : Executing command(queryId=hive_20171020061717_09bc3f2d-d8c2-43ba-b520-254f6e388d63): SHOW TABLES
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171020061717_09bc3f2d-d8c2-43ba-b520-254f6e388d63); Time taken: 0.492 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| customers  |
| sample_07  |
| sample_08  |
| web_logs   |
+------------+--+
4 rows selected (2.748 seconds)
```

```
[siwicki@bedg1-cdh ~]$ beeline
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
INFO  : Compiling command(queryId=hive_20171020062222_1760eeaa-b0e0-4e85-b4fd-ef176f34bfb6): SHOW TABLES
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20171020062222_1760eeaa-b0e0-4e85-b4fd-ef176f34bfb6); Time taken: 0.057 seconds
INFO  : Executing command(queryId=hive_20171020062222_1760eeaa-b0e0-4e85-b4fd-ef176f34bfb6): SHOW TABLES
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171020062222_1760eeaa-b0e0-4e85-b4fd-ef176f34bfb6); Time taken: 0.117 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| sample_07  |
+------------+--+
1 row selected (0.271 seconds)
```
