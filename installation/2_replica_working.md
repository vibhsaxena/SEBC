# Replica Working



Set root password? [Y/n] Y
New password:
Re-enter new password:
Password updated successfully!
Reloading privilege tables..
 ... Success!


Remove anonymous users? [Y/n] Y
 ... Success!


Disallow root login remotely? [Y/n] n
 ... skipping.

Remove test database and access to it? [Y/n] Y
 - Dropping test database...
 ... Success!
 - Removing privileges on test database...
 ... Success!

Reloading the privilege tables will ensure that all changes made so far
will take effect immediately.

Reload privilege tables now? [Y/n] Y
 ... Success!

Cleaning up...



All done!  If you've completed all of the above steps, your MySQL
installation should now be secure.



5.
[ec2-user@CDH5Master ~]$ mysql -u localhost -p

mysql> GRANT REPLICATION SLAVE ON *.* TO 'root'@'CDH5Data1.compute-1.amazonaws.com' IDENTIFIED BY 'Password.1';
Query OK, 0 rows affected (0.00 sec)

mysql> SET GLOBAL binlog_format = 'ROW';
Query OK, 0 rows affected (0.00 sec)

mysql> FLUSH TABLES WITH READ LOCK;
Query OK, 0 rows affected (0.00 sec)


6. 
mysql> SHOW MASTER STATUS;

+------------------+----------+--------------+------------------+
| File             | Position | Binlog_Do_DB | Binlog_Ignore_DB |
+------------------+----------+--------------+------------------+
| mysql-bin.000001 |     1239 |              |                  |
+------------------+----------+--------------+------------------+
1 row in set (0.00 sec)

7.
mysql> CHANGE MASTER TO MASTER_HOST = 'CDH5Master.compute-1.amazonaws.com', MASTER_USER='root', MASTER_PASSWORD='Password.1', MASTER_LOG_FILE='mysql-bin.000001',MASTER_LOG_POS=1239;
Query OK, 0 rows affected (0.02 sec)

8.

mysql> START SLAVE;
Query OK, 0 rows affected (0.00 sec)


mysql> 

SHOW SLAVE STATUS \G


*************************** 1. row ***************************

               Slave_IO_State: Waiting for master to send event
