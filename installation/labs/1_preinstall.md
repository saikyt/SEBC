## Check vm.swappiness on one node
```
[root@ip-172-31-36-59 ec2-user]# cat /proc/sys/vm/swappiness
60
[root@ip-172-31-36-59 ec2-user]# vi /etc/sysc
sysconfig/   sysctl.conf  sysctl.d/
[root@ip-172-31-36-59 ec2-user]# vi /etc/sysc
sysconfig/   sysctl.conf  sysctl.d/
[root@ip-172-31-36-59 ec2-user]# vi /etc/sysctl.conf
```
## Change the vm.swappiness to 1 and restart the node
```
[root@ip-172-31-36-59 ec2-user]# cat /proc/sys/vm/swappiness
1
[root@ip-172-31-36-59 ec2-user]#
```


