[root@amst1-cdh58 ~]# mysql -u root -p -e 'SHOW SLAVE STATUS \G'
Enter password:
*************************** 1. row ***************************
               Slave_IO_State: Waiting for master to send event
                  Master_Host: aedg1-cdh58.hadoop
                  Master_User: ruser
                  Master_Port: 3306
                Connect_Retry: 10
              Master_Log_File: master1-bin.000001
          Read_Master_Log_Pos: 47218302
               Relay_Log_File: mariadb-relay-bin.000002
                Relay_Log_Pos: 47218588
        Relay_Master_Log_File: master1-bin.000001
             Slave_IO_Running: Yes
            Slave_SQL_Running: Yes
              Replicate_Do_DB:
          Replicate_Ignore_DB:
           Replicate_Do_Table:
       Replicate_Ignore_Table:
      Replicate_Wild_Do_Table:
  Replicate_Wild_Ignore_Table:
                   Last_Errno: 0
                   Last_Error:
                 Skip_Counter: 0
          Exec_Master_Log_Pos: 47218302
              Relay_Log_Space: 47218884
              Until_Condition: None
               Until_Log_File:
                Until_Log_Pos: 0
           Master_SSL_Allowed: No
           Master_SSL_CA_File:
           Master_SSL_CA_Path:
              Master_SSL_Cert:
            Master_SSL_Cipher:
               Master_SSL_Key:
        Seconds_Behind_Master: 0
Master_SSL_Verify_Server_Cert: No
                Last_IO_Errno: 0
                Last_IO_Error:
               Last_SQL_Errno: 0
               Last_SQL_Error:
  Replicate_Ignore_Server_Ids:
             Master_Server_Id: 1
