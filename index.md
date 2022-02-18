---
layout: page
title: "Home"
class: home
---

# Welcome!

<div class="columns" markdown="1">

<div class="intro" markdown="1">
My name is Zhuohao Zhang (张倬豪). I am currently a Ph.D. student at University of Washington, focusing on HCI and Accessibility. I am fortunate to work with [Prof. Jacob Wobbrock](https://faculty.washington.edu/wobbrock/){:target="_blank"} at [ACE Lab](http://depts.washington.edu/acelab/index.html){:target="_blank"}. I obtained my Master of Science degree in CS from University of Illinois Urbana-Champaign, where I worked with [Prof. Yang Wang](http://yangwang.ischool.illinois.edu/){:target="_blank"} at [SALT Lab](https://socialcomputing.web.illinois.edu/){:target="_blank"}. I also worked closely with [Prof. Sauvik Das](https://sauvikdas.com/){:target="_blank"} at Georgia Tech, [Prof. Shiri Azenkot](http://shiriazenkot.com/){:target="_blank"} at Cornell Tech, and [Prof. Yingcai Wu](http://www.ycwu.org/){:target="_blank"} at Zhejiang University, where I obtained my Bachelor degree in CS. 

I am interested in integrating human intellect to solve real-world accessibility problems when AI is not a perfect solution. The specific user groups I have been targeting on are people with visual impairments and people with no technical backgrounds but need to engage in novel techniques. Recently, I am working on making creative workspaces accessible for blind people.
</div>

<div class="me" markdown="1">
<picture>
  <img
    src='/images/zhuohao.jpg'
    alt='Zhuohao Zhang at CHI 2019 standing in front of a poster, wearing a black sweater.'>
</picture>

{:.no-list}
* <i class="fas fa-envelope" aria-hidden="true"></i> zhuohao [at] uw.edu
* <i class="fab fa-twitter" aria-hidden="true"></i> <a href="https://twitter.com/ZhuohaoZhang" target= "_blank"> @ZhuohaoZhang</a>
* Photo taken at CHI 2019
</div>

</div>

## <a href="{{ "/projects/" | relative_url }}">Projects</a>

<div class="featured-projects">
  {% assign sorted_projects = site.data.projects | sort: 'highlight' %}
  {% for project in sorted_projects %}
    {% if project.highlight %}
      {% include project.html project=project %}
    {% endif %}
  {% endfor %}
</div>
<a href="{{ "/projects/" | relative_url }}" class="button">
  <i class="fas fa-chevron-circle-right"></i>
  Show All Projects
</a>

## Selected <a href="{{ "/publications/" | relative_url }}">Publications</a>

<div class="featured-publications">
  {% assign sorted_publications = site.publications | sort: 'year' | reverse %}
  {% for pub in sorted_publications %}
    {% if pub.highlight %}
      <a href="{{ pub.pdf }}" class="publication">
        <strong>{{ pub.title }}</strong><br/>
        <span class="authors">{% for author in pub.authors %}{{ author }}{% unless forloop.last %}, {% endunless %}{% endfor %}</span>. <br/>
        <i>{% if pub.venue %}{{ pub.venue }}, {% endif %}{{ pub.year }}</i>.
        <!-- {% for award in pub.awards %}<br/><span class="award"><i class="fas fa-{% if award == "Best Paper Award" %}trophy{% else %}award{% endif %}" aria-hidden="true"></i> {{ award }}</span>{% endfor %} -->
      </a>
    {% endif %}
  {% endfor %}
</div>

<a href="{{ "/publications/" | relative_url }}" class="button">
  <i class="fas fa-chevron-circle-right"></i>
  Show All Publications
</a>

<div class="news-travel" markdown="1">

<div class="news" markdown="1">
## News

<ul>
{% for news in site.data.news limit:10 %}
  {% include news.html news=news %}
{% endfor %}
</ul>

</div>

<div class="travel" markdown="1">
## Travels and Talks

<table>
<tbody>
{% assign future_travel = site.data.travel | where_exp:'item','item.start == null' %}
{% for travel in future_travel %}
  {% include travel.html travel=travel %}
{% endfor %}
{% assign sorted_travel = site.data.travel | where_exp:'item','item.start' | sort: 'start' | reverse %}
{% for travel in sorted_travel limit:10 %}
  {% include travel.html travel=travel %}
{% endfor %}
</tbody>
</table>

</div>

</div>