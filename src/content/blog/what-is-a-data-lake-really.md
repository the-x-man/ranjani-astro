---
slug: what-is-a-data-lake-really
publishDate: 2020-07-14T16:52:36Z
author: Ranjani Mani
title: What is a Data lake, really? 
excerpt: “A data lake is usually a single store of all enterprise data including raw copies of source system data and transformed data used for tasks such as reporting, visualization, advanced analytics and machine learning”, says the Wiki definition. 1\] What is a Data lake It is essentially a Storage Repository Holds large amount of data Stores it in its ‘native format’ until it  ... 
category: 13
---

“A **data lake** is usually a single store of all enterprise **data** including raw copies of source system **data** and transformed **data** used for tasks such as reporting, visualization, advanced analytics and machine learning”, says the Wiki definition.

![](https://i0.wp.com/ranjanimani.com/wp-content/uploads/2020/07/Datalake.png?resize=321%2C323&ssl=1)

Image source – AWS

**1\] What is a Data lake**

* It is essentially a Storage Repository
* Holds large amount of data
* Stores it in its ‘native format’ until it is needed
* The data can thus be in a structured, semi-structured and unstructured data. The structure is not defined until the data is required.

**2\] How is it different from a data warehouse?**

* While an hierarchical data warehouse holds it as data or files or folders, a data lake uses a flat structureÂ to store data.
* It is a low cost storage solution whilst being highly agile with configuration/re-configuration capabilities are required.

**3\] How is it stored?**

* Each element in a data lake is assigned an unique identifier and tagged with a set of metadata tags.
* When a requirement arises, the datalake can be queried for the specific data which can then be analyzed to help answer the question

The term data lake is usually associated with Hadoop – object oriented storage. In such a scenario, an organization’s data is first loaded into the hadoop platform and then the data mining tools are applied onto the data that resides in the Hadoop Clusters

\[**Side note on Hadoop**\]

Hadoop is an open source, Java-based programming framework that supports the processing and storage of extremely large data sets in distributed computing environment. It is part of the Apache project sponsored by the Apache software foundation. Hadoop allows one to run applications on systems with thousands of community nodes and handles thousands of terabytes of data. Its distributed file system facilitates rapid data transfer rates among nodes and allows the system to continue operating in the case of node failure\]

James Dixon, the founder and CTO of Pentaho, has been credited with coming up with the term. This is how he describes a data lake:

> _If you think of a datamart as a store of bottled water “ cleansed and packaged and structured for easy consumption”, the data lake is a large body of water in a more natural state. The contents of the data lake stream in from a source to fill the lake, and various users of the lake can come to examine, dive in, or take samples._

![](https://i0.wp.com/ranjanimani.com/wp-content/uploads/2020/07/BlogimageDataWarehouse-1.png?resize=847%2C512&ssl=1)

Source – <https://www.grazitti.com/>