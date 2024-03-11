---
layout: page
title: "Home"
class: home
---

# Welcome!

<div class="columns" markdown="1">

<div class="me" markdown="1">
<picture>
  <img
    src='/images/zhuohao.jpg'
    alt='Zhuohao (Jerry) Zhang at CHI 2019 standing in front of a poster, wearing a black sweater.'>
</picture>

{:.no-list}
* <i class="fas fa-envelope" aria-hidden="true"></i> zhuohao [at] uw.edu
* <i class="fab fa-twitter" aria-hidden="true"></i> <a href="https://twitter.com/ZhuohaoZhang" target= "_blank"> @ZhuohaoZhang</a>
* Photo taken at CHI 2019
</div>

<div class="intro" markdown="1">
My name is Zhuohao (Jerry) Zhang (Chinese: 张倬豪). I am currently a Ph.D. student at the University of Washington, focusing on HCI and accessibility research. I am fortunate to work with [Prof. Jacob Wobbrock](https://faculty.washington.edu/wobbrock/){:target="_blank"} at the [ACE Lab](http://depts.washington.edu/acelab/index.html){:target="_blank"}. I obtained my Master of Science degree in CS from the University of Illinois, Urbana-Champaign, where I worked with [Prof. Yang Wang](http://yangwang.ischool.illinois.edu/){:target="_blank"} at the [SALT Lab](https://socialcomputing.web.illinois.edu/){:target="_blank"}, and my Bachelor's degree in CS from Zhejiang University, China. I also worked closely with [Prof. Anhong Guo](https://guoanhong.com/){:target="_blank"} at the University of Michigan and [Prof. Shiri Azenkot](http://shiriazenkot.com/){:target="_blank"} at Cornell Tech. During summers, I also interned at Microsoft Research, Meta Reality Labs, and Adobe Research. My research has been recognized and supported by the [Apple Scholars in AI/ML PhD fellowship](https://machinelearning.apple.com/updates/apple-scholars-aiml-2024){:target="_blank"}.
<!-- I also worked closely with [Prof. Sauvik Das](https://sauvikdas.com/){:target="_blank"} at CMU, [Prof. Shiri Azenkot](http://shiriazenkot.com/){:target="_blank"} at Cornell Tech, and [Prof. Yingcai Wu](http://www.ycwu.org/){:target="_blank"} at Zhejiang University, where I obtained my Bachelor's degree in CS.  -->

I am interested in addressing real-world accessibility problems by designing assistive technologies leveraging multimodal interaction techniques and human-AI collaboration.
<!-- Recently, I am working on designing intelligent interactive systems to enable blind and low-vision people to move from consumers to creators of digital content like slides, visualizations, and even videos. -->
<!-- The specific user groups I have been targeting on include people with visual impairments and people with no technical backgrounds but need to engage in novel technologies.  -->
<!-- integrating human intellect to solve real-world accessibility problems when AI is not a perfect solution.  -->
</div>

</div>

## Selected <a href="{{ "/projects/" | relative_url }}">Projects</a>

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
      <a href="{{ pub.pdf }}" class="publication" target="_blank">
        <strong>{{ pub.title }}</strong><br/>
        <span class="authors">{% for author in pub.authors %}{{ author }}{% unless forloop.last %}, {% endunless %}{% endfor %}</span>. <br/>
        <i>{% if pub.venue %}{{ pub.venue }}, {% endif %}{{ pub.year }}</i>.
        {% for award in pub.awards %}<br/><span class="award"><i class="fas fa-{% if award == "Best Paper Award" %}trophy{% else %}award{% endif %}" aria-hidden="true"></i> {{ award }}</span>{% endfor %}
      </a>
    {% endif %}
  {% endfor %}
</div>

<a href="{{ "/publications/" | relative_url }}" class="button">
  <i class="fas fa-chevron-circle-right"></i>
  Show All Publications
</a>

<!-- <div class="news-travel" markdown="1">

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

</div> -->