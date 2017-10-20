```
[ernest@bedg1-cdh ~]$ hadoop jar /opt/cloudera/parcels/CDH/jars/hadoop-examples.jar terasort /user/ernest/tgen512m /user/ernest/tgen512m_sort

17/10/20 05:57:33 INFO terasort.TeraSort: starting
17/10/20 05:57:35 INFO hdfs.DFSClient: Created token for ernest: HDFS_DELEGATION_TOKEN owner=ernest@G0DJ4CK4L.CO.UK, renewer=yarn, realUser=, issueDate=1508493454954, maxDate=1509098254954, sequenceNumber=1, masterKeyId=2 on 172.31.27.173:8020
17/10/20 05:57:35 INFO security.TokenCache: Got dt for hdfs://bedg1-cdh.hadoop:8020; Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.27.173:8020, Ident: (token for ernest: HDFS_DELEGATION_TOKEN owner=ernest@G0DJ4CK4L.CO.UK, renewer=yarn, realUser=, issueDate=1508493454954, maxDate=1509098254954, sequenceNumber=1, masterKeyId=2)
17/10/20 05:57:35 INFO input.FileInputFormat: Total input paths to process : 1
Spent 363ms computing base-splits.
Spent 4ms computing TeraScheduler splits.
Computing input splits took 368ms
Sampling 10 splits of 153
Making 6 from 100000 sampled records
Computing parititions took 932ms
Spent 1302ms computing partitions.
17/10/20 05:57:36 INFO client.RMProxy: Connecting to ResourceManager at bedg1-cdh.hadoop/172.31.27.173:8032
17/10/20 05:57:36 INFO mapreduce.JobSubmitter: number of splits:153
17/10/20 05:57:36 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1508493348273_0001
17/10/20 05:57:36 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.27.173:8020, Ident: (token for ernest: HDFS_DELEGATION_TOKEN owner=ernest@G0DJ4CK4L.CO.UK, renewer=yarn, realUser=, issueDate=1508493454954, maxDate=1509098254954, sequenceNumber=1, masterKeyId=2)
17/10/20 05:57:37 INFO impl.YarnClientImpl: Submitted application application_1508493348273_0001
17/10/20 05:57:37 INFO mapreduce.Job: The url to track the job: http://bedg1-cdh.hadoop:8088/proxy/application_1508493348273_0001/
17/10/20 05:57:37 INFO mapreduce.Job: Running job: job_1508493348273_0001
17/10/20 05:57:45 INFO mapreduce.Job: Job job_1508493348273_0001 running in uber mode : false
17/10/20 05:57:45 INFO mapreduce.Job:  map 0% reduce 0%
17/10/20 05:57:57 INFO mapreduce.Job:  map 1% reduce 0%
17/10/20 05:57:58 INFO mapreduce.Job:  map 2% reduce 0%
17/10/20 05:58:04 INFO mapreduce.Job:  map 3% reduce 0%
17/10/20 05:58:05 INFO mapreduce.Job:  map 8% reduce 0%
17/10/20 05:58:07 INFO mapreduce.Job:  map 9% reduce 0%
17/10/20 05:58:13 INFO mapreduce.Job:  map 10% reduce 0%
17/10/20 05:58:15 INFO mapreduce.Job:  map 11% reduce 0%
17/10/20 05:58:16 INFO mapreduce.Job:  map 12% reduce 0%
17/10/20 05:58:17 INFO mapreduce.Job:  map 16% reduce 0%
17/10/20 05:58:21 INFO mapreduce.Job:  map 17% reduce 0%
17/10/20 05:58:23 INFO mapreduce.Job:  map 18% reduce 0%
17/10/20 05:58:28 INFO mapreduce.Job:  map 21% reduce 0%
17/10/20 05:58:29 INFO mapreduce.Job:  map 24% reduce 0%
17/10/20 05:58:32 INFO mapreduce.Job:  map 25% reduce 0%
17/10/20 05:58:37 INFO mapreduce.Job:  map 26% reduce 0%
17/10/20 05:58:38 INFO mapreduce.Job:  map 27% reduce 0%
17/10/20 05:58:40 INFO mapreduce.Job:  map 33% reduce 0%
17/10/20 05:58:48 INFO mapreduce.Job:  map 35% reduce 0%
17/10/20 05:58:49 INFO mapreduce.Job:  map 36% reduce 0%
17/10/20 05:58:50 INFO mapreduce.Job:  map 37% reduce 0%
17/10/20 05:58:51 INFO mapreduce.Job:  map 39% reduce 0%
17/10/20 05:58:52 INFO mapreduce.Job:  map 40% reduce 0%
17/10/20 05:58:53 INFO mapreduce.Job:  map 41% reduce 0%
17/10/20 05:58:58 INFO mapreduce.Job:  map 42% reduce 0%
17/10/20 05:58:59 INFO mapreduce.Job:  map 43% reduce 0%
17/10/20 05:59:01 INFO mapreduce.Job:  map 44% reduce 0%
17/10/20 05:59:02 INFO mapreduce.Job:  map 48% reduce 0%
17/10/20 05:59:06 INFO mapreduce.Job:  map 49% reduce 0%
17/10/20 05:59:08 INFO mapreduce.Job:  map 50% reduce 0%
17/10/20 05:59:10 INFO mapreduce.Job:  map 51% reduce 0%
17/10/20 05:59:12 INFO mapreduce.Job:  map 53% reduce 0%
17/10/20 05:59:13 INFO mapreduce.Job:  map 56% reduce 0%
17/10/20 05:59:17 INFO mapreduce.Job:  map 57% reduce 0%
17/10/20 05:59:18 INFO mapreduce.Job:  map 58% reduce 0%
17/10/20 05:59:21 INFO mapreduce.Job:  map 59% reduce 0%
17/10/20 05:59:23 INFO mapreduce.Job:  map 62% reduce 0%
17/10/20 05:59:24 INFO mapreduce.Job:  map 63% reduce 0%
17/10/20 05:59:26 INFO mapreduce.Job:  map 65% reduce 0%
17/10/20 05:59:29 INFO mapreduce.Job:  map 66% reduce 0%
17/10/20 05:59:30 INFO mapreduce.Job:  map 67% reduce 0%
17/10/20 05:59:34 INFO mapreduce.Job:  map 68% reduce 0%
17/10/20 05:59:35 INFO mapreduce.Job:  map 71% reduce 0%
17/10/20 05:59:37 INFO mapreduce.Job:  map 73% reduce 0%
17/10/20 05:59:39 INFO mapreduce.Job:  map 74% reduce 0%
17/10/20 05:59:43 INFO mapreduce.Job:  map 75% reduce 0%
17/10/20 05:59:45 INFO mapreduce.Job:  map 76% reduce 0%
17/10/20 05:59:46 INFO mapreduce.Job:  map 79% reduce 0%
17/10/20 05:59:47 INFO mapreduce.Job:  map 80% reduce 0%
17/10/20 05:59:48 INFO mapreduce.Job:  map 81% reduce 0%
17/10/20 05:59:51 INFO mapreduce.Job:  map 82% reduce 0%
17/10/20 05:59:55 INFO mapreduce.Job:  map 83% reduce 0%
17/10/20 05:59:56 INFO mapreduce.Job:  map 84% reduce 0%
17/10/20 05:59:57 INFO mapreduce.Job:  map 85% reduce 0%
17/10/20 05:59:58 INFO mapreduce.Job:  map 88% reduce 0%
17/10/20 05:59:59 INFO mapreduce.Job:  map 89% reduce 0%
17/10/20 06:00:04 INFO mapreduce.Job:  map 89% reduce 3%
17/10/20 06:00:07 INFO mapreduce.Job:  map 89% reduce 8%
17/10/20 06:00:09 INFO mapreduce.Job:  map 90% reduce 12%
17/10/20 06:00:10 INFO mapreduce.Job:  map 92% reduce 17%
17/10/20 06:00:11 INFO mapreduce.Job:  map 93% reduce 17%
17/10/20 06:00:12 INFO mapreduce.Job:  map 93% reduce 21%
17/10/20 06:00:13 INFO mapreduce.Job:  map 93% reduce 22%
17/10/20 06:00:15 INFO mapreduce.Job:  map 93% reduce 25%
17/10/20 06:00:16 INFO mapreduce.Job:  map 93% reduce 26%
17/10/20 06:00:18 INFO mapreduce.Job:  map 95% reduce 26%
17/10/20 06:00:20 INFO mapreduce.Job:  map 97% reduce 26%
17/10/20 06:00:21 INFO mapreduce.Job:  map 97% reduce 27%
17/10/20 06:00:23 INFO mapreduce.Job:  map 98% reduce 27%
17/10/20 06:00:24 INFO mapreduce.Job:  map 99% reduce 27%
17/10/20 06:00:26 INFO mapreduce.Job:  map 100% reduce 27%
17/10/20 06:00:27 INFO mapreduce.Job:  map 100% reduce 32%
17/10/20 06:00:28 INFO mapreduce.Job:  map 100% reduce 45%
17/10/20 06:00:30 INFO mapreduce.Job:  map 100% reduce 49%
17/10/20 06:00:31 INFO mapreduce.Job:  map 100% reduce 59%
17/10/20 06:00:32 INFO mapreduce.Job:  map 100% reduce 62%
17/10/20 06:00:33 INFO mapreduce.Job:  map 100% reduce 64%
17/10/20 06:00:34 INFO mapreduce.Job:  map 100% reduce 68%
17/10/20 06:00:35 INFO mapreduce.Job:  map 100% reduce 70%
17/10/20 06:00:36 INFO mapreduce.Job:  map 100% reduce 72%
17/10/20 06:00:37 INFO mapreduce.Job:  map 100% reduce 77%
17/10/20 06:00:40 INFO mapreduce.Job:  map 100% reduce 82%
17/10/20 06:00:41 INFO mapreduce.Job:  map 100% reduce 86%
17/10/20 06:00:43 INFO mapreduce.Job:  map 100% reduce 90%
17/10/20 06:00:44 INFO mapreduce.Job:  map 100% reduce 93%
17/10/20 06:00:46 INFO mapreduce.Job:  map 100% reduce 94%
17/10/20 06:00:47 INFO mapreduce.Job:  map 100% reduce 95%
17/10/20 06:00:48 INFO mapreduce.Job:  map 100% reduce 96%
17/10/20 06:00:50 INFO mapreduce.Job:  map 100% reduce 98%
17/10/20 06:00:54 INFO mapreduce.Job:  map 100% reduce 100%
17/10/20 06:00:55 INFO mapreduce.Job: Job job_1508493348273_0001 completed successfully
17/10/20 06:00:55 INFO mapreduce.Job: Counters: 49
        File System Counters
                FILE: Number of bytes read=2267830834
                FILE: Number of bytes written=4511010698
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=5120019431
                HDFS: Number of bytes written=5120000000
                HDFS: Number of read operations=477
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=12
        Job Counters
                Launched map tasks=153
                Launched reduce tasks=6
                Data-local map tasks=153
                Total time spent by all maps in occupied slots (ms)=1421346
                Total time spent by all reduces in occupied slots (ms)=264957
                Total time spent by all map tasks (ms)=1421346
                Total time spent by all reduce tasks (ms)=264957
                Total vcore-seconds taken by all map tasks=1421346
                Total vcore-seconds taken by all reduce tasks=264957
                Total megabyte-seconds taken by all map tasks=1455458304
                Total megabyte-seconds taken by all reduce tasks=271315968
        Map-Reduce Framework
                Map input records=51200000
                Map output records=51200000
                Map output bytes=5222400000
                Map output materialized bytes=2223254826
                Input split bytes=19431
                Combine input records=0
                Combine output records=0
                Reduce input groups=51200000
                Reduce shuffle bytes=2223254826
                Reduce input records=51200000
                Reduce output records=51200000
                Spilled Records=102400000
                Shuffled Maps =918
                Failed Shuffles=0
                Merged Map outputs=918
                GC time elapsed (ms)=23889
                CPU time spent (ms)=784880
                Physical memory (bytes) snapshot=76379963392
                Virtual memory (bytes) snapshot=443131961344
                Total committed heap usage (bytes)=76164890624
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters
                Bytes Read=5120000000
        File Output Format Counters
                Bytes Written=5120000000
17/10/20 06:00:55 INFO terasort.TeraSort: done

```
