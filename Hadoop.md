### What is big data 
IBM data scientist break big data into 4 dimensions: 
* Volume (Scale of data), 
* Variety (Different forms of data), 
* Velocity (Analysis of streaming data), 
* Veracity (Uncertainty of data).

Traditional database management system is used to store and process relational and structured data only. 

### what is Hadoop
Hadoop is a framework to process Big Data. It is a framework that allows to store and process large data sets in parallel and distributed fashion.
Two major parts of Hadoop
* Hadoop Distributed File System (HDFS) 
  takes care of storage part of Hadoop architecture
* MapReduce
  processing modal and software framework for writing applications which can run on Hadoop. The programs are capable of processing big data in parallel on large clusters of computational nodes

#### what is HDFS
stores files across many nodes in a cluster
name node -> data node 
* name node - maintains and manages data node, records metadata, inforamtion about data blocks
* data node - stores actual data

#### what is MapReduce
* MapReduce is a programming framework that allows us to perform distributed and parallel processing on large data sets in a distributed environment
* Map & reduce
  * map tasks - splitting(input is divided into fixed-size chunks, it produces the output in (key, value) pair), mapping (each input split is passed to a mapping function which divides the split into list(key value))
  * reduce tasks - shuffling & sorting (consumes output of the mapping phase, main task is to club together the relevant record in sorting manner from the output of mapping phase, the output is <strong>Key, List(value)</strong>), reducing(output from shuffling and sorting are aggregated and returns single (key, value), the final output value is then written in the output file of HDFS)
  
 
 https://www.datasciencecentral.com/profiles/blogs/hadoop-for-beginners
 https://www.datasciencecentral.com/profiles/blogs/hadoop-for-beginners-part-2
