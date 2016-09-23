

* mysql> grant all privileges on *.* to 'cloudera'@'54.173.162.99' with grant option;

Query OK, 0 rows affected (0.00 sec)


* [ec2-user@ip-172-31-23-200 ~]$ sudo head -1 /var/log/cloudera-scm-server/cloudera-scm-server.log

2016-09-23 09:57:17,610 INFO main:com.cloudera.server.cmf.Main: Starting SCM Server. JVM Args: [-Dlog4j.configuration=file:/etc/cloudera-scm-server/log4j.properties, -Dfile.encoding=UTF-8, -Dcmf.root.logger=INFO,LOGFILE, -Dcmf.log.dir=/var/log/cloudera-scm-server, -Dcmf.log.file=cloudera-scm-server.log, -Dcmf.jetty.threshhold=WARN, -Dcmf.schema.dir=/usr/share/cmf/schema, -Djava.awt.headless=true, -Djava.net.preferIPv4Stack=true, -Dpython.home=/usr/share/cmf/python, -XX:+UseConcMarkSweepGC, -XX:+UseParNewGC, -XX:+HeapDumpOnOutOfMemoryError, -Xmx2G, -XX:MaxPermSize=256m, -XX:+HeapDumpOnOutOfMemoryError, -XX:HeapDumpPath=/tmp, -XX:OnOutOfMemoryError=kill -9 %p], Args: [], Version: 5.8.2 (#17 built by jenkins on 20160916-1419 git: d23c620f3a3bbd85d8511d6ebba49beaaab14b75)

* [ec2-user@ip-172-31-23-200 ~]$ sudo cat /var/log/cloudera-scm-server/cloudera-scm-server.log | grep "Started Jetty server"

2016-09-23 09:58:32,861 INFO WebServerImpl:com.cloudera.server.cmf.WebServerImpl: Started Jetty server.
