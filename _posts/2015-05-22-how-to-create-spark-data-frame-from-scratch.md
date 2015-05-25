---
layout: post
title: How to create a spark data frame from scratch in scala
---

```
import org.apache.spark.sql.Row
import org.apache.spark.sql.types._


val schema = StructType(Array(
  StructField("name", StringType, true),
  StructField("price", DoubleType, true)
))

val data = sc.parallelize(Seq(Row("MacBook", 1499.99)))
val frame = sqlContext.createDataFrame(data, schema)
```

The point is, you can create an RDD object by calling
`SparkContext#parallelize` function. In this way you can
create a data frame without any input file.

It is based on Spark 1.3.1.
