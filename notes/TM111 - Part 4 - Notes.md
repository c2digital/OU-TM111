---
title: TM111 - Part 4 - Notes
created: '2024-09-12T07:51:26.512Z'
modified: '2024-09-15T16:13:24.733Z'
---

# TM111 - Part 4 - Notes

** =** 
**Attribute =** properties describing an entity
**Big Data =** a data handling technology for extracting useful information from huge pool sof ill-defined data
**Cluster =** a group of computing nodes. The nodes are normally of the same type of computer and on the same network. Each node has its own RAM.
**Data =** One or more values that can be assigned to an object. It can assume any form (numbers, letters, pictures etc) but has no context. "100meters" is data but means nothing without the context.
**Database =** A collection of related data stored in an organised manner for efficent reading and updating
**Distributed Computing =** where data processing is distributed across nodes (such as clusters or grid etc) with each node working on a small part of the task
**Entity =** an item about which we want to store data. Can be tangible (a person, building etc) or intagible (an event, study objective). Described using attributes.
**Grid Computing =** similar to a cluster except mude of a different types of computers all working on the same task. Often distributed across the internet instead of being on the same network
**Instance =** an instance of an entity. Whereas an entity could be 'student', the instance would be the object 'Carl Mason' of the student type.
**Parallel Processing=** a type of distrbuted computing where a task is distributed across nodes that share memory (as oppose to a cluster where each node as it's own memory)
**Query Language =** combines limited set of english phrases with logical commands. SQL is the most propular.
**Node =** a single computing instance within a cluster
**Normalisation =** dividing data in a database into two or more tables with relationships
**Sampling (data) =** 
**Structured Data =** data in which individual pieces have a defined attribute that can be known in advanced - such as an address (street, city, postcode etc)
**Unstructured Data =** data that has not yet been structured or is unsuitable for structuring like images, sensor data, social media content
**Velocity (data) =** how fast the data is being acquired
**Veracity (data) =** how trustworthy or correct the data is
**Volume (data) =** the amouont of data acquired (GB etc)



## Notes
- Data on its own has no context. Data is turned into useful information by placing it within context.
- Computer programs process data following instructions.
- When we want to store large amounts of data, we use a database

### Flat Databases
- Simpliest of all, also known as just a table
- Column = field. Row = record.
- Interact with the database using queries
- Becomes cumberson when adding new fields and updated selected rows, as well as requiring duplicating data. 

### Relational Databases
- Overcomes the problems of flat databases
- Divides data into two or more tables (known as normalisation). The benefits of normalisation includes:-
  - It is not necessary to have empty fields as with the flat table as many relations can be created in a joining table
  - If a change is required, it only has to be made in one table/row, rather than duplicating across many rows
  - No more unneccesary repetition
- Uses entities and instances of entities
- Entities have attributes (such as date of birth). Instances have values of intributes (such as 7th April 1989).
- Relationships are stored in 'joining tables' Such as a student_id to a course_id.
- Joining tables are for the convenience of the computer, not that user friendly to humans
- Relationships can be one-to-many, many-to-many and many-to-one

### Views

- Databases permit 'views' - which uses a query to combine data from one or more tables to create virtual tables, which can be queried itself
- Views are useful for:-
  - Showing table from multiple tables together
  - Limiting access to data (eg. retrieve a users basic profile without contact details)
  - Combining data from tables based on criteria
  - Can be assigned as 'readonly' to prevent unwanted access/changes
- On the downside:-
  - Depend on the arrangement of the underlying tables. If the table structures are changed, the views need updating too
  - Data access is slightly slower

### Database Management Systems (DBMS)

- MSSQL, IBM DB2, MySQL etc

### Big Data
- Estimated that humanity had created 5 exabytes (1b Gigabytes) of data in total in 2003.
- Curently estimated that humanity is now generating 5 exabytes every 2 days
- Data processing is traditionally complicated and time consuming. So much so that it was only possible to examine a subset of the available data. This is known as a sample (sampling). Political opinion polls are one example of this. Relied on the sample being indicative of the whole.
- Creating representivie sample groups is difficult. Samples can have hidden biasis, people can lie and accidently omissions will lead to incorrect results.
- Thanks to modern computers it is now possible to use extremly large samples or process all data. This allows us to find connections that a smaller sample would not have found.
- Fraud analysis is one example of where big data is useful to find patterns of unusual activity that need investigating.
- Big data is often defined by the "Three V's":-
  - Volume: large amount of data to be processed
  - Velocity: relentless demand for the data to be acquired and processed
  - Variety: the data being acquired can take any form - not just numeric or text.
  - The possibility that some data might be inaccurate requires big data applications to perform checks for misleading values. This has led to the creation of a forth 'V': veracity. "Ensuring the correctness and trustworthiness of the data"
- Often uses unstructured data. This can be machine-acquired data such as aerial photography & sensor data or human-generated content such as business documents, social media content etc
- In the last few years, the demand for unstructured data has outstripped the demand for structured data
- Structured vs unstructured refers to the content not how the data is stored

### Data Volume vs Data Quality
- Analytics results are only as good as the original data
- Sampling can be used to improve the quality of the data at the expense of volume (by selecting the best data instead of random)
- Researchers will often exclude extreme values as they are likely to be errors or contamination and do not represent the whole

## Processing Big Data

- Big data requires alot of computing power. This is often not just one big computer but more often a collection of modestly powered computers. These are called nodes and are grouped into clusters.
- Nodes are connected using very high speed networks and overseen through a central "master" computer which allocates tasks to a node.
- Nodes are often connected to an array of disk storage drives rather than having their own nodes
- The disk storage is often also connected to the central computer
- Nodes can be added to a cluster or old nodes replaced with more power versions as required
- Clusters are resilient to failure of one or more nodes as the tasks are allocated across the various nodes (ie. if one fails, the task to redirected to another node)

### MapReduce
- Big Data software created by Google for using clusters
- Composed of three components
  - Map: a procedure that performs a task, such as sorting data
  - Reduce: a procedure that summarises the output of the mapping
  - Framework: divides the data sending chunks to each node. Manages fault detection and comms.
- Formally used for the PageRank system.
- More than one copy of data blocks were processed to prevent data corruption or data loss if a node failed mid-task
- Since replaced but now lives on as Apache Hadoop as used by AWS S3, Azure and others.
