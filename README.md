my-hadoop-study
===============

connect hive's metadata
/usr/java6/bin/java -cp derbytools-10.4.2.0.jar:derby-10.4.2.0.jar -Dij.connection.myconnection=jdbc:derby:../metastore_db org.apache.derby.tools.ij 

connect 'jdbc:derby:../metastore_db';

set fs.default.name;
set hadoop.bin.path;
set mapred.job.tracker;
set hive.exec.scratchdir;
set hive.metastore.warehouse.dir;

set hive.exec.reducers.bytes.per.reducer;
set hive.exec.reducers.max;

set mapred.reduce.tasks;
set hive.exec.parallel;
set hive.exec.parallel.thread.number;