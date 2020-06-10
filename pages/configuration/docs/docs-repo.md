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

{% raw %}



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


{% endraw %}



 ---
 
