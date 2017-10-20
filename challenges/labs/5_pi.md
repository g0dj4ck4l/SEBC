```
[siwicki@bedg1-cdh ~]$ hadoop jar /opt/cloudera/parcels/CDH/jars/hadoop-examples.jar pi 1 1
Number of Maps  = 1
Samples per Map = 1
Wrote input for Map #0
Starting Job
17/10/20 06:01:45 INFO client.RMProxy: Connecting to ResourceManager at bedg1-cdh.hadoop/172.31.27.173:8032
17/10/20 06:01:45 INFO hdfs.DFSClient: Created token for siwicki: HDFS_DELEGATION_TOKEN owner=siwicki@G0DJ4CK4L.CO.UK, renewer=yarn, realUser=, issueDate=1508493705613, maxDate=1509098505613, sequenceNumber=2, masterKeyId=2 on 172.31.27.173:8020
17/10/20 06:01:45 INFO security.TokenCache: Got dt for hdfs://bedg1-cdh.hadoop:8020; Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.27.173:8020, Ident: (token for siwicki: HDFS_DELEGATION_TOKEN owner=siwicki@G0DJ4CK4L.CO.UK, renewer=yarn, realUser=, issueDate=1508493705613, maxDate=1509098505613, sequenceNumber=2, masterKeyId=2)
17/10/20 06:01:45 INFO input.FileInputFormat: Total input paths to process : 1
17/10/20 06:01:45 INFO mapreduce.JobSubmitter: number of splits:1
17/10/20 06:01:45 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1508493348273_0002
17/10/20 06:01:45 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.27.173:8020, Ident: (token for siwicki: HDFS_DELEGATION_TOKEN owner=siwicki@G0DJ4CK4L.CO.UK, renewer=yarn, realUser=, issueDate=1508493705613, maxDate=1509098505613, sequenceNumber=2, masterKeyId=2)
17/10/20 06:01:46 INFO impl.YarnClientImpl: Submitted application application_1508493348273_0002
17/10/20 06:01:46 INFO mapreduce.Job: The url to track the job: http://bedg1-cdh.hadoop:8088/proxy/application_1508493348273_0002/
17/10/20 06:01:46 INFO mapreduce.Job: Running job: job_1508493348273_0002
17/10/20 06:01:53 INFO mapreduce.Job: Job job_1508493348273_0002 running in uber mode : false
17/10/20 06:01:53 INFO mapreduce.Job:  map 0% reduce 0%
17/10/20 06:01:58 INFO mapreduce.Job:  map 100% reduce 0%
17/10/20 06:02:04 INFO mapreduce.Job:  map 100% reduce 100%
17/10/20 06:02:05 INFO mapreduce.Job: Job job_1508493348273_0002 completed successfully
17/10/20 06:02:05 INFO mapreduce.Job: Counters: 49
        File System Counters
                FILE: Number of bytes read=37
                FILE: Number of bytes written=249063
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=274
                HDFS: Number of bytes written=215
                HDFS: Number of read operations=7
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=3
        Job Counters
                Launched map tasks=1
                Launched reduce tasks=1
                Data-local map tasks=1
                Total time spent by all maps in occupied slots (ms)=2424
                Total time spent by all reduces in occupied slots (ms)=4391
                Total time spent by all map tasks (ms)=2424
                Total time spent by all reduce tasks (ms)=4391
                Total vcore-seconds taken by all map tasks=2424
                Total vcore-seconds taken by all reduce tasks=4391
                Total megabyte-seconds taken by all map tasks=2482176
                Total megabyte-seconds taken by all reduce tasks=4496384
        Map-Reduce Framework
                Map input records=1
                Map output records=2
                Map output bytes=18
                Map output materialized bytes=33
                Input split bytes=156
                Combine input records=0
                Combine output records=0
                Reduce input groups=2
                Reduce shuffle bytes=33
                Reduce input records=2
                Reduce output records=0
                Spilled Records=4
                Shuffled Maps =1
                Failed Shuffles=0
                Merged Map outputs=1
                GC time elapsed (ms)=117
                CPU time spent (ms)=2060
                Physical memory (bytes) snapshot=647708672
                Virtual memory (bytes) snapshot=5583294464
                Total committed heap usage (bytes)=624427008
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters
                Bytes Read=118
        File Output Format Counters
                Bytes Written=97
Job Finished in 20.435 seconds
Estimated value of Pi is 4.00000000000000000000
```
