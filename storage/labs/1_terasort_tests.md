# Teragen and Terasort benchmarks

**teragen**

time hadoop jar hadoop-examples.jar teragen -D dfs.block.size=33554432 100000000 /user/hduser/teragen-output

  - real    2m20.165s
  - user    0m6.010s
  -  sys     0m0.248s

**terasort**

sudo -u hdfs hdfs cacheadmin -addPool testPool

  sudo -u hdfs hdfs cacheadmin -addDirective -path /user/hduser/teragen-output -pool testPool


time hadoop jar hadoop-examples.jar terasort /user/hduser/teragen-output /user/hduser/terasort-output

16/09/20 19:53:31 INFO terasort.TeraSort: done
  - real    5m5.445s
  - user    0m9.153s
  -  sys     0m0.347s

*Second Run*

16/09/20 20:06:53 INFO terasort.TeraSort: done

  - real    4m55.356s
  - user    0m9.162s
  -  sys    0m0.377s
 

