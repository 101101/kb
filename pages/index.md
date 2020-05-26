---
layout: page
title: welcome
permalink: /
---

# Welcome to kb

> This is a searchable, flat, document storage frontend, which leverages github for document management.

| Build Status |
| :----------: |
| [![CircleCI](https://circleci.com/gh/101101/kb/tree/master.svg?style=shield)](https://circleci.com/gh/101101/kb/tree/master) |  


## Purpose

This was created to integrate with the Prometheus monitoring solution which I architected.  


## Features

The Runbooks in `/docs` are searchable, and links are created to these when alerts fire from Prometheus. There are integrations with Slack and PagerDuty, for quick reference to runbooks during impacts.

## Sample  

When an alert comes in, a tag is used to lookup the associated runbook.  

Here's a sample alert that arrived in Slack:  
![sample-slack-alert.jpg]({{ site.baseurl }}/assets/img/sample-slack-alert.jpg "slack alert")  

When you click the **Runbook** link, it performs a search for the associated runbook:  
![sample-search-result.jpg]({{ site.baseurl }}/assets/img/sample-search-result.jpg "search result")  

---

Would you like to request a feature or contribute?
[Open an issue]({{ site.repo }}/issues)

---

| **[Slack](https://101101workspace.slack.com/archives/D012ESWSXHQ "dsmith73 on 101101 workspace")** |
| :---------: |
| ![github.com/dsmith73](https://avatars1.githubusercontent.com/u/44279121?s=60&u=7a933a33b51505f9d6435eeffae1c8156a47dc77&v=4 "github.com/dsmith73") |
