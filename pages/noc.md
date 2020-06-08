---
layout: page
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

<div class="section-index">
    <hr class="panel-line">
    {% for post in site.docs %}
        {% if post.category contains "noc" %}
            <div class="entry">
            <h5><a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a></h5>
            <p>{{ post.description }}</p>
            </div>
        {% endif %}
    {% endfor %}
</div>

---

| Contact: |
| :---------: |
| **[Slack](https://101101workspace.slack.com/archives/D012ESWSXHQ "dsmith73 on 101101 workspace")** / **[Discord](https://discord.gg/RmzVNzx)** / **[Teams](https://teams.microsoft.com/l/chat/0/0?users=dsmith73@gmail.com)** |
| ![github.com/dsmith73](https://avatars1.githubusercontent.com/u/44279121?s=60&u=7a933a33b51505f9d6435eeffae1c8156a47dc77&v=4 "github.com/dsmith73") |

