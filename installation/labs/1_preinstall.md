**1. Check vm.swappiness on all your nodes**
[root@aedg1-cdh58 ~]# sysctl vm.swappiness
vm.swappiness = 1

**2. Show the mount attributes of all volumes**
[root@aedg1-cdh58 ~]# mount
sysfs on /sys type sysfs (rw,nosuid,nodev,noexec,relatime)
proc on /proc type proc (rw,nosuid,nodev,noexec,relatime)
devtmpfs on /dev type devtmpfs (rw,nosuid,size=7607712k,nr_inodes=1901928,mode=755)
securityfs on /sys/kernel/security type securityfs (rw,nosuid,nodev,noexec,relatime)
tmpfs on /dev/shm type tmpfs (rw,nosuid,nodev)
devpts on /dev/pts type devpts (rw,nosuid,noexec,relatime,gid=5,mode=620,ptmxmode=000)
tmpfs on /run type tmpfs (rw,nosuid,nodev,mode=755)
tmpfs on /sys/fs/cgroup type tmpfs (ro,nosuid,nodev,noexec,mode=755)
cgroup on /sys/fs/cgroup/systemd type cgroup (rw,nosuid,nodev,noexec,relatime,xattr,release_agent=/usr/lib/systemd/systemd-cgroups-agent,name=systemd)
pstore on /sys/fs/pstore type pstore (rw,nosuid,nodev,noexec,relatime)
cgroup on /sys/fs/cgroup/memory type cgroup (rw,nosuid,nodev,noexec,relatime,memory)
cgroup on /sys/fs/cgroup/freezer type cgroup (rw,nosuid,nodev,noexec,relatime,freezer)
cgroup on /sys/fs/cgroup/net_cls type cgroup (rw,nosuid,nodev,noexec,relatime,net_cls)
cgroup on /sys/fs/cgroup/cpu,cpuacct type cgroup (rw,nosuid,nodev,noexec,relatime,cpuacct,cpu)
cgroup on /sys/fs/cgroup/devices type cgroup (rw,nosuid,nodev,noexec,relatime,devices)
cgroup on /sys/fs/cgroup/perf_event type cgroup (rw,nosuid,nodev,noexec,relatime,perf_event)
cgroup on /sys/fs/cgroup/hugetlb type cgroup (rw,nosuid,nodev,noexec,relatime,hugetlb)
cgroup on /sys/fs/cgroup/cpuset type cgroup (rw,nosuid,nodev,noexec,relatime,cpuset)
cgroup on /sys/fs/cgroup/blkio type cgroup (rw,nosuid,nodev,noexec,relatime,blkio)
configfs on /sys/kernel/config type configfs (rw,relatime)
/dev/mapper/centos-root on / type xfs (rw,relatime,attr2,inode64,noquota)
systemd-1 on /proc/sys/fs/binfmt_misc type autofs (rw,relatime,fd=30,pgrp=1,timeout=300,minproto=5,maxproto=5,direct)
mqueue on /dev/mqueue type mqueue (rw,relatime)
hugetlbfs on /dev/hugepages type hugetlbfs (rw,relatime)
debugfs on /sys/kernel/debug type debugfs (rw,relatime)
/dev/xvda1 on /boot type xfs (rw,relatime,attr2,inode64,noquota)
tmpfs on /run/user/1000 type tmpfs (rw,nosuid,nodev,relatime,size=1497296k,mode=700,uid=1000,gid=1000)
binfmt_misc on /proc/sys/fs/binfmt_misc type binfmt_misc (rw,relatime)

**3. Show the reserve space of any non-root, ext-based volumes: XFS volumes do not maintain reserve space**
All non-root partitions are XFS

**4. Disable transparent hugepage support**
[root@aedg1-cdh58 ~]# cat /sys/kernel/mm/transparent_hugepage/enabled && cat /sys/kernel/mm/transparent_hugepage/defrag
always madvise [never]
always madvise [never]

**5. List your network interface configuration**
[root@aedg1-cdh58 ~]# ip a
1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN
    link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
    inet 127.0.0.1/8 scope host lo
       valid_lft forever preferred_lft forever
    inet6 ::1/128 scope host
       valid_lft forever preferred_lft forever
2: eth0: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 9001 qdisc pfifo_fast state UP qlen 1000
    link/ether 06:3b:44:6a:df:08 brd ff:ff:ff:ff:ff:ff
    inet 172.31.27.154/20 brd 172.31.31.255 scope global dynamic eth0
       valid_lft 3292sec preferred_lft 3292sec
    inet6 fe80::43b:44ff:fe6a:df08/64 scope link
       valid_lft forever preferred_lft forever

**6. List forward and reverse host lookups using getent or nslookup**
[root@aedg1-cdh58 ~]# for i in $(cat /etc/hosts | grep -v local | cut -d' ' -f1); do echo -n "Resolving $i: "; getent hosts $i; done
Resolving 172.31.21.83: 172.31.21.83    amst1-cdh58.hadoop amst1-cdh58
Resolving 172.31.27.154: 172.31.27.154   aedg1-cdh58.hadoop aedg1-cdh58
Resolving 172.31.18.8: 172.31.18.8     awrk1-cdh58.hadoop awrk1-cdh58
Resolving 172.31.20.76: 172.31.20.76    awrk2-cdh58.hadoop awrk2-cdh58
Resolving 172.31.31.23: 172.31.31.23    awrk3-cdh58.hadoop awrk3-cdh58

[root@aedg1-cdh58 ~]# for i in $(cat /etc/hosts | grep -v local | cut -d' ' -f3); do echo -n "Resolving $i: "; getent hosts $i; done
Resolving amst1-cdh58: 172.31.21.83    amst1-cdh58.hadoop amst1-cdh58
Resolving aedg1-cdh58: 172.31.27.154   aedg1-cdh58.hadoop aedg1-cdh58
Resolving awrk1-cdh58: 172.31.18.8     awrk1-cdh58.hadoop awrk1-cdh58
Resolving awrk2-cdh58: 172.31.20.76    awrk2-cdh58.hadoop awrk2-cdh58
Resolving awrk3-cdh58: 172.31.31.23    awrk3-cdh58.hadoop awrk3-cdh58

**7. Show the nscd service is running**
[root@aedg1-cdh58 ~]# systemctl status nscd
● nscd.service - Name Service Cache Daemon
   Loaded: loaded (/usr/lib/systemd/system/nscd.service; enabled; vendor preset: disabled)
   Active: active (running) since Mon 2017-10-16 16:41:01 EDT; 3min 10s ago
  Process: 673 ExecStart=/usr/sbin/nscd $NSCD_OPTIONS (code=exited, status=0/SUCCESS)
 Main PID: 679 (nscd)
   CGroup: /system.slice/nscd.service
           └─679 /usr/sbin/nscd

Oct 16 16:41:01 aedg1-cdh58.hadoop nscd[679]: 679 monitoring directory `/etc` (2)
Oct 16 16:41:01 aedg1-cdh58.hadoop nscd[679]: 679 monitoring file `/etc/resolv.conf` (5)
Oct 16 16:41:01 aedg1-cdh58.hadoop nscd[679]: 679 monitoring directory `/etc` (2)
Oct 16 16:41:01 aedg1-cdh58.hadoop nscd[679]: 679 monitoring file `/etc/services` (6)
Oct 16 16:41:01 aedg1-cdh58.hadoop nscd[679]: 679 monitoring directory `/etc` (2)
Oct 16 16:41:01 aedg1-cdh58.hadoop nscd[679]: 679 disabled inotify-based monitoring for file `/etc/netgroup': No such file or directory
Oct 16 16:41:01 aedg1-cdh58.hadoop nscd[679]: 679 stat failed for file `/etc/netgroup'; will try again later: No such file or directory
Oct 16 16:41:01 aedg1-cdh58.hadoop systemd[1]: Started Name Service Cache Daemon.
Oct 16 16:41:01 aedg1-cdh58.hadoop nscd[679]: 679 monitored file `/etc/resolv.conf` was moved into place, adding watch
Oct 16 16:41:21 aedg1-cdh58.hadoop nscd[679]: 679 checking for monitored file `/etc/netgroup': No such file or directory

**8. Show the ntpd service is running**
[root@aedg1-cdh58 ~]# systemctl status ntpd
● ntpd.service - Network Time Service
   Loaded: loaded (/usr/lib/systemd/system/ntpd.service; enabled; vendor preset: disabled)
   Active: active (running) since Mon 2017-10-16 16:41:01 EDT; 3min 32s ago
  Process: 664 ExecStart=/usr/sbin/ntpd -u ntp:ntp $OPTIONS (code=exited, status=0/SUCCESS)
 Main PID: 669 (ntpd)
   CGroup: /system.slice/ntpd.service
           └─669 /usr/sbin/ntpd -u ntp:ntp -g

Oct 16 16:41:03 aedg1-cdh58.hadoop ntpd_intres[685]: DNS 0.centos.pool.ntp.org -> 54.229.222.210
Oct 16 16:41:03 aedg1-cdh58.hadoop ntpd_intres[685]: DNS 1.centos.pool.ntp.org -> 193.1.31.66
Oct 16 16:41:03 aedg1-cdh58.hadoop ntpd_intres[685]: DNS 2.centos.pool.ntp.org -> 89.234.64.77
Oct 16 16:41:03 aedg1-cdh58.hadoop ntpd_intres[685]: DNS 3.centos.pool.ntp.org -> 173.51.147.14
Oct 16 16:41:04 aedg1-cdh58.hadoop ntpd[669]: Listen normally on 4 eth0 172.31.27.154 UDP 123
Oct 16 16:41:04 aedg1-cdh58.hadoop ntpd[669]: Listen normally on 5 eth0 fe80::43b:44ff:fe6a:df08 UDP 123
Oct 16 16:41:04 aedg1-cdh58.hadoop ntpd[669]: new interface(s) found: waking up resolver
Oct 16 16:41:11 aedg1-cdh58.hadoop ntpd[669]: 0.0.0.0 c61c 0c clock_step +0.706962 s
Oct 16 16:41:12 aedg1-cdh58.hadoop ntpd[669]: 0.0.0.0 c614 04 freq_mode
Oct 16 16:41:13 aedg1-cdh58.hadoop ntpd[669]: 0.0.0.0 c618 08 no_sys_peer
