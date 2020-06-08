---
title: NOC
permalink: /noc/
---

# NOC

{% if user %}
  Hello {{ user.name }}!
{% endif %}

Welcome to the {{ site.title }} NOC pages! Here you can quickly jump to a 
particular page.

---

### TEST 3

{% capture site_tags %}{% for tag in site.tags %}{% if tag %}{{ tag | first }}{% unless forloop.last %},{% endunless %}{% endif %}{% endfor %}{% endcapture %}{% assign docs_tags = "" %}{% for doc in site.docs %}{% assign ttags = doc.tags | join:',' | append:',' %}{% assign docs_tags = docs_tags | append:ttags %}{% endfor %}
{% assign all_tags = site_tags | append:docs_tags %}{% assign tags_list = all_tags | split:',' | uniq | sort %}

{% for tag in tags_list %}{% if tag %}<h3 id="{{ tag | replace: '/', '-' }}" class="linked-section">{{ tag }}</h3>
<div class="post-list" style="margin-bottom:40px">
    {% for post in site.tags[tag] %}<div class="tag-entry">
    <a href="{{- site.url -}}{{- post.url -}}">{{- post.title -}}</a>
    <time style="font-style:italic; float:right" datetime="{{- post.date | date_to_xmlschema -}}"> {{- post.date | date: "%B %d, %Y" -}}</time>
</div>{%- endfor -%}
{% for doc in site.docs %}{% if doc.tags contains tag %}
<div class="tag-entry">
    <a href="{{- site.baseurl -}}{{- doc.url -}}">{{ doc.title }}</a>
        <time style="font-style:italic; float:right" datetime="{{- doc.date | date_to_xmlschema -}}"> {{- doc.date | date: "%B %d, %Y" -}}</time>
    </div>{% endif %}{% endfor %}
</div>{% endif %}{%- endfor -%}


---

### TEST 6

{% for doc in site.docs %}
    {% if doc.category == "noc" %}
        <div class="entry">
        <h5><a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a></h5>
        <p>{{ post.description }}</p>
        </div>
    {% endif %}
{% endfor %}

---

### TEST 7

{% for t in site.tags %}
    {% if t contains 'noc' %}     
        <div class="entry">
        <h5><a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a></h5>
        <p>{{ post.description }}</p>
        </div>
    {% endif %}
{% endfor %}

---

### TEST 8

{% for post in site.docs %}
    {% if post.category contains "noc" %}
        <div class="entry">
        <h5><a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a></h5>
        <p>{{ post.description }}</p>
        </div>
    {% endif %}
{% endfor %}

---

### TEST 9

{% for post in site.docs %}
    {% if post.category == "noc" %}
        <div class="entry">
        <h5><a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a></h5>
        <p>{{ post.description }}</p>
        </div>
    {% endif %}
{% endfor %}

---

| Contact: |
| :---------: |
| **[Slack](https://101101workspace.slack.com/archives/D012ESWSXHQ "dsmith73 on 101101 workspace")** / **[Discord](https://discord.gg/RmzVNzx)** / **[Teams](https://teams.microsoft.com/l/chat/0/0?users=dsmith73@gmail.com)** |
| ![github.com/dsmith73](https://avatars1.githubusercontent.com/u/44279121?s=60&u=7a933a33b51505f9d6435eeffae1c8156a47dc77&v=4 "github.com/dsmith73") |

