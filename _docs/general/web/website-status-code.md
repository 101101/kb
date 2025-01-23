---
title: website-status-code
permalink: /docs/general/web/website-status-code/
tags: 
 - web
 - website
 - status
category:
 - web
description: Process for website-status-code
---

# website-status-code  

> *what to do when a alert received for website-status-code* 
general information on status codes can be found here: [httpstatuses](https://httpstatuses.com)  

---

[![](https://mermaid.ink/img/eyJjb2RlIjoiZ3JhcGggVERcblx0Q3tTdGF0dXMgQ29kZSBSZWNlaXZlZH1cblxuICBDIC0tPnw8PTE5OSBvciA-PTQwMHwgRHtTZXJ2aWNlcyBVUD99XG5cdEMgLS0-fDB8IEZbVmFsaWRhdGUgUXVlcnkgTWV0aG9kXVxuICBGIC0tPkYxe1dlYnNpdGUgJiBRdWVyeSBTYW1lP31cbiAgRCAtLT58Tk98IEQxW1N0YXJ0IFNlcnZpY2VzXVxuXG4gIEQxIC0tPiBEMntSZXNvbHZlZD99XG4gIEQyIC0tPnxZRVN8IEQzW1Jlc2VhcmNoIElzc3VlXVxuICBEMiAtLT58Tk98IEQ0W0NvbnRhY3QgSW5mcmEgZm9yIGFzc2lzdGFuY2VdXG4gIEQgLS0-fFlFU3wgRDVbQ29udGFjdCBQcm9kdWN0IHRlYW0gZm9yIGFzc2lzdGFuY2VdXG4gIFxuICBGMSAtLT58Tk98IEYyW0ZpeCBxdWVyeV1cbiAgRjEgLS0-fFlFU3wgRjNbQ29udGFjdCBQcm9kdWN0IHRlYW1dXG4iLCJtZXJtYWlkIjp7InRoZW1lIjoibmV1dHJhbCJ9LCJ1cGRhdGVFZGl0b3IiOmZhbHNlfQ)](https://mermaid-js.github.io/mermaid-live-editor/#/edit/eyJjb2RlIjoiZ3JhcGggVERcblx0Q3tTdGF0dXMgQ29kZSBSZWNlaXZlZH1cblxuICBDIC0tPnw8PTE5OSBvciA-PTQwMHwgRHtTZXJ2aWNlcyBVUD99XG5cdEMgLS0-fDB8IEZbVmFsaWRhdGUgUXVlcnkgTWV0aG9kXVxuICBGIC0tPkYxe1dlYnNpdGUgJiBRdWVyeSBTYW1lP31cbiAgRCAtLT58Tk98IEQxW1N0YXJ0IFNlcnZpY2VzXVxuXG4gIEQxIC0tPiBEMntSZXNvbHZlZD99XG4gIEQyIC0tPnxZRVN8IEQzW1Jlc2VhcmNoIElzc3VlXVxuICBEMiAtLT58Tk98IEQ0W0NvbnRhY3QgSW5mcmEgZm9yIGFzc2lzdGFuY2VdXG4gIEQgLS0-fFlFU3wgRDVbQ29udGFjdCBQcm9kdWN0IHRlYW0gZm9yIGFzc2lzdGFuY2VdXG4gIFxuICBGMSAtLT58Tk98IEYyW0ZpeCBxdWVyeV1cbiAgRjEgLS0-fFlFU3wgRjNbQ29udGFjdCBQcm9kdWN0IHRlYW1dXG4iLCJtZXJtYWlkIjp7InRoZW1lIjoibmV1dHJhbCJ9LCJ1cGRhdGVFZGl0b3IiOmZhbHNlfQ)  

---

### HTTP Status Code `<= 199 OR >= 400`

- [ ] Validate services are up on host servers    
  * UP?
    - [ ] **YES** - Pull recent changes and contact Product team  
    - [ ] **NO** - Start services
      * UP?
        - [ ] **YES** - 
          * Pull recent changes  
          * Research issue to understand why services went down and inform owning team  
        - [ ] **NO** - Contact Infra for assistance  


---

### HTTP Status Code `0`

- [ ] Validate query method (`HTTP or HTTPS`)  
- [ ] Open website  
  * Does it match query method?
    - [ ] **YES** - Website is HTTP & query is HTTP or Website is HTTPS & query is HTTPS  
      * Contact Product team to investigate scenarios for Response Code `0` in accordance with [W3C Spec](https://fetch.spec.whatwg.org/#concept-network-error)  
    - [ ] **NO** - Update query method in `alert-rules` to match  
      * Alert issue resolved?
        - [ ] **YES** - Close issue   
        - [ ] **NO** - Contact Product team for assistance  

---
