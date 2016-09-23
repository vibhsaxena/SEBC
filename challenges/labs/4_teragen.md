

* # Teragen command

[ec2-user@ip-172-31-23-199 ~]$ sudo -u christie time hadoop jar /opt/cloudera/parcels/CDH-5.7.3-1.cdh5.7.3.p0.5/jars/hadoop-examples.jar teragen -D dfs.block.size=67108864 512000 /user/christie/tgen64

* # output of time
 
5.31user 0.20system 0:16.79elapsed 32%CPU (0avgtext+0avgdata 182848maxresident)k
0inputs+968outputs (0major+33732minor)pagefaults 0swaps

* # hdfs dfs -ls /user/christie/tgen64

[ec2-user@ip-172-31-23-199 ~]$ sudo -u hdfs hdfs dfs -ls /user/christie/tgen64

Found 3 items
-rw-r--r--   3 christie supergroup          0 2016-09-23 10:47 /user/christie/tgen64/_SUCCESS
-rw-r--r--   3 christie supergroup   25600000 2016-09-23 10:47 /user/christie/tgen64/part-m-00000
-rw-r--r--   3 christie supergroup   25600000 2016-09-23 10:47 /user/christie/tgen64/part-m-00001

* # number of blocks ~ 49?


