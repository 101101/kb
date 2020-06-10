---
title: hardware-metrics
permalink: /docs/noc/definitions/hardware-metrics/
tags: 
 - noc
 - metric
 - hardware
 - infrastructure
category:
 - noc
description: hardware-metrics
---

# hardware-metrics  

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
  
### Load  
  *	How efficiently the node is using CPU, Memory, and Disk.  
  *	Load ≥ 8 indicates the node is having difficulty keeping up with work.  
  
### Open Files Descriptors (OFD)  
  *	Measurement of the current/total available OFD.  
  *	High percentage of OFD indicates an unhealthy application.  

---

