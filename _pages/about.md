---
layout: page
title: About
permalink: /about
comments: true
---

[Jump to author biographies](#authors)

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

<h2 id="authors">Author Biographies</h2>
  {% assign author_list = site.data.authors %}
  <div class="author-nav">
    <ul>
      {% for author in author_list %}
        {% assign author_data  = author[1] %}
        <li>
              <a href="#{{ author[0] }}">{{ author_data.display_name }}</a>
        </li>
      {% endfor %}
    </ul>
  </div>
<div class="authorpage">
  {% for author in author_list %}
    <div id="{{ author[0] }}">
    {% assign author_data  = author[1] %}
    {% assign bio = author_data.bio %}
      <h2>{{ author_data.display_name }}</h2>
        <div class="row post-top-meta">
        <div class="col-xs-12 col-md-3 col-lg-2 text-center text-md-left mb-4 mb-md-0">
            {% if author_data.avatar %}
            <img class="author-thumb" src="{{site.baseurl}}/{{ author_data.avatar }}"
                alt="{{ author_data.display_name }}">
            {% else %}
            <img class="author-thumb"
                src="https://www.gravatar.com/avatar/{{ author_data.gravatar }}?s=250&d=mm&r=x"
                alt="{{ author_data.display_name }}">
            {% endif %}
        </div>
        <div class="col-xs-12 col-md-9 col-lg-10 text-center text-md-left">
            {% if author_data.follow %}
                <a target="_blank" href="{{ author_data.follow }}" class="btn follow">Follow</a>
            {% endif %}
            <span class="author-description">{{ author_data.description }}</span>
        </div>
    </div>
      <p>{{ bio | markdownify }}</p>
      <a href="{{ site.baseurl }}/{{ author[0] }}">Read posts by {{ author_data.name }}</a>
      <p></p>
    </div>
  {% endfor %}
</div>
