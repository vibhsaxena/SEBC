mysql> START SLAVE;

Query OK, 0 rows affected (0.01 sec)

mysql> SHOW SLAVE STATUS \G

*************************** 1. row ***************************
               Slave_IO_State: Waiting for master to send event
                  Master_Host: ip-172-31-25-51.ec2.internal
                  Master_User: repl
                  Master_Port: 3306
