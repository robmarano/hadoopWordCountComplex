hadoopWordCountComplex
======================

A simple project template to begin hacking Hadoop MapReduce with Maven

To build:
$> mvn compile

To package:
$> mvn package

To run, assuming you have Cloudera Hadoop CDH4 installed:
$> hadoop fs -copyFromLocal ./src/test/resources/patterns.txt /user/${USER}/
$> hadoop fs -rm -r /user/${USER}/output/
$> hadoop jar ./target/WordCount2-1.0-SNAPSHOT.jar com.thehackerati.hadoop.WordCount /user/${USER}/input /user/${USER}/output

or

$> hadoop jar ./target/WordCount2-1.0-SNAPSHOT.jar com.thehackerati.hadoop.WordCount /user/${USER}/input /user/${USER}/output -skip patterns.txt

and not difference between the two outputs.

