---
layout:     post
title:      Hadoop-introduction
subtitle:   First chapter of Hadoop
date:       2024-02-15
author:     Noob24
header-img: img/hadoop.jpg
catalog: true
tags:
    - Hadoop
    - Big data
---

# Hadoop
## Catalog

- [Overview of Hadoop](#section-1)
- [HDFS, Yarn and MapReduce](#section-2)

## 1. Overview of Hadoop
<a name="section-1"></a>

### 1.1 What is Hadoop?
<font face=consolas>Hadoop is a distributed system structure developed by the Apache Foundation. It mainly solves the problems of massive data storage and massive data analysis & calculation. More generally, Hadoop indicates the Hadoop ecosystem. </font>


### 1.2 Apache Hadoop
<font face=consolas>Hadoop has three distribution versions: Apache, Cloudera, Hortonworks. Apache version is comfortable for rookie(like me) because it is the most basic version. The official website of Apache Hadoop is: [http://hadoop.apache.org/](http://hadoop.apache.org/). </font>

### 1.3 Architecture of Hadoop
- <font face=consolas>Hadoop 1.x version: It contains Common, HDFS and MapReduce. MapReduce handles both logic operations and resource scheduling, with high coupling. </font>
- <font face=consolas>Hadoop 2.x version: It contains Common, HDFS Yarn and MapReduce. Compared to version 1.x, Yarn is responsible for resource scheduling and MapReduce is responsible for computation. </font>
- <font face=consolas>Hadoop 3.x version: Its architecture is same with 2.x version. </font>

![Hadoop versions](https://github.com/CChenTaiyu/CChenTaiyu.github.io/blob/main/img/store/article/hadoop1.jpg?raw=true)

## 2. HDFS, Yarn and MapReduce
<a name="section-2"></a>

### 2.1 HDFS Architecture
<font face=consolas>The full name of HDFS is Hadoop File Distributed System, it contains three main components.</font>

- **NameNode(nn)**: <font face=consolas>Store metadata for files, such as file name, structure of directory, file attributes(generation times, number of copies, permission), as well as the list of blocks for each file and the DataNode where the blocks are located.</font>

- **DataNode(dn)**: <font face=consolas>Store file block data and checksum of block data in the local file system.</font>

- **Secondary NameNode(2nn)**: <font face=consolas>Backup NameNode metadata periodically.</font>

![HDFS Architecture](https://github.com/CChenTaiyu/CChenTaiyu.github.io/blob/main/img/store/article/hadoop2.jpg?raw=true)

### 2.2 Yarn Architecture
<font face=consolas>The full name of Yarn is Yet Another Resource Negotiator, It is a resource manager for Hadoop.

- **ResourceManager(RM)**: The boss of the entire cluster resources(memory, CPU).

- **NodeManager(NM)**: The boss of single node server resources

- **ApplicationMaster(AM)**: The boss of a single running task.

- **Container**: Equivalent to an independent server, encapsulating the resources required for task running.

![Yarn Architecture](https://github.com/CChenTaiyu/CChenTaiyu.github.io/blob/main/img/store/article/hadoop3.jpg?raw=true)
</font>

### 2.2 MapReduce Architecture
<font face=consolas>MapReduce divides the calculation process into two stages: Map and Reduce.

- **Map**: The Map stage processes input data in parallel.

- **Reduce**: Reduce stage summarizes Map results.

![MapReduce Architecture](https://github.com/CChenTaiyu/CChenTaiyu.github.io/blob/main/img/store/article/hadoop4.jpg?raw=true)
</font>


