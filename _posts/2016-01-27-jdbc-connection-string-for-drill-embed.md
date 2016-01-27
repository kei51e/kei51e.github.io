---
layout: post
title: JDBC connection string for running drill-embedded instance
---

The answer is `jdbc:drill:drillbit=localhost`. Thanks to the post on stackoverflow:  http://stackoverflow.com/questions/31654658/apache-drill-connection-to-drill-in-embedded-mode-java
 
```java
Class.forName("org.apache.drill.jdbc.Driver");
Connection conn = DriverManager.getConnection("jdbc:drill:drillbit=localhost");
```      
