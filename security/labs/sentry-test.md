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
## login as admin user and create roles

```
0: jdbc:hive2://edgenode:10000/default> create role reads;
INFO  : Compiling command(queryId=hive_20170622184242_14d3c522-8cf5-46bd-819f-648db0e6b300): create role reads
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20170622184242_14d3c522-8cf5-46bd-819f-648db0e6b300); Time taken: 0.054 seconds
INFO  : Executing command(queryId=hive_20170622184242_14d3c522-8cf5-46bd-819f-648db0e6b300): create role reads
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170622184242_14d3c522-8cf5-46bd-819f-648db0e6b300); Time taken: 0.04 seconds
INFO  : OK
No rows affected (0.105 seconds)
0: jdbc:hive2://edgenode:10000/default> create role writes;
INFO  : Compiling command(queryId=hive_20170622184242_86c358aa-7465-4aa1-94a9-83e38d76e232): create role writes
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20170622184242_86c358aa-7465-4aa1-94a9-83e38d76e232); Time taken: 0.054 seconds
INFO  : Executing command(queryId=hive_20170622184242_86c358aa-7465-4aa1-94a9-83e38d76e232): create role writes
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170622184242_86c358aa-7465-4aa1-94a9-83e38d76e232); Time taken: 0.025 seconds
INFO  : OK
No rows affected (0.091 seconds)
0: jdbc:hive2://edgenode:10000/default> GRANT SELECT ON DATABASE default TO ROLE reads;
INFO  : Compiling command(queryId=hive_20170622184646_19f0abe8-36f5-4c55-a74d-8a409951b064): GRANT SELECT ON DATABASE default TO ROLE reads
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20170622184646_19f0abe8-36f5-4c55-a74d-8a409951b064); Time taken: 0.059 seconds
INFO  : Executing command(queryId=hive_20170622184646_19f0abe8-36f5-4c55-a74d-8a409951b064): GRANT SELECT ON DATABASE default TO ROLE reads
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170622184646_19f0abe8-36f5-4c55-a74d-8a409951b064); Time taken: 0.039 seconds
INFO  : OK
No rows affected (0.108 seconds)
0: jdbc:hive2://edgenode:10000/default> GRANT ROLE reads TO GROUP selector;
INFO  : Compiling command(queryId=hive_20170622184646_61304f9b-c7c2-49b9-91ed-2b42c7fac800): GRANT ROLE reads TO GROUP selector
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20170622184646_61304f9b-c7c2-49b9-91ed-2b42c7fac800); Time taken: 0.052 seconds
INFO  : Executing command(queryId=hive_20170622184646_61304f9b-c7c2-49b9-91ed-2b42c7fac800): GRANT ROLE reads TO GROUP selector
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170622184646_61304f9b-c7c2-49b9-91ed-2b42c7fac800); Time taken: 0.038 seconds
INFO  : OK
No rows affected (0.102 seconds)
0: jdbc:hive2://edgenode:10000/default> REVOKE ALL ON DATABASE default FROM ROLE writes;
INFO  : Compiling command(queryId=hive_20170622184747_a60b14f7-16f5-4583-92ff-208decf9489b): REVOKE ALL ON DATABASE default FROM ROLE writes
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20170622184747_a60b14f7-16f5-4583-92ff-208decf9489b); Time taken: 0.054 seconds
INFO  : Executing command(queryId=hive_20170622184747_a60b14f7-16f5-4583-92ff-208decf9489b): REVOKE ALL ON DATABASE default FROM ROLE writes
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170622184747_a60b14f7-16f5-4583-92ff-208decf9489b); Time taken: 0.083 seconds
INFO  : OK
No rows affected (0.15 seconds)
0: jdbc:hive2://edgenode:10000/default> GRANT SELECT ON default.sample_07 TO ROLE writes;
INFO  : Compiling command(queryId=hive_20170622184747_ac4be058-5bbd-4e60-af20-2a8614dff724): GRANT SELECT ON default.sample_07 TO ROLE writes
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20170622184747_ac4be058-5bbd-4e60-af20-2a8614dff724); Time taken: 0.053 seconds
INFO  : Executing command(queryId=hive_20170622184747_ac4be058-5bbd-4e60-af20-2a8614dff724): GRANT SELECT ON default.sample_07 TO ROLE writes
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170622184747_ac4be058-5bbd-4e60-af20-2a8614dff724); Time taken: 0.041 seconds
INFO  : OK
No rows affected (0.105 seconds)
0: jdbc:hive2://edgenode:10000/default> GRANT ROLE writes TO GROUP inserters;
INFO  : Compiling command(queryId=hive_20170622184747_716797fe-28a2-4538-a825-9d809047ec9f): GRANT ROLE writes TO GROUP inserters
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20170622184747_716797fe-28a2-4538-a825-9d809047ec9f); Time taken: 0.051 seconds
INFO  : Executing command(queryId=hive_20170622184747_716797fe-28a2-4538-a825-9d809047ec9f): GRANT ROLE writes TO GROUP inserters
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170622184747_716797fe-28a2-4538-a825-9d809047ec9f); Time taken: 0.035 seconds
INFO  : OK
No rows affected (0.097 seconds)
0: jdbc:hive2://edgenode:10000/default>
```

## show tables for user ferdinand
```
[root@edgenode ec2-user]# sudo su ferdinand
[ferdinand@edgenode ec2-user]$ kinit
Password for ferdinand@HADOOP.COM:
[ferdinand@edgenode ec2-user]$ beeline
Beeline version 1.1.0-cdh5.9.2 by Apache Hive
beeline>  !connect jdbc:hive2://edgenode:10000/default;principal=hive/edgenode@H                                                                                                    ADOOP.COM
scan complete in 2ms
Connecting to jdbc:hive2://edgenode:10000/default;principal=hive/edgenode@HADOOP                                                                                                    .COM
Connected to: Apache Hive (version 1.1.0-cdh5.9.2)
Driver: Hive JDBC (version 1.1.0-cdh5.9.2)
Transaction isolation: TRANSACTION_REPEATABLE_READ

0: jdbc:hive2://edgenode:10000/default> show tables;
INFO  : Compiling command(queryId=hive_20170622190202_9001d52f-d71b-4a61-9a06-83ad7376a68d): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20170622190202_9001d52f-d71b-4a61-9a06-83ad7376a68d); Time taken: 0.053 seconds
INFO  : Executing command(queryId=hive_20170622190202_9001d52f-d71b-4a61-9a06-83ad7376a68d): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170622190202_9001d52f-d71b-4a61-9a06-83ad7376a68d); Time taken: 0.101 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| sample_07  |
+------------+--+
1 row selected (0.173 seconds)
0: jdbc:hive2://edgenode:10000/default>
```
## Show tables for george - see all tables;

```
[ec2-user@edgenode ~]$ sudo su george
[george@edgenode ec2-user]$ kinit
Password for george@HADOOP.COM:
[george@edgenode ec2-user]$ beeline
Beeline version 1.1.0-cdh5.9.2 by Apache Hive
beeline> !connect jdbc:hive2://edgenode:10000/default;principal=hive/edgenode@HADOOM.COM
scan complete in 2ms
Connecting to jdbc:hive2://edgenode:10000/default;principal=hive/edgenode@HADOOM.COM
Connected to: Apache Hive (version 1.1.0-cdh5.9.2)
Driver: Hive JDBC (version 1.1.0-cdh5.9.2)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://edgenode:10000/default> show tables;
INFO  : Compiling command(queryId=hive_20170622190303_e7f1e209-5e90-4be6-a4b2-51be2cb16bac): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20170622190303_e7f1e209-5e90-4be6-a4b2-51be2cb16bac); Time taken: 0.059 seconds
INFO  : Executing command(queryId=hive_20170622190303_e7f1e209-5e90-4be6-a4b2-51be2cb16bac): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170622190303_e7f1e209-5e90-4be6-a4b2-51be2cb16bac); Time taken: 0.123 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| sai_test   |
| sample_07  |
+------------+--+
2 rows selected (0.289 seconds)
0: jdbc:hive2://edgenode:10000/default>

```
