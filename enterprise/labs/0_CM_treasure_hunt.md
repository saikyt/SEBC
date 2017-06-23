## * What is ubertask optimization?
This is a configuration setting in YARN to decide Whether to enable ubertask optimization, which runs "sufficiently small" jobs sequentially within a single JVM. "Small" is defined by the mapreduce.job.ubertask.maxmaps, mapreduce.job.ubertask.maxreduces, and mapreduce.job.ubertask.maxbytes settings.

## * Where in CM is the Kerberos Security Realm value displayed?
Under Administration -> Category -> Kerberos

## * Which CDH service(s) host a property for enabling Kerberos authentication?
Zookeeber, YARN and HDFS
## * How do you upgrade the CM agents?
ON clouera manager click on HOSTS -> ReRun Upgrade wizard
## * Give the tsquery statement used to chart Hue's CPU utilization?
select total_cpu_user where serviceType=HUE
## * Name all the roles that make up the Hive service
* Gateway
* Hive Metastore Server
* HiveServer
* WebHCat Server

## * What steps must be completed before integrating Cloudera Manager with Kerberos?

* Step 1:To install packages for KDC/Kerberos server
```
yum -y install krb5-server krb5-libs krb5-auth-dialog krb5-workstation
To install packages for a Kerberos client:
```
* Step 2: Install client kerberos packages on all nodes
```
 yum -y install krb5-workstation krb5-libs krb5-auth-dialog
 ```
* Step 3: Configure kdc.conf on Admin server (KDC)
vim /var/kerberos/krb5kdc/kdc.conf

* Step 4: configure krb5.conf to update realm name and kdc amin details etc on each node

* Step 5: Create the database using the kdb5_util utility. (Server)
```
# /usr/sbin/kdb5_util create -s
```
* Step 6: In Server, add cloudera-scm principal, it will be used by Cloudera Manager later to manage Hadoop principals.
```
# kadmin.local
kadmin.local:  addprinc cloudera-scm@HADOOP.COM
WARNING: no policy specified for cloudera-scm@HADOOP.COM; defaulting to no policy
Enter password for principal "cloudera-scm@HADOOP.COM":
Re-enter password for principal "cloudera-scm@HADOOP.COM":
Principal "cloudera-scm@HADOOP.COM" created.
```
* Step 7: Add */admin and cloudera-scm to ACL(Access Control List), which gives privilege to add principals for admin and cloudera-scm principal
```
# vi /var/kerberos/krb5kdc/kadm5.acl 
*/admin@HADOOP.COM *
cloudera-scm@HADOOP.COM admilc
```
* Step 8: Adds the password policy to the database.
```
# kadmin.local
kadmin.local:  addpol admin
kadmin.local:  addpol users
kadmin.local:  addpol hosts
kadmin.local:  exit
```
Step 9: Start Kerberos 
```
#service krb5kdc start
#service kadmin start
```
