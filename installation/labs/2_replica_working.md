## Show mysql replica working
```
mysql> CHANGE MASTER TO MASTER_HOST='master', MASTER_USER='root', MASTER_PASSWORD='admin', MASTER_LOG_FILE='mysqld-bin.000002', MASTER_LOG_POS=325;
Query OK, 0 rows affected, 2 warnings (0.02 sec)

mysql> start slave;
Query OK, 0 rows affected (0.01 sec)

mysql> show slave status \G
*************************** 1. row ***************************
               Slave_IO_State: Waiting for master to send event
                  Master_Host: master
                  Master_User: root
                  Master_Port: 3306
                Connect_Retry: 60
              Master_Log_File: mysqld-bin.000002
          Read_Master_Log_Pos: 325
               Relay_Log_File: mysqld-relay-bin.000002
                Relay_Log_Pos: 284
        Relay_Master_Log_File: mysqld-bin.000002
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
          Exec_Master_Log_Pos: 325
              Relay_Log_Space: 458
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
                  Master_UUID: 4c844dec-5541-11e7-8420-0a54ade845dc
             Master_Info_File: /var/lib/mysql/master.info
                    SQL_Delay: 0
          SQL_Remaining_Delay: NULL
      Slave_SQL_Running_State: Slave has read all relay log; waiting for the slave I/O thread to update it
           Master_Retry_Count: 86400
                  Master_Bind:
      Last_IO_Error_Timestamp:
     Last_SQL_Error_Timestamp:
               Master_SSL_Crl:
           Master_SSL_Crlpath:
           Retrieved_Gtid_Set:
            Executed_Gtid_Set:
                Auto_Position: 0
1 row in set (0.00 sec)
```
### verfiy /var/log/mysqld.log
```
es not guarantee that the relay log info will be consistent, Error_code: 0
2017-06-19 19:23:09 11533 [Note] Slave SQL thread initialized, starting replication in log 'mysqld-bin.000002' at position 325, relay log './mysqld-relay-bin.000001' position: 4
2017-06-19 19:23:09 11533 [Note] Slave I/O thread: connected to master 'root@master:3306',replication started in log 'mysqld-bin.000002' at position 325

```
