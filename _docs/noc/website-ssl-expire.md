---
title: website-ssl-expire
permalink: /docs/noc/website-ssl-expire/
tags: 
 - noc
 - ssl
 - certificate
 - expire
category:
 - noc
description: Process for website-ssl-expire
---

# website-ssl-expire  

> *what to do when a alert received for website ssl certificate expiring* 


---
[![](https://mermaid.ink/img/eyJjb2RlIjoiZ3JhcGggTFJcblxuICBzdWJncmFwaCBzZzAgW1NTTCBFeHBpcmluZ11cbiAgYTEoW0FsZXJ0IFJlY2VpdmVkXSlcbiAgZW5kXG4gIHN1YmdyYXBoIHNnMSBbVmFsaWRhdGVdXG4gIGExIC0uLT4gYTJcbiAgYTJbW1wiZmE6ZmEtY29kZSBWYWxpZGF0ZSBFeHBpcmF0aW9uICZsZTsgMTAgZGF5c1wiXV0gXG4gIGVuZFxuXG4gIHN1YmdyYXBoIHNnMiBbTm90aWZ5XVxuICBhMiAtLi0-IG4zW1tOb3RpZnkgVGVhbV1dXG4gIGVuZFxuXG4iLCJtZXJtYWlkIjp7InRoZW1lIjoibmV1dHJhbCJ9LCJ1cGRhdGVFZGl0b3IiOmZhbHNlfQ)](https://mermaid-js.github.io/mermaid-live-editor/#/edit/eyJjb2RlIjoiZ3JhcGggTFJcblxuICBzdWJncmFwaCBzZzAgW1NTTCBFeHBpcmluZ11cbiAgYTEoW0FsZXJ0IFJlY2VpdmVkXSlcbiAgZW5kXG4gIHN1YmdyYXBoIHNnMSBbVmFsaWRhdGVdXG4gIGExIC0uLT4gYTJcbiAgYTJbW1wiZmE6ZmEtY29kZSBWYWxpZGF0ZSBFeHBpcmF0aW9uICZsZTsgMTAgZGF5c1wiXV0gXG4gIGVuZFxuXG4gIHN1YmdyYXBoIHNnMiBbTm90aWZ5XVxuICBhMiAtLi0-IG4zW1tOb3RpZnkgVGVhbV1dXG4gIGVuZFxuXG4iLCJtZXJtYWlkIjp7InRoZW1lIjoibmV1dHJhbCJ9LCJ1cGRhdGVFZGl0b3IiOmZhbHNlfQ)  



---

- [ ] Validate that cert is expiring  
- [ ] verify with `script`  
  * Expiring?
    - [ ] **YES** - goto **[unresponsive-service](./unresponsive-service.md)**
    - [ ] **NO** - Start the service  
       * Did it start?
        - [ ] **YES** - Notify Team  
        - [ ] **NO** - Investigate False Alert  


---

### The mermaid code:  

```mermaid
graph LR
  subgraph sg0 [SSL Expiring]
  a1([Alert Received])
  end
  
  subgraph sg1 [Validate]
  a1 -.-> a2
  a2[["fa:fa-code Validate Expiration &le; 10 days"]] 
  end

  subgraph sg2 [Notify]
  a2 -.-> n3[[Notify Team]]
  end
```
Flowchart can be edited **[here](https://mermaid-js.github.io/mermaid-live-editor)**  

---

| Contact: |
| :---------: |
| **[Slack](https://101101workspace.slack.com/archives/D012ESWSXHQ "dsmith73 on 101101 workspace")**  / **[Discord](https://discord.gg/RmzVNzx)** |
| ![github.com/dsmith73](https://avatars1.githubusercontent.com/u/44279121?s=60&u=7a933a33b51505f9d6435eeffae1c8156a47dc77&v=4 "github.com/dsmith73") |
