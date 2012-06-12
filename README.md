gatling-sbt
===========

A sbt template project for writing [Gatling](https://github.com/excilys/gatling.git) simulations in Eclipse.

Depends on :

* gatling 1.2.1

* sbt 0.11.3

* Scala 2.9.2

To generate Eclipse project:

* sbt eclipse

To run within sbt:

* sbt run
* Choose engine 
* Data is generated in the results folder

(n.b Still need to figure out how to fork it correctly with the correct VM options)

To run standalone (with correct VM options):

* sbt compile

* export JAVA_OPTS="-XX:+UseThreadPriorities -XX:ThreadPriorityPolicy=42 -Xms512M -Xmx512M -Xmn100M -Xss1024k -XX:+HeapDumpOnOutOfMemoryError -XX:+AggressiveOpts -XX:+OptimizeStringConcat -XX:+UseFastAccessorMethods -XX:+UseParNewGC -XX:+UseConcMarkSweepGC -XX:+CMSParallelRemarkEnabled -XX:SurvivorRatio=8 -XX:MaxTenuringThreshold=1 -XX:CMSInitiatingOccupancyFraction=75 -XX:+UseCMSInitiatingOccupancyOnly"

* sbt stage

* target/start Engine


