---
title: url-monitoring
permalink: /docs/infra/url-monitoring/
tags: 
 - prometheus
 - url-monitoring
 - website
 - blackbox
description: yaml configuration for url-monitoring
---

## url-monitoring

I created several files in `prometheus/url-monitoring/xxxxx.yml` to handle url monitoring  
They're formatted like:  
```yml
## url-monitoring configuration

- targets:
    #url;humanname;lob;webservice
    ### Slack  
    - https://www.slack.com;slack.com;it;3rd-party
    ### PagerDuty  
    - https://yourcompany.pagerduty.com;pagerduty.com;it;3rd-party
    ### ServiceNOW  
    - https://yourcompany.service-now.com;service-now.com;it;3rd-party
    ### AppDynamics
    - https://yourcompany-prod.saas.appdynamics.com;prod.saas.appdynamics.com;it;3rd-party
    ### Zoom  
    - https://yourcompany.zoom.us;zoom.us;it;3rd-party
    ### Okta  
    - https://yourcompany.okta.com;okta.com;it;3rd-party
    ### Jira / Atlassian  
    - https://yourcompany.atlassian.net;atlassian.net;it;3rd-party
    ### Splunk  
    - https://yourcompany.splunkcloud.com;splunkcloud.com;it;3rd-party
    ### OpsRamp  
    - https://yourcompany.app.opsramp.com;opsramp.com;it;3rd-party
    ### Microsoft Office  
    - https://www.office.com;office.com;it;3rd-party    
```

Then in the `prometheus.yml` I added:
```yml
  - job_name: 'blackbox'
    metrics_path: /probe
    scrape_interval: 30s
    scheme: http
    params:
      module: [http_2xx]  # Look for a HTTP 200 response.  
    file_sd_configs:
      - files:
        - './url-monitoring/*.yml'
    # more info here: https://prometheus.io/docs/prometheus/latest/configuration/configuration/#static_config  
    relabel_configs:
      - source_labels: [__address__]
        regex: '(.*);(.*);(.*);(.*)'  #first is the url, unique for instance  
        target_label: instance
        replacement: $1
      - source_labels: [__address__]
        regex: '(.*);(.*);(.*);(.*)'  #second is humanname to use in charts  
        target_label: humanname
        replacement: $2
      - source_labels: [__address__]
        regex: '(.*);(.*);(.*);(.*)'  #third which Line of Business (LOB) owns this route    
        target_label: lob
        replacement: $3
      - source_labels: [__address__]
        regex: '(.*);(.*);(.*);(.*)'  #fourth is which web-service the url is supporting    
        target_label: webservice
        replacement: $4
      - source_labels: [instance]
        target_label: __param_target
      - target_label: __address__
        replacement: blackbox:9115    
```















---

![github.com/dsmith73](https://avatars1.githubusercontent.com/u/44279121?s=60&u=7a933a33b51505f9d6435eeffae1c8156a47dc77&v=4 "github.com/dsmith73")  

