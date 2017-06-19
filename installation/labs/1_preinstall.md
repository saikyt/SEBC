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
### After changing /etc/sysctl.conf you need to run sysctl -p to apply
```
 sysctl -p
```
## Change the vm.swappiness to 1 and restart the node
```
[root@ip-172-31-36-59 ec2-user]# cat /proc/sys/vm/swappiness
1
[root@ip-172-31-36-59 ec2-user]#
```
## Show mount attributes

```
/dev/xvda2 on / type xfs (rw,relatime,seclabel,attr2,inode64,noquota)
selinuxfs on /sys/fs/selinux type selinuxfs (rw,relatime)
systemd-1 on /proc/sys/fs/binfmt_misc type autofs (rw,relatime,fd=26,pgrp=1,timeout=300,minproto=5,maxproto=5,direct)
debugfs on /sys/kernel/debug type debugfs (rw,relatime)
mqueue on /dev/mqueue type mqueue (rw,relatime,seclabel)
hugetlbfs on /dev/hugepages type hugetlbfs (rw,relatime,seclabel)

```
## Disable transparent huge page support
### Check current status
```
[ec2-user@ip-172-31-40-234 ~]$ cat /sys/kernel/mm/transparent_hugepage/enabled
[always] madvise never
```
### Disable during startup
```
cat /etc/rc.local
#!/bin/bash
# THIS FILE IS ADDED FOR COMPATIBILITY PURPOSES
#
# It is highly advisable to create own systemd services or udev rules
# to run scripts during boot instead of using this file.
#
# In contrast to previous versions due to parallel execution during boot
# this script will NOT be run after all other services.
#
# Please note that you must run 'chmod +x /etc/rc.d/rc.local' to ensure
# that this script will be executed during boot.

touch /var/lock/subsys/local

sysctl -w vm.swappiness=1
if test -f /sys/kernel/mm/transparent_hugepage/enabled; then
   echo never > /sys/kernel/mm/transparent_hugepage/enabled
fi
```
### Disable during startup
```
chmod +x /etc/rc.d/rc.local
```
## Show interface configuration
```
eth0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 9001
        inet 172.31.40.234  netmask 255.255.240.0  broadcast 172.31.47.255
        inet6 fe80::811:2dff:fe34:4e4e  prefixlen 64  scopeid 0x20<link>
        ether 0a:11:2d:34:4e:4e  txqueuelen 1000  (Ethernet)
        RX packets 253  bytes 27788 (27.1 KiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 277  bytes 30451 (29.7 KiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        inet6 ::1  prefixlen 128  scopeid 0x10<host>
        loop  txqueuelen 0  (Local Loopback)
        RX packets 4  bytes 340 (340.0 B)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 4  bytes 340 (340.0 B)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0
```

