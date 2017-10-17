**1. Create a precious directory in HDFS; copy the ZIP course file into it.**
[g0dj4ck4l@aedg1-cdh58 ~]$ hdfs dfs -mkdir /user/g0dj4ck4l/precious
[g0dj4ck4l@aedg1-cdh58 ~]$ hdfs dfs -put SEBC-master.zip /user/g0dj4ck4l/precious

**2. Enable snapshots for precious**
[hdfs@aedg1-cdh58 ~]$ hdfs dfsadmin -allowSnapshot /user/g0dj4ck4l/precious
Allowing snaphot on /user/g0dj4ck4l/precious succeeded

**3. Create a snapshot called sebc-hdfs-test**
[g0dj4ck4l@aedg1-cdh58 ~]$ hdfs dfs -createSnapshot /user/g0dj4ck4l/precious sebc-hdfs-test
Created snapshot /user/g0dj4ck4l/precious/.snapshot/sebc-hdfs-test

**4. Delete the directory**
[g0dj4ck4l@aedg1-cdh58 ~]$ hdfs dfs -rm -r /user/g0dj4ck4l/precious/
rm: Failed to move to trash: hdfs://amst1-cdh58.hadoop:8020/user/g0dj4ck4l/precious: The directory /user/g0dj4ck4l/precious cannot be deleted since /user/g0dj4ck4l/precious is snapshottable and already has snapshots

**5. Delete the ZIP file**
[g0dj4ck4l@aedg1-cdh58 ~]$ hdfs dfs -rm -r /user/g0dj4ck4l/precious/SEBC-master.zip
17/10/17 10:05:56 INFO fs.TrashPolicyDefault: Moved: 'hdfs://amst1-cdh58.hadoop:8020/user/g0dj4ck4l/precious/SEBC-master.zip' to trash at: hdfs://amst1-cdh58.hadoop:8020/user/g0dj4ck4l/.Trash/Current/user/g0dj4ck4l/precious/SEBC-master.zip

**6. Restore the deleted file**
[g0dj4ck4l@aedg1-cdh58 ~]$ hdfs dfs -cp -ptopax /user/g0dj4ck4l/precious/.snapshot/sebc-hdfs-test/SEBC-master.zip /user/g0dj4ck4l/precious/
