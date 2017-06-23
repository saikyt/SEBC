## Host details running mysql
```
[root@edgenode yum.repos.d]# hostname -f
edgenode
[root@edgenode yum.repos.d]# ps -ef | grep mysql
root      9882     1  0 12:33 ?        00:00:00 /bin/sh /usr/bin/mysqld_safe --datadir=/var/lib/mysql --socket=/var/lib/mysql/mysql.sock --pid-file=/var/run/mysqld/mysqld.pid --basedir=/usr --user=mysql
mysql    10098  9882  0 12:33 ?        00:00:00 /usr/sbin/mysqld --basedir=/usr --datadir=/var/lib/mysql --plugin-dir=/usr/lib64/mysql/plugin --user=mysql --log-error=/var/log/mysqld.log --pid-file=/var/run/mysqld/mysqld.pid --socket=/var/lib/mysql/mysql.sock
root     10165  9316  0 12:45 pts/1    00:00:00 grep --color=auto mysql
```

## Database server version
```
[root@edgenode yum.repos.d]# mysql --version
mysql  Ver 14.14 Distrib 5.6.36, for Linux (x86_64) using  EditLine wrapper

```

## Databases contained
```
+--------------------+
| Database           |
+--------------------+
| information_schema |
| hive               |
| hue                |
| mysql              |
| oozie              |
| performance_schema |
| rman               |
| scm                |
+--------------------+
```
