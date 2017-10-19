```
[hdfs@amst1-cdh58 ~]$ hdfs fsck /user/g0dj4ck4l -files -blocks
Connecting to namenode via http://amst1-cdh58.hadoop:50070
FSCK started by hdfs (auth:SIMPLE) from /172.31.21.83 for path /user/g0dj4ck4l at Tue Oct 17 08:09:16 EDT 2017
/user/g0dj4ck4l <dir>
/user/g0dj4ck4l/_SUCCESS 0 bytes, 0 block(s):  OK

/user/g0dj4ck4l/part-m-00000 250000000 bytes, 2 block(s):  OK
0. BP-1280794202-172.31.21.83-1508193034219:blk_1073743720_2896 len=134217728 Live_repl=3
1. BP-1280794202-172.31.21.83-1508193034219:blk_1073743722_2898 len=115782272 Live_repl=3

/user/g0dj4ck4l/part-m-00001 250000000 bytes, 2 block(s):  OK
0. BP-1280794202-172.31.21.83-1508193034219:blk_1073743721_2897 len=134217728 Live_repl=3
1. BP-1280794202-172.31.21.83-1508193034219:blk_1073743723_2899 len=115782272 Live_repl=3

Status: HEALTHY
 Total size:    500000000 B
 Total dirs:    1
 Total files:   3
 Total symlinks:                0
 Total blocks (validated):      4 (avg. block size 125000000 B)
 Minimally replicated blocks:   4 (100.0 %)
 Over-replicated blocks:        0 (0.0 %)
 Under-replicated blocks:       0 (0.0 %)
 Mis-replicated blocks:         0 (0.0 %)
 Default replication factor:    3
 Average block replication:     3.0
 Corrupt blocks:                0
 Missing replicas:              0 (0.0 %)
 Number of data-nodes:          3
 Number of racks:               1
FSCK ended at Tue Oct 17 08:09:16 EDT 2017 in 1 milliseconds


The filesystem under path '/user/g0dj4ck4l' is HEALTHY
```

```
[hdfs@amst1-cdh58 ~]$ hdfs fsck /user/ale966 -files -blocks
Connecting to namenode via http://amst1-cdh58.hadoop:50070
FSCK started by hdfs (auth:SIMPLE) from /172.31.21.83 for path /user/ale966 at Tue Oct 17 08:07:23 EDT 2017
/user/ale966 <dir>
/user/ale966/_SUCCESS 0 bytes, 0 block(s):  OK

/user/ale966/part-m-00000 250000000 bytes, 2 block(s):  OK
0. BP-1280794202-172.31.21.83-1508193034219:blk_1073743890_3066 len=134217728 Live_repl=3
1. BP-1280794202-172.31.21.83-1508193034219:blk_1073743893_3069 len=115782272 Live_repl=3

/user/ale966/part-m-00001 250000000 bytes, 2 block(s):  OK
0. BP-1280794202-172.31.21.83-1508193034219:blk_1073743892_3068 len=134217728 Live_repl=3
1. BP-1280794202-172.31.21.83-1508193034219:blk_1073743894_3070 len=115782272 Live_repl=3

Status: HEALTHY
 Total size:    500000000 B
 Total dirs:    1
 Total files:   3
 Total symlinks:                0
 Total blocks (validated):      4 (avg. block size 125000000 B)
 Minimally replicated blocks:   4 (100.0 %)
 Over-replicated blocks:        0 (0.0 %)
 Under-replicated blocks:       0 (0.0 %)
 Mis-replicated blocks:         0 (0.0 %)
 Default replication factor:    3
 Average block replication:     3.0
 Corrupt blocks:                0
 Missing replicas:              0 (0.0 %)
 Number of data-nodes:          3
 Number of racks:               1
FSCK ended at Tue Oct 17 08:07:23 EDT 2017 in 1 milliseconds


The filesystem under path '/user/ale966' is HEALTHY
```
