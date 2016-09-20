# Configuration Checks


**1. vm.swappiness**

///
[ec2-user@CDH5Master ~]$  cat /proc/sys/vm/swappiness

1
///


**2. check if noatime is set for non-root**

It's not:  
[ec2-user@CDH5Master ~]$ cat /proc/mounts | grep noatime
/dev/xvda1 / ext4 rw,noatime,data=ordered 0 0


**3. check if reserve space for any non-root volumes is not zero**

///
sudo /sbin/tune2fs -l /dev/sdb | grep reserve

Reserved blocks uid:      0 (user root)

Reserved blocks gid:      0 (group root)

///
*This implies blocks aren't reserverd for anything other than root* 



**4. Check the user limits for maximum file descriptors and processes**

[ec2-user@CDH5Master ~]$ ulimit -a | grep processes
max user processes              (-u) 60086

file desc:
[ec2-user@CDH5Master ~]$ ulimit -n
1024



**5. Test forward and reverse host lookups for correct resolution**

///

[ec2-user@CDH5Master ~]$ host ec2-52-4-184-142.compute-1.amazonaws.com.
ec2-52-4-184-142.compute-1.amazonaws.com has address 172.31.58.249
[ec2-user@CDH5Master ~]$ host 172.31.58.249
249.58.31.172.in-addr.arpa domain name pointer ip-172-31-58-249.ec2.internal.
///

**6. Verify/enable the nscd service**

*nscd service wasn't installed, installed and started*

///
[ec2-user@CDH5Master ~]$ service nscd status
nscd (pid 3137) is running...
///

**7. Verify/enable the ntpd service**

///
[ec2-user@CDH5Master ~]$ service ntpd status
ntpd (pid  2551) is running...
///


