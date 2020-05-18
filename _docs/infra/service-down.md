---
title: service-down
permalink: /docs/infra/service-down/
tags: 
 - infra
 - service-down
 - service
description: What do do when a service-down alert is received  
---

## Service Down

> what to do when a service stops responding on a server  

---

- [ ] Access the target node  
- [ ] Run `ps <service name>` to list the service  
  * Does the service show up?
    - [ ] **YES** - goto **[unresponsive-service](./unresponsive-service.md)**
    - [ ] **NO** - Start the service  
       * Did it start?
        - [ ] **YES** - Validate no other issues & close ticket  
        - [ ] **NO** - goto next step  
- [ ] Run `top` or `htop` to identify running processes  
- [ ] Is the box under heavy load?  
  - [ ] **YES** - Record top processes & goto **[load-issue](./high-load-avg.md "throubleshoot load-issue")**  
  - [ ] **NO** - Restart the service  
    * Was restart successful?
      - [ ] **YES** - Validate no other issues & close ticket  
      - [ ] **NO** - Try restarting again, _and if it still fails_, contact the **[infra team](https://pagerduty.com "This would be a link to the infra on-call in pagerduty")** for assistance  


---
[![](https://mermaid.ink/img/eyJjb2RlIjoiZ3JhcGggVERcbkFbU2VydmljZSBEb3duXSAtLT4gQltBY2Nlc3MgdGhlIHRhcmdldCBub2RlXVxuQiAtLT4gQ1tSdW4gcHMgPHNlcnZpY2UgbmFtZT5dXG5DIC0tPiBEe0RvZXMgdGhlIHNlcnZpY2Ugc2hvdyB1cD99XG5EIC0tPnxZRVN8IEVbZ290byB1bnJlc3BvbnNpdmUtc2VydmljZV1cbkQgLS0-fE5PfCBGW1N0YXJ0IHRoZSBzZXJ2aWNlXVxuRiAtLT4gR3tEaWQgaXQgc3RhcnQ_fVxuRyAtLT58WUVTfCBIW1ZhbGlkYXRlIG5vIG90aGVyIGlzc3Vlc11cbkggLS0tIFNbY2xvc2UgdGlja2V0XVxuRyAtLT58Tk98IElbUnVuIGB0b3BgIG9yIGBodG9wYF1cbkkgLS0-IEp7SXMgdGhlIGJveCB1bmRlciBoZWF2eSBsb2FkP31cbkogLS0-fFlFU3wgS1tSZWNvcmQgdG9wIHByb2Nlc3Nlc11cbksgLS0-IExbZ290byAnbG9hZC1pc3N1ZSddXG5KIC0tPnxOT3wgTVtSZXN0YXJ0IHRoZSBzZXJ2aWNlXVxuTSAtLT4gTntXYXMgcmVzdGFydCBzdWNjZXNzZnVsP31cbk4gLS0-fFlFU3wgT1tWYWxpZGF0ZSBubyBvdGhlciBpc3N1ZXNdXG5PIC0tLSBSW2Nsb3NlIHRpY2tldF1cbk4gLS0-fE5PfCBQW1RyeSByZXN0YXJ0aW5nIGFnYWluXVxuUCAtLS0gUVtpZiBpdCBmYWlscywgY29udGFjdCB0aGUgaW5mcmEgdGVhbV1cblxuXG5cbiIsIm1lcm1haWQiOnsidGhlbWUiOiJkZWZhdWx0In0sInVwZGF0ZUVkaXRvciI6ZmFsc2V9)](https://mermaid-js.github.io/mermaid-live-editor/#/edit/eyJjb2RlIjoiZ3JhcGggVERcbkFbU2VydmljZSBEb3duXSAtLT4gQltBY2Nlc3MgdGhlIHRhcmdldCBub2RlXVxuQiAtLT4gQ1tSdW4gcHMgPHNlcnZpY2UgbmFtZT5dXG5DIC0tPiBEe0RvZXMgdGhlIHNlcnZpY2Ugc2hvdyB1cD99XG5EIC0tPnxZRVN8IEVbZ290byB1bnJlc3BvbnNpdmUtc2VydmljZV1cbkQgLS0-fE5PfCBGW1N0YXJ0IHRoZSBzZXJ2aWNlXVxuRiAtLT4gR3tEaWQgaXQgc3RhcnQ_fVxuRyAtLT58WUVTfCBIW1ZhbGlkYXRlIG5vIG90aGVyIGlzc3Vlc11cbkggLS0tIFNbY2xvc2UgdGlja2V0XVxuRyAtLT58Tk98IElbUnVuIGB0b3BgIG9yIGBodG9wYF1cbkkgLS0-IEp7SXMgdGhlIGJveCB1bmRlciBoZWF2eSBsb2FkP31cbkogLS0-fFlFU3wgS1tSZWNvcmQgdG9wIHByb2Nlc3Nlc11cbksgLS0-IExbZ290byAnbG9hZC1pc3N1ZSddXG5KIC0tPnxOT3wgTVtSZXN0YXJ0IHRoZSBzZXJ2aWNlXVxuTSAtLT4gTntXYXMgcmVzdGFydCBzdWNjZXNzZnVsP31cbk4gLS0-fFlFU3wgT1tWYWxpZGF0ZSBubyBvdGhlciBpc3N1ZXNdXG5PIC0tLSBSW2Nsb3NlIHRpY2tldF1cbk4gLS0-fE5PfCBQW1RyeSByZXN0YXJ0aW5nIGFnYWluXVxuUCAtLS0gUVtpZiBpdCBmYWlscywgY29udGFjdCB0aGUgaW5mcmEgdGVhbV1cblxuXG5cbiIsIm1lcm1haWQiOnsidGhlbWUiOiJkZWZhdWx0In0sInVwZGF0ZUVkaXRvciI6ZmFsc2V9)  


```mermaid
graph TD
A[Service Down] --> B[Access the target node]
B --> C[Run ps -service name- to list the service]
C --> D{Does the service show up?}
D -->|YES| E[goto "unresponsive-service"]
D -->|NO| F[Start the service]
F --> G{Did it start?}
G -->|YES| H[Validate no other issues]
H --- S[close ticket]
G -->|NO| I[goto next step]
I --> J[Run `top` or `htop`]
J --> K{Is the box under heavy load?}
K -->|YES| L[Record top processes & goto "load-issue"]
K -->|NO| M[Restart the service]
M --> N{Was restart successful?}
N -->|YES| O[Validate no other issues]
O --- R[close ticket]
N -->|NO| P[Try restarting again]
P --- Q [if it fails, contact the infra team]
```

---

<meta name="description" content="investigate service failure on server">
<meta name="author" content="Dan Smith">
<meta name="date" content="2020-04-25"> 


![github.com/dsmith73](https://avatars1.githubusercontent.com/u/44279121?s=60&u=7a933a33b51505f9d6435eeffae1c8156a47dc77&v=4 "github.com/dsmith73")  
