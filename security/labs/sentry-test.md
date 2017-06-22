## Login as the user you created on all the nodes
```
[ec2-user@edgenode ~]$ sudo su mylinuxuser

```
## kinit with that user
```
[mylinuxuser@edgenode ec2-user]$ kinit
Password for mylinuxuser@HADOOP.COM:
[mylinuxuser@edgenode ec2-user]$ klist
Ticket cache: FILE:/tmp/krb5cc_1001
Default principal: mylinuxuser@HADOOP.COM

Valid starting       Expires              Service principal
06/22/2017 17:02:11  06/23/2017 17:02:11  krbtgt/HADOOP.COM@HADOOP.COM
        renew until 06/29/2017 17:02:11
 ```
 ## login into beeline
 ```
[mylinuxuser@edgenode ec2-user]$ beeline
Beeline version 1.1.0-cdh5.9.2 by Apache Hive
beeline> !connect jdbc:hive2://edgenode:10000/default;principal=hive/edgenode@HADOOP.COM
scan complete in 2ms
Connecting to jdbc:hive2://edgenode:10000/default;principal=hive/edgenode@HADOOP.COM
Connected to: Apache Hive (version 1.1.0-cdh5.9.2)
Driver: Hive JDBC (version 1.1.0-cdh5.9.2)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://edgenode:10000/default> show tables;
INFO  : Compiling command(queryId=hive_20170622170303_81174efa-92b7-49bb-a264-5645c555078c): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20170622170303_81174efa-92b7-49bb-a264-5645c555078c); Time taken: 0.648 seconds
INFO  : Executing command(queryId=hive_20170622170303_81174efa-92b7-49bb-a264-5645c555078c): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170622170303_81174efa-92b7-49bb-a264-5645c555078c); Time taken: 0.22 seconds
INFO  : OK
+-----------+--+
| tab_name  |
+-----------+--+
+-----------+--+
No rows selected (2.222 seconds)
0: jdbc:hive2://edgenode:10000/default>

```
