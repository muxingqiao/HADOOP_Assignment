1.思考Hive数据仓库在Hadoop中起到的作用是什么？
   hive是基于Hadoop构建的一套数据仓库分析系统，它提供了丰富的SQL查询方式来分析存储在Hadoop分布式文件系统中的数据：可以将结构化的数据文件映射为一张数据库表，并提供完整的SQL查询功能；可以将SQL语句转换为MapReduce任务运行，通过自己的SQL查询分析需要的内容，这套SQL简称Hive SQL，使不熟悉mapreduce的用户可以很方便地利用SQL语言查询、汇总和分析数据。而mapreduce开发人员可以把自己写的mapper和reducer作为插件来支持hive做更复杂的数据分析。它与关系型数据库的SQL略有不同，但支持了绝大多数的语句如DDL、DML以及常见的聚合函数、连接查询、条件查询。它还提供了一系列的进行数据提取转化加载，用来存储、查询和分析存储在Hadoop中的大规模数据集，并支持UDF（User-Defined Function）、UDAF(User-Defnes AggregateFunction)和USTF（User-Defined Table-Generating Function），也可以实现对map和reduce函数的定制，为数据操作提供了良好的伸缩性和可扩展性。
2.简述Hive清洗数据清洗的特点。
数据清洗：按照进行数据清洗，并将清洗后的数据导入hive数据库中。
1.	将.csv文件导入hive数据库。
（1）把.csv文件上传到HDFS中
（2）在hive中建立对应的table
（3）将数据导入hive仓库
2.将hive数据库中的数据表进行查询操作，然后把清洗后的结果存入新建的hive表。
（1）建立新样表
（2）将清洗后的数据导入
（3）查看导入成功后的结果
3.Hive元数据库是用来做什么的，主要存储什么信息？
元数据：本质上只是用来存储hive中有哪些数据库，哪些表，表的模式，目录，分区，索引以及命名空间。为数据库创建的目录一般在hive数据仓库目录下。Hive 的元数据信息通常存储在关系型数据库中，常用MySQL数据库作为元数据库管理。
