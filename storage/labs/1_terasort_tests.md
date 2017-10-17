[g0dj4ck4l@aedg1-cdh58 ~]$ time (hadoop jar /opt/cloudera/parcels/CDH-5.8.3-1.cdh5.8.3.p0.2/jars/hadoop-examples.jar teragen -Dmapreduce.job.maps=4 -Ddfs.blocksize=33554432 100000000 /user/g0dj4ck4l/hdfs_
performance &> /tmp/teragen-hdfs_performance.out)

real    2m26.297s
user    0m6.200s
sys     0m0.287s

[g0dj4ck4l@aedg1-cdh58 ~]$ time (hadoop jar /opt/cloudera/parcels/CDH-5.8.3-1.cdh5.8.3.p0.2/jars/hadoop-examples.jar terasort /user/g0dj4ck4l/hdfs_performance /user/g0dj4ck4l/hdfs_performance_terasort  &>
 /tmp/terasort-hdfs_performance.out)

real    9m4.979s
user    0m10.120s
sys     0m0.471s
