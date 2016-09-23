
* # show grants

///
mysql> show grants for rman;

+-----------------------------------------------------------------------------------------------------+
| Grants for rman@%                                                                                   |
+-----------------------------------------------------------------------------------------------------+
| GRANT USAGE ON *.* TO 'rman'@'%' IDENTIFIED BY PASSWORD '*AEF345BFE495D8E678EA9D3D5708FD110AD2F08E' |
| GRANT ALL PRIVILEGES ON `rman`.* TO 'rman'@'%'                                                      |
+-----------------------------------------------------------------------------------------------------+
2 rows in set (0.00 sec)

mysql> show grants for oozie;

+------------------------------------------------------------------------------------------------------+
| Grants for oozie@%                                                                                   |
+------------------------------------------------------------------------------------------------------+
| GRANT USAGE ON *.* TO 'oozie'@'%' IDENTIFIED BY PASSWORD '*81A1BB46F79EBD0AA76E6EFAA31D62458CFCAF62' |
| GRANT ALL PRIVILEGES ON `oozie`.* TO 'oozie'@'%'                                                     |
+------------------------------------------------------------------------------------------------------+
2 rows in set (0.00 sec)

mysql> show grants for hive;

+-----------------------------------------------------------------------------------------------------+
| Grants for hive@%                                                                                   |
+-----------------------------------------------------------------------------------------------------+
| GRANT USAGE ON *.* TO 'hive'@'%' IDENTIFIED BY PASSWORD '*8AC2E431CC7A9F2C4C0E51A65B8D8175892D9F22' |
| GRANT ALL PRIVILEGES ON `hive`.* TO 'hive'@'%'                                                      |
+-----------------------------------------------------------------------------------------------------+
2 rows in set (0.00 sec)
///

* # output for hdfs dfs -ls /user

[ec2-user@ip-172-31-23-200 ~]$ sudo -u hdfs hdfs dfs -ls /user

///
Found 6 items
drwxr-xr-x   - christie supergroup          0 2016-09-23 10:30 /user/christie
drwxrwxrwx   - mapred   hadoop              0 2016-09-23 10:27 /user/history
drwxrwxr-t   - hive     hive                0 2016-09-23 10:27 /user/hive
drwxrwxr-x   - hue      hue                 0 2016-09-23 10:28 /user/hue
drwxrwxr-x   - oozie    oozie               0 2016-09-23 10:28 /user/oozie
drwxr-xr-x   - weiner   supergroup          0 2016-09-23 10:30 /user/weiner
///
 

* # output for hadoop classpath

///

[ec2-user@ip-172-31-23-199 ~]$ sudo -u hdfs hadoop classpath
/etc/hadoop/conf:/opt/cloudera/parcels/CDH-5.7.3-1.cdh5.7.3.p0.5/lib/hadoop/libexec/../../hadoop/lib/*:/opt/cloudera/parcels/CDH-5.7.3-1.cdh5.7.3.p0.5/lib/hadoop/libexec/../../hadoop/.//*:/opt/cloudera/parcels/CDH-5.7.3-1.cdh5.7.3.p0.5/lib/hadoop/libexec/../../hadoop-hdfs/./:/opt/cloudera/parcels/CDH-5.7.3-1.cdh5.7.3.p0.5/lib/hadoop/libexec/../../hadoop-hdfs/lib/*:/opt/cloudera/parcels/CDH-5.7.3-1.cdh5.7.3.p0.5/lib/hadoop/libexec/../../hadoop-hdfs/.//*:/opt/cloudera/parcels/CDH-5.7.3-1.cdh5.7.3.p0.5/lib/hadoop/libexec/../../hadoop-yarn/lib/*:/opt/cloudera/parcels/CDH-5.7.3-1.cdh5.7.3.p0.5/lib/hadoop/libexec/../../hadoop-yarn/.//*:/opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/lib/*:/opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/.//*

///


* # first item output from the CM API call

///

"items" : [ {
    "hostId" : "i-0cc1a2f760ec7fff3",
    "ipAddress" : "172.31.23.198",
    "hostname" : "ip-172-31-23-198.ec2.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-23-200.ec2.internal:7180/cmf/hostRedirect/i-0cc1a2f760ec7fff3",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 15332438016
  }
  
  ///