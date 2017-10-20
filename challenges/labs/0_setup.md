**List the cloud provider you are using**
```
AWS
```

**List the Linux release you have chosen**
```
CentOS Linux release 7.2.1511 (Core)
```

**Show that the disk space on each node is at least 30 GB**
```
[root@bedg1-cdh ~]# df -h /
Filesystem               Size  Used Avail Use% Mounted on
/dev/mapper/centos-root   48G  1.9G   46G   4% /
```

```
[root@bmst1-cdh ~]# df -h /
Filesystem               Size  Used Avail Use% Mounted on
/dev/mapper/centos-root   48G  1.9G   46G   4% /
```

```
[root@bwrk1-cdh ~]# df -h /
Filesystem               Size  Used Avail Use% Mounted on
/dev/mapper/centos-root   48G  1.9G   46G   4% /
```

```
[root@bwrk2-cdh ~]# df -h /
Filesystem               Size  Used Avail Use% Mounted on
/dev/mapper/centos-root   48G  1.9G   46G   4% /
```

```
[root@bwrk3-cdh ~]# df -h /
Filesystem               Size  Used Avail Use% Mounted on
/dev/mapper/centos-root   48G  1.9G   46G   4% /
```

**List the command and output for yum repolist enabled**
```
[root@bedg1-cdh ~]# yum repolist enabled
Loaded plugins: fastestmirror
Loading mirror speeds from cached hostfile
 * base: ftp.heanet.ie
 * extras: ftp.heanet.ie
 * updates: ftp.heanet.ie
repo id                                                                                           repo name                                                                                           status
base/7/x86_64                                                                                     CentOS-7 - Base                                                                                     9,591
extras/7/x86_64                                                                                   CentOS-7 - Extras                                                                                     227
updates/7/x86_64                                                                                  CentOS-7 - Updates                                                                                    741
repolist: 10,559
```

**List the /etc/passwd entries for ernest and siwicki in your setup file**
```
[root@bedg1-cdh ~]# egrep 'ernest|siwicki' /etc/passwd
ernest:x:2000:2000::/home/ernest:/bin/bash
siwicki:x:3000:3000::/home/siwicki:/bin/bash
```

**List the /etc/group entries for usa and emea in your setup file**
```
[root@bedg1-cdh ~]# egrep 'usa|emea' /etc/group
usa:x:3001:ernest
emea:x:3002:siwicki
```
