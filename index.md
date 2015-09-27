---
layout: default
---



### Fedora

Tips and guides for the [Fedora](https://fedora.org) distribution

{% for page in site.pages %}
  {% if page.title and page.distribution == "fedora" %}
  - <a class="page-link" href="{{ page.url | prepend: site.baseurl }}">{{ page.title }}</a>
  {% endif %}
{% endfor %}
---


### Debian

Tips and guides for the [Debian](https://debian.org) distribution

{% for page in site.pages %}
  {% if page.title and page.distribution == "debian" %}
  - <a class="page-link" href="{{ page.url | prepend: site.baseurl }}">{{ page.title }}</a>
  {% endif %}
{% endfor %}
---

### Arch

*Tips and guides for the Arch distribution need to be written...*

---


### Gentoo

*Tips and guides for the [Gentoo](https://www.gentoo.org) distribution need to be written...*

---


### openSUSE

*Tips and guides for the [openSUSE](https://www.opensuse.org) distribution need to be written...*

---


### Slackware

*Tips and guides for the [Slackware](http://www.slackware.com) distribution need to be written...*

---


*The content of this site is constantly changing, this is a rough pass at structure. This should probably be redone to use Jeykll data values and this is all likely to change, sooner than later :)*
