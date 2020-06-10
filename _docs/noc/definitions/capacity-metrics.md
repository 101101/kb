---
title: capacity-metrics
permalink: /docs/noc/definitions/capacity-metrics/
tags: 
 - noc
 - metric
 - capacity
category:
 - noc
description: capacity-metrics are to identify when environments should be grown, to handle increasing demand on resources
---

# Core Targeted Capacity Metrics  
> Used to identify when environments should be grown, to handle increasing demand on resources. While these metrics are intended for growth planning, they will also have a hard upper limit for alerting, since maxing them out will have impactful results in the environment.  

---

**CPU –** % Utilization, % Busy, and Wait time  

**Memory –** % Utilization  

**Disk –** % Utilization, I/O Wait time, Queue Length  

**Apdex Rating –** Lower Apdex rating indicates poor user satisfaction with product performance  
  * `((# Satisfactory samples) + (0.5 * (# Tolerating samples))) / Total number samples = Apdex Score`  

---

