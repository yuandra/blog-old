---
layout: post
title: Working With Big Data
categories:
- blog, data
---

Big data is quite a buzzword these last few years with so many different definitions.

Wikipedia describes big data as such :

> Big data is a term for data sets that are so large or complex that traditional data processing application softwares are inadequate to deal with them. Challenges include capture, storage, analysis, data curation, search, sharing, transfer, visualization, querying, updating and information privacy.

For me, I just shorten the entire thing to :

> “Big data is a data large or complex enough that made you need to really think how to deal with it”

As a very simplified example, let’s imagine you have a CSV - a file with Comma Separated Values - showing financial transactions. The file will have data such as transaction id, user id, timestamp, value of transaction, etc with about 15 total columns. How would you process (extract - analyse - visualise) the data ? 

Now you have several options depending on the size of the data :

1. If your data is about 500 rows, then you can use a spreadsheet program such as Microsoft Excel.

2. If your data is about 500K rows, then you might have to put the data into a database (either relational or non-relational works fine) and then interact with the data via an application that you either bought or custom made.

3. If your data is about 500M rows, you might want to scale your system to a large scale and leverage a general purpose large-scale data processing engine such as Apache Spark. This means you need to set up more just than a few machine for your data infrastructure, maybe implement various database optimisation techniques, and use custom code to interact with the data. Alternatively, you can use an existing third party platform such as Google Cloud Platform’s Big Query or IBM Big Insight.

The situation will be more complex if you want to add more dimension such as velocity or variety. High volume of data coming in constantly might cause you to implement a message queue like Kafka or data that has many variety of forms might cause you to use a NoSQL database.  Different data dimensions will make you consider different options or add different component to your data processing flow.

As you can see, the way you handle data will change depending on the size and the dimension of your data. This will make your data processing flow become more challenging and you might want to use some big data processing techniques - things like Hadoop, Spark, Kafka, etc - which means, yeah, you are working on big data !

TLDR: Don’t wonder too much if you are working with big data or no. Once your data get big and complex enough, you’ll end up using some of big data processing techniques which essentially put you working with big data :)




