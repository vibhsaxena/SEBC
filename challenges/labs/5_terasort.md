

///
hadoop jar /opt/cloudera/parcels/CDH-5.7.3-1.cdh5.7.3.p0.5/jars/hadoop-examples.jar terasort /user/christie/tgen64 /user/christie/tgen64

16/09/23 12:12:45 INFO mapreduce.Job: Job job_1474646687539_0002 completed successfully
16/09/23 12:12:45 INFO mapreduce.Job: Counters: 49
        File System Counters
                FILE: Number of bytes read=22182399
                FILE: Number of bytes written=45582242
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=51200280
                HDFS: Number of bytes written=51200000
                HDFS: Number of read operations=30
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=16
        Job Counters
                Launched map tasks=2
                Launched reduce tasks=8
                Data-local map tasks=2
                Total time spent by all maps in occupied slots (ms)=10814
                Total time spent by all reduces in occupied slots (ms)=66176
                Total time spent by all map tasks (ms)=10814
                Total time spent by all reduce tasks (ms)=66176
                Total vcore-seconds taken by all map tasks=10814
                Total vcore-seconds taken by all reduce tasks=66176
                Total megabyte-seconds taken by all map tasks=11073536
                Total megabyte-seconds taken by all reduce tasks=67764224
        Map-Reduce Framework
                Map input records=512000
                Map output records=512000
                Map output bytes=52224000
                Map output materialized bytes=22186131
                Input split bytes=280
                Combine input records=0
                Combine output records=0
                Reduce input groups=512000
                Reduce shuffle bytes=22186131
                Reduce input records=512000
                Reduce output records=512000
                Spilled Records=1024000
                Shuffled Maps =16
                Failed Shuffles=0
                Merged Map outputs=16
                GC time elapsed (ms)=500
                CPU time spent (ms)=30590
                Physical memory (bytes) snapshot=2653765632
                Virtual memory (bytes) snapshot=15883591680
                Total committed heap usage (bytes)=3435659264
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters
                Bytes Read=51200000
        File Output Format Counters
                Bytes Written=51200000

///

