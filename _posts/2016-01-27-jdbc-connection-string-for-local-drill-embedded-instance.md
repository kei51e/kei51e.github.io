---
layout: post
title: JDBC connection string for local drill-embedded instance
---

If you want to connect to the local drill-embedded instance already running using jdbc, 
you can use `jdbc:drill:drillbit=localhost` for a jdbc connection string. 
Thanks to the post on stackoverflow:  http://stackoverflow.com/questions/31654658/apache-drill-connection-to-drill-in-embedded-mode-java
 
```java
Class.forName("org.apache.drill.jdbc.Driver");
Connection conn = DriverManager.getConnection("jdbc:drill:drillbit=localhost");
```      
