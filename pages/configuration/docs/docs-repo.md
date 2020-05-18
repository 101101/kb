---
title: Configuration of Docs Repo
permalink: /pages/configuration/docs-repo/
tags: 
 - docs-repo
 - configuration
 - how-to
description: Configuration info for setting up docs to work with prometheus
---

## Configuration of Docs Repo  


Prometheus and Docs work together through a naming standard.  
  * `Product` affected from Prometheus  
  * `Alert-Name` of the alert firing in Prometheus  
  * `alert-name.md` file in the associated `product` directory  

There are 2 GO templates that can be used:  
_direct link:_  
```go
{{ define "RUNBOOK_LINK" }}https://101101.github.io/kb/docs/{{ .CommonLabels.product }}/{{ .CommonLabels.alertname }}{{ end }}
```
and
_search based:_  
```go
{{ define "RUNBOOK_SEARCH" }}https://101101.github.io/kb/search/?q={{ .CommonLabels.alertname }}{{ end }}
```

I send the search based link to PagerDuty, incase there is a problem with product identification, and I currently use the direct link for Slack.  

**In summary**  
In order for the links to correctly send you to the right runbook, you need to:  
 1. create a `product` directory in `_docs/`  
 1. create a `.md` file in the product directory with the same name as the alert in `prometheus/alert-rules/`  
 1. validate the threshold with the affected team  
 1. verify the alert routes correctly when it triggers  




 ---
 

| Contact: |
| :---------: |
| **[Slack](https://101101workspace.slack.com/archives/D012ESWSXHQ "dsmith73 on 101101 workspace")** |
| ![github.com/dsmith73](https://avatars1.githubusercontent.com/u/44279121?s=60&u=7a933a33b51505f9d6435eeffae1c8156a47dc77&v=4 "github.com/dsmith73") |

