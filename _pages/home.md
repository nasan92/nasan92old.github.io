---
permalink: /
title: "Welcome"
excerpt: "About me"
author_profile: true
redirect_from: 
  - /home/
  - /home.html
---

<!--- just ![Editing a markdown file for a talk](/images/denali.jpg ) ---> 
<!-- 
## Powershell Blog Posts
[search-gpo](/posts/2021/05/search-gpo/)
## Azure Blog Posts
## General IT 
[gpresult-remote](/posts/2021/05/gpresult-remote/)
 ---> 
 ## Recent posts
---

<section class="archive-post-list">
   {% for post in site.posts %}
       {% assign currentDate = post.date | date: "%Y" %}
       {% if currentDate != myDate %}
           {% unless forloop.first %}</ul>{% endunless %}
            <h3> {{ currentDate }} </h3>
           <ul>
           {% assign myDate = currentDate %}
       {% endif %}
       <li><a href="{{ post.url }}">{{ post.title }}<span style="color:blue;font-size:10px"> {{ post.date | date: "%B %-d" }}</span></a></li>
       {% if forloop.last %}</ul>{% endif %}
   {% endfor %}
</section>
