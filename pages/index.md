---
layout: page
title: Welcome
permalink: /
---

# Welcome to kb

> KB is a simple, crisp, responsive, and searchable, document management solution, which leverages github.

---

### Build Status : [![CircleCI](https://circleci.com/gh/101101/kb/tree/master.svg?style=shield)](https://circleci.com/gh/101101/kb/tree/master)  

---

### Purpose

KB was created to integrate with monitoring solutions like Prometheus, which I architect. They will leverage this product to quickly identify Processes, Runbooks, Instructions, Policies, etc, by passing tags to the integrated communication platforms, and allowing the customer to use hot-links to rapidly lookup, identify, and access documents within KB, to improve efficiency. 


### Features

The Runbooks in `/docs` are searchable, and links are created to these when alerts fire from Prometheus. There are integrations with Slack and PagerDuty, for quick reference to runbooks during impacts.

---

### Example  

When an alert comes in, a tag is used to lookup the associated runbook.  

Here's a sample alert that arrived in Slack:  
![sample-slack-alert.jpg]({{ site.baseurl }}/assets/img/sample-slack-alert.jpg "slack alert")  

When you click the **Runbook** link, it performs a search for the associated runbook and presents the customer with options:  
![sample-search-result.jpg]({{ site.baseurl }}/assets/img/sample-search-result.jpg "search result")  

This is easily achieved by correlating the `alert name` to the `runbook name`. *With repository growth, more complex tag passing options are available, and weighted answers could be generated.*  

---

Would you like to request a feature or contribute?
[Open an issue]({{ site.repo }}/issues)

---

| **[Slack](https://101101workspace.slack.com/archives/D012ESWSXHQ "dsmith73 on 101101 workspace")** |
| :---------: |
| ![github.com/dsmith73](https://avatars1.githubusercontent.com/u/44279121?s=60&u=7a933a33b51505f9d6435eeffae1c8156a47dc77&v=4 "github.com/dsmith73") |
