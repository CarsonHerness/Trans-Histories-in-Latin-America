---
layout: page
title: About
permalink: /about
comments: true
---

[Mission Statement](#mission)

[Authors](#authors)

<h2 id="mission">
Mission Statement
</h2>

<div>
<p>
Trans issues around the world are both hidden and rapidly changing. By discussing transnational trans politics and history, our blog adds to and steers a developing discussion. Understanding trans histories is important because public policy pertaining to trans people is in flux globally. The first step towards trans people’s political representation is understanding and interpreting trans histories, because doing so builds a base of historical knowledge from which trans empowerment can be understood and advocated.
</p>
<p>
In our blog, we provide insight into the academic work of trans studies and contemporary trans life in Latin America. Our topic is also significant because trans asylum policy is in flux in the United States, and providing the historical context for activists, students, lawyers and the constituency can garner support for the cause and inform approaches to activism and litigation. 
</p>
<p>
Studying trans history is difficult due to changing vocabulary and different understandings of gender across cultures, regions, and time periods. The purpose of the blog is to highlight the lived experiences of trans people across history.<em> We hope to inspire activists, scholars, and any interested people to know more about trans histories and provide allyship. </em>
</p>
</div>

<h2 id="authors">
Author Bios
</h2>
{{ site.authors }}
<div>
  {% for author in site.authors %}
  {{ author }}
    {% assign current = site.authors[author] %}
    {{ current.display_name }}
      <h2>{{ current.display_name }}</h2>
      <p>{{ current.bio }}</p>
      <a href="{{ site.baseurl }}/{{ current.name }}">Read posts by {{ current.name }}</a>
  {% endfor %}
</div>
