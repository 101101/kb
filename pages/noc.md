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

<div class="section-index">
    <hr class="panel-line">
    {% for post in site.docs.noc  %}        
    <div class="entry">
    <h5><a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a></h5>
    <p>{{ post.description }}</p>
    </div>{% endfor %}
</div>







---

<table>
    <thead>
        <tr>
            <th colspan=2>Contact:</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td rowspan=3><a href="https://dsmith73.github.io"><img src="https://avatars1.githubusercontent.com/u/44279121?s=60&u=7a933a33b51505f9d6435eeffae1c8156a47dc77&v=4" alt="dsmith73.github.io"></a></td>
            <td><b><a href="https://101101workspace.slack.com/archives/D012ESWSXHQ" alt="dsmith73 on Slack">Slack</a></b></td>
        </tr>
        <tr>
            <td><b><a href="https://discord.gg/RmzVNzx" alt="dsmith73 on Discord">Discord</a></b></td>
        </tr>
        <tr>
            <td><b><a href="skype:dsmith73?chat">Skype</a></b> or <b><a href="https://teams.microsoft.com/l/chat/0/0?users=dsmith73@gmail.com">Teams</b></a></td>
        </tr>
    </tbody>
</table>

