## Kinit command used to create HDFS directories
```
kinit hdfs/master@HADOOP.COM -k -t  /var/run/cloudera-scm-agent/process/139-hdfs-DATANODE/hdfs.keytab
```
### Then run the hadoop command to create the user folder

```
hdfs dfs -mkdir /user/mylinuxuser
```
