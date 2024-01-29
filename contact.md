---
layout: default
is_contact: true
title: "./jpdias/contact"
---

## Contact

<i class="far fa-envelope"></i> Email: [majid.babaei[at]mcgill.ca](mailto:majid.babaei@mcgill.ca)

### Address

> Majid Babaei
>
> McGill University,
> 680 Sherbrooke St W 13th Floor, RM#1323
> Montréal, QC, Canada H3A 2M7

### Social

{% for entry in site.social %}
<a href="{{ entry.url }}" target="_blank"><i class="{{ entry.icon }}"></i> {{ entry.name }}</a>
{% endfor %}

### Academic

{% for entry in site.academic %}
<a href="{{ entry.url }}" target="_blank"><i class="{{ entry.icon }}"></i> {{ entry.name }}</a>
{% endfor %}
