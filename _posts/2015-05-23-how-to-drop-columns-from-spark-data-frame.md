---
layout: post
title: How to drop columns from a spark data frame in scala
---

```
import org.apache.spark.sql._
val frame = ...

val newframe =
  frame.select(frame.columns.filter(c => c != "columnToDrop").map(c => new Column(c)).toList :_*)

```

In R/dplyr world, you can drop column A from a data frame by just specifying `select(-A)` ,
but there's no such easy way in spark data frames.
so basically you need to list all the columns you want to keep in the select
function. The key here is to use a filter function to filter out unwanted
column(s). It is useful especially if you want to drop only a few columns
out of many columns.  

It is based on Spark 1.3.1.
