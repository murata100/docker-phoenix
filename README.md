docker-phoenix
==============

A Docker image to quick start [Apache Phoenix](http://phoenix.apache.org/) on [Apache HBase](https://hbase.apache.org/)
to provide an SQL interface.

Apache Phoenix is a SQL skin over HBase delivered as a client-embedded JDBC driver targeting low latency queries over HBase data. Apache Phoenix takes your SQL query, compiles it into a series of HBase scans, and orchestrates the running of those scans to produce regular JDBC result sets. The table metadata is stored in an HBase table and versioned, such that snapshot queries over prior versions will automatically use the correct schema. Direct use of the HBase API, along with coprocessors and custom filters, results in performance on the order of milliseconds for small queries, or seconds for tens of millions of rows.

### Versions
* Apache Hadoop - 2.7.0  
* Apache HBase - 1.2.6
* Apache Phoenix - 4.10.0

### Launch
`docker run -it -p 8765:8765 david4096/docker-phoenix` will let you view the logs of the queryserver.

Launch into `docker run -it david4096/docker-phoenix /etc/bootstrap-phoenix.sh -bash`  in order to run ETL scripts within the docker container.

Launch a daemon using `docker run -itd -p 8765:8765 david4096/docker-phoenix`
