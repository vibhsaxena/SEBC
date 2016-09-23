

///
[weiner@ip-172-31-23-199 ~]$ hadoop jar /opt/cloudera/parcels/CDH-5.7.3-1.cdh5.7.3.p0.5/jars/hadoop-mapreduce-examples-2.6.0-cdh5.7.3.jar pi 16 1000


      File System Counters
                FILE: Number of bytes read=124
                FILE: Number of bytes written=2051754
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=4566
                HDFS: Number of bytes written=215
                HDFS: Number of read operations=67
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=3
        Job Counters
                Launched map tasks=16
                Launched reduce tasks=1
                Data-local map tasks=16
                Total time spent by all maps in occupied slots (ms)=189237
                Total time spent by all reduces in occupied slots (ms)=3462
                Total time spent by all map tasks (ms)=189237
                Total time spent by all reduce tasks (ms)=3462
                Total vcore-seconds taken by all map tasks=189237
                Total vcore-seconds taken by all reduce tasks=3462
                Total megabyte-seconds taken by all map tasks=193778688
                Total megabyte-seconds taken by all reduce tasks=3545088
        Map-Reduce Framework
                Map input records=16
                Map output records=32
                Map output bytes=288
                Map output materialized bytes=544
                Input split bytes=2678
                Combine input records=0
                Combine output records=0
                Reduce input groups=2
                Reduce shuffle bytes=544
                Reduce input records=32
                Reduce output records=0
                Spilled Records=64
                Shuffled Maps =16
                Failed Shuffles=0
                Merged Map outputs=16
                GC time elapsed (ms)=978
                CPU time spent (ms)=10530
                Physical memory (bytes) snapshot=7670657024
                Virtual memory (bytes) snapshot=26776952832
                Total committed heap usage (bytes)=8749842432
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters
                Bytes Read=1888
        File Output Format Counters
                Bytes Written=97
Job Finished in 31.027 seconds
Estimated value of Pi is 3.14250000000000000000
