---
layout: default
title: "./majidbabaei.com/"
description: "Passionate Educator. Software Engineer. Key Note Speaker. Pro Mountain Biker"
---

## About Me

<img class="profile-picture" src="images/profile.png" alt="Profile picture">

{% highlight bash %}
$ whoami
Passionate Educator. Software Engineer. Key Note Speaker. Pro Mountain Biker.
{% endhighlight %}

Dr. Majid Babaei holds a Ph.D. in Software Engineering with a focus on debugging and testing distributed systems at the model-level under the supervision of [Prof. Juergen Dingel](https://www.cs.queensu.ca/people/Juergen/Dingel). He is a member of the Professional Development Committee at the Canadian Association for University Continuing Education ([CAUCE](<(https://cauce-aepuc.ca/)>)).

From collaborating with [Bosch Engineering Group](https://www.bosch-engineering.com/) in Germany to working as a Senior Software Developer and DevOps Engineer at the [National Research Council of Canada] (https://nrc.canada.ca/en) (NRC), Majid has gained invaluable industry experience. He has collaborated in the development of [Row64] (https://row64.com/), a GPU-enabled spreadsheet system, that allows users to work with massive datasets and generate stunning graphics.

Majid is a passionate educator, having taught courses on cutting-edge topics like Software Delivery, Operating Systems, and Applied Machine Learning at different institutions such as [St.Lawrence College](https://www.stlawrencecollege.ca/), [Queen's University] (https://www.queensu.ca/), [Concordia University](https://www.concordia.ca/), and [McGill University](https://www.mcgill.ca/). His dedication to academia extends to the School of Continuing Studies at McGill University, where he serves as an assistant professor and academic program coordinator.

## Research Interests

- Software Engineering
- Model-Driven Engineering
- Internet-of-Things
- Artificial Intelligence

## Recent Publications

{% assign counter = 0 %}

{% for pub in site.data.publications.confs limit:3 %}

{% assign counter = counter | plus:1 %}

<div class="pub-item">
<div class="pub-title"><span>[{{ counter }}]</span><a href="{{ pub.url }}" target="_blank"><b>{{ pub.title }}</b></a><br></div>
<div><i class="ri-group-line"></i> {{ pub.authors }}</div>
<div><i class="ri-book-3-line"></i>  {{ pub.conference }}</div>
</div>

{% endfor %}

{% for pub in site.data.publications.journals limit:2 %}

{% assign counter = counter | plus:1 %}

<div class="pub-item">
<div class="pub-title"><span>[{{ counter }}]</span><a href="{{ pub.url }}" target="_blank"><b>{{ pub.title }}</b></a><br></div>
<div><i class="ri-group-line"></i> {{ pub.authors }}</div>
<div><i class="ri-book-3-line"></i>  {{ pub.conference }}</div>
</div>

{% endfor %}

<a href="/publications"><i class="ri-add-circle-line"></i> **View More**</a>
