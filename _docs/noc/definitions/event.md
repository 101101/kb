---
title: event
permalink: /docs/noc/definitions/event/
tags: noc event
category:
 - noc
description: An event is a condition which exists in the environment
---

# event  

> An Event is a condition which exists in the environment, while an Alert is an Event which has been evaluated and determined to require some level of action. We focus on alerting for actionable events in the environment, and have adopted the following 80/20 concepts:  

  *	**Production Standard –** Implement metrics and thresholds in the Production and Testing environments which result in action, with the exception being to implement a monitor which does not alert.  
  *	**Non-Production Standard –** Implement metrics and thresholds in lower level environments which would result in action in a Production environment, but suppress alerting, and use the data to deliver regular reports on performance, with the exception being to implement a monitor which does alert.  

---


