# HBase

How to run

Follow Commands.txt to run on terminal. Java codes will run on eclipse directly after referencing HBase libraries.

Stop HBase

Stop the service when required using below command

$HBASE_HOME/bin/stop-hbase.sh

Common error fix:

Error 1: ERROR [main] zookeeper.RecoverableZooKeeper: ZooKeeper exists failed after 4 attempts
org.apache.zookeeper.KeeperException$ConnectionLossException: KeeperErrorCode = ConnectionLoss for /hbase/hbaseid
Explanation and Fix: If you run "jps" in terminal you will not find any "HMaster" service running. To fix this run below command

$HBASE_HOME/bin/start-hbase.sh

You can use the below command to check if HMaster is running.

jps

Error 2: Exception in thread "main" org.apache.hadoop.hbase.client.RetriesExhaustedException: Cannot get the location for replica0 of region for Twitter,, in hbase:meta
Explanation and Fix: You will get this error in eclipse if you run HBase on eclipse when HMaster is not running.

Go to terminal and run command:

$HBASE_HOME/bin/start-hbase.sh
