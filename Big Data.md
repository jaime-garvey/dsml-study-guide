
# Big Data


# Tools

## Spark (Data Processing)

## Hadoop (Data Storage & Processing)

### Overview 
*  platform for disributed storage and processing
* tool for maintaining,  pipeling, and cleaning data (ETL - Extract, Transform, Load)
* Use Case:
	* large amounts of data
	* 


### Major Components
1. **Hadoop Distributed File System (HDFS)** -  "used to scale a single cluster to hundreds (and even thousands) of nodes. It is a distributed file system that handles large data sets running on commodity hardware."
2. **Yet Another Resource Negotiator (YARN)**  - assigns computational resources (Components: ResourceManager, ApplicationManager, NodeManagers)
3.  **MapReduce** - framework for processing distributed data 
4.  **ZooKeeper** - tool used for coordination and synchronization of distributed systems

#### Name Nodes vs. Data Nodes
|Name Nodes					|  Data Nodes			|
|---------------------------|-----------------------|
|controls where data lives  |stores data 		    |
|process requests to add and find data on cluster|  |


#### Map Reduce
* Utilizes data clusters 
* *Map*: processes data in each node and outpus to a collection stream
* *Reduce*: Takes all outputs from Mappers and combines them into a single output



### Tool Suite
* Hive - allow SQL queries to Hadoop 
* Pig - processing library that looks like SQL
* Sqoop - load data from SQL databases to HFDS
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE3NzU5MTU4MSw4MTAwNjgwODRdfQ==
-->