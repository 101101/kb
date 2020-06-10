---
title: templates.md
permalink: /pages/configuration/alertmanager/templates/
tags: 
 - alertmanager
 - templates
 - tmpl
description: templates.tmpl configuration
---

## templates.tmpl configuration  

{% raw %}

.
.
.
.
.
```go
# Slack Title  
{{ define "SLACK_MSG_TITLE" }}
    {{ if eq .Status "resolved" }}
        {{- .Status | toUpper }} : {{ template "SLACK_TITLE_SUMMARY" . }}
    {{ else if eq .Status "firing" }}
        {{ .CommonLabels.severity | toUpper }} : {{ template "SLACK_TITLE_SUMMARY" . }}
    {{ end }}
{{ end }}
```

.
.
.

```go
#Slack Summary
{{ define "SLACK_TITLE_SUMMARY" -}}
    {{- if .CommonAnnotations.summary -}}
        {{- .CommonAnnotations.summary -}}
    {{- else -}}
        {{- with index .Alerts 0 -}}
            {{- .Annotations.summary -}}
        {{- end -}}
    {{- end -}}
{{- end -}}
```

.
.
.

```go
# Slack Text  
{{define "SLACK_MSG_TEXT" }}
      <!here> - {{ .CommonAnnotations.description }}
      `View:` :chart_with_upwards_trend:*<{{ (index .Alerts 0).GeneratorURL }}|Prometheus>* or :notebook:*<{{ template "RUNBOOK_LINK" . }}|Runbook>* or *<Set this up|:slack_call:>*

      *Details:*
      {{ range .CommonLabels.SortedPairs }}• *{{ .Name }}:* `{{ .Value }}`
    {{ end }}
{{ end }}
```

.
.
.

```go
# Slack Color
{{ define "SLACK_MSG_COLOR" }}{{ if eq .Status "firing" }}{{ if eq .CommonLabels.severity "critical" }}danger{{ else if eq .CommonLabels.severity "error" }}danger{{ else if eq .CommonLabels.severity "warning" }}warning{{ else }}#439FE0{{ end }}{{ else}}good{{ end }}{{ end }}
```

.
.
.

```go
# Runbook Link
{{ define "RUNBOOK_LINK" }}https://101101.github.io/kb/docs/{{ .CommonLabels.product }}/{{ .CommonLabels.alertname }}{{ end }}

# Runbook Search
{{ define "RUNBOOK_SEARCH" }}https://101101.github.io/kb/search/?q={{ .CommonLabels.alertname }}{{ end }}
```

.
.
.

```go
# Pagerduty description  
{{ define "PAGERDUTY_DESCRIPTION" }}
    {{if .CommonAnnotations.summary }}{{ .CommonAnnotations.summary }}
    {{ else }}{{ .GroupLabels.alertname }}
    {{ if .CommonLabels.instance }}{{ .CommonLabels.instance }}
    {{ end }}
    {{ end }}
{{ end }}
```

.
.
.

{% endraw %}

---

![github.com/dsmith73](https://avatars1.githubusercontent.com/u/44279121?s=60&u=7a933a33b51505f9d6435eeffae1c8156a47dc77&v=4 "github.com/dsmith73")  



















