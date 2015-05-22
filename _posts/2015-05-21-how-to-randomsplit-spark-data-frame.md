---
layout: post
title: How to randomsplit a spark data frame in scala
---

```
val frame = ...
val splits = frame.rdd.randomSplit(Array(0.7, 0.3))
val (trainRDD, testRDD) = (splits(0), splits(1))
val trainFrame = sqlContext.createDataFrame(trainRDD, frame.schema)
val testFrame = sqlContext.createDataFrame(testRDD, frame.schema)
```

The point is, the schema is the same before and after the split,
so that you can just reuse the same schema from the original
data frame to create back data frames from RDDs.

Note that this is based on Spark 1.3.1. I guess the randomSplit
will be implemeted at the data frame level pretty soon.
