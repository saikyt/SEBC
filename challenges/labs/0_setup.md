* List the cloud provider you are using (AWS, GCE, Azure, CloudCat, other)
```
AWS

```
* List your instances by IP address and DNS name (don't use /etc/hosts for this)
```
ec2-34-193-87-160.compute-1.amazonaws.com
34.193.87.160
edgenode

ec2-34-193-151-84.compute-1.amazonaws.com
34.193.151.84
master

ec2-34-193-72-133.compute-1.amazonaws.com
34.193.72.133
snn

ec2-34-198-155-222.compute-1.amazonaws.com
34.198.155.222
dn1

ec2-34-198-170-245.compute-1.amazonaws.com
34.198.170.245
dn2
```
* List the Linux release you are using

```
[root@master yum.repos.d]# cat /etc/redhat-release
Red Hat Enterprise Linux Server release 7.3 (Maipo)

```

* List the file system capacity for the first node
```
[root@master yum.repos.d]# lsblk
NAME    MAJ:MIN RM SIZE RO TYPE MOUNTPOINT
xvda    202:0    0  30G  0 disk
├─xvda1 202:1    0   1M  0 part
└─xvda2 202:2    0  30G  0 part /
```

List the command and output for yum repolist enabled
```
Loaded plugins: amazon-id, rhui-lb, search-disabled-repos
repo id                                          repo name                status
rhui-REGION-client-config-server-7/x86_64        Red Hat Update Infrastru      6
rhui-REGION-rhel-server-releases/7Server/x86_64  Red Hat Enterprise Linux 14,473
rhui-REGION-rhel-server-rh-common/7Server/x86_64 Red Hat Enterprise Linux    228
repolist: 14,707

```
