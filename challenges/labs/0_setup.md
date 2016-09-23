# Challenges Setup

*AWS Region-
N.Virginia

*AMI - RHEL - 7.2

*Public IP for MySQL Server - 54.88.233.170

*Output for /usr/java- 

[ec2-user@ip-172-31-23-199 ~]$ sudo ls /usr/java
ls: cannot access /usr/java: No such file or directory


*[ec2-user@ip-172-31-23-199 ~]$ sudo cat /etc/passwd | grep christie
christie:x:2500:2500::/home/christie:/bin/bash

[ec2-user@ip-172-31-23-199 ~]$ sudo cat /etc/passwd | grep weiner
weiner:x:2501:2501::/home/weiner:/bin/bash

*[ec2-user@ip-172-31-23-199 ~]$ sudo cat /etc/group | grep pictures
pictures:x:2502:weiner

[ec2-user@ip-172-31-23-199 ~]$ sudo cat /etc/group | grep bridges
bridges:x:2503:christie

