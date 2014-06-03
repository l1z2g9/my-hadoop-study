my-hadoop-study
===============

* Hive
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


- upgrade of protobuf-2.5.0 
git clone https://github.com/apache/hive.git
build hive-0.13 in cygwin to solve problem of upgrade of protobuf-2.5.0 in hive
mvn package -DskipTests

replace all hive-0.12-* to hive-0.13-*, protobuf-java-2.4.1.jar to protobuf-java-2.5.0.jar
add netty-3.5.11.Final.jar

- Can not create a Path from an empty string
hive-env.sh
HIVE_AUX_JARS_PATH is set with comma as delimited sign