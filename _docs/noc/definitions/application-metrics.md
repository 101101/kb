---
title: application-metrics
permalink: /docs/noc/definitions/application-metrics/
tags: 
 - noc
 - metric
 - application
category: noc
description: standard application-metrics to monitor for app health  
---

# application-metrics  

### Uptime %  
  *	Used to measure uptime / availability.  
  *	Issues with this metric equate to reduced revenue generation.  
  
### Response Time ms  
  *	Measurement of how long it takes the application or infrastructure to respond.  
  *	Poor response time indicates communication or processing issues along the application path.  
  
### Error Rate %  
  *	Percentage of errors generated per minute.  
  *	Higher error rates indicate problems with the application or the hosted infrastructure.  
  
### Requests per Second  
  *	Indication of incoming load to the environment; precursor to other load indicators.  
  *	Higher numbers mean that the environment will start to experience heavy load.  
  
### Fast, Slow, Very Slow, Stalled, Failed Requests  
  *	Indicates how Application Transactions are performing.  
  *	Poor numbers indicate an issue with a transaction or the hardware supporting the application.  
  
### Threads  
  *	Measurement of the amount of processes that an application is using to process work.  
  *	High thread counts indicate an unhealthy condition in the application.  
  
### Count of Application Instances (Extensible architectures)  
  *	Measurement of node churn to identify processing issues or load.  
  *	Higher numbers indicate issues with expansion, the trigger, or increased environmental load.  


---

