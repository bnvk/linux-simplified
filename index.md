---
layout: default
---

**Linux, Simplified** is a collection of tips & guides for beginner - intermediate level tasks that someone new to desktop Linux (or a new distro) might struggle with. Familiarity with the command line is required.

---

## Fedora

{% for page in site.pages %}
  {% if page.title and page.distribution == "fedora" and page.title != "Fedora" %}
  - <a class="page-link" href="{{ page.url | prepend: site.baseurl }}">{{ page.title }}</a>
  {% endif %}
{% endfor %}
  - Help add more...


Popular distros built on top of [Fedora](https://fedora.org) are [Red Hat Enterprise](http://www.redhat.com/en/technologies/linux-platforms/enterprise-linux), [CentOS](https://www.centos.org), and [Oracle Linux](http://www.oracle.com/us/technologies/linux/overview/index.html)

---


## Debian

{% for page in site.pages %}
  {% if page.title and page.distribution == "debian" and page.title != "Debian" %}
  - <a class="page-link" href="{{ page.url | prepend: site.baseurl }}">{{ page.title }}</a>
  {% endif %}
{% endfor %}
  - Help add more...

Popular distros built on top of [Debian](htttps://debian.org) are: [Ubuntu](http://www.ubuntu.com), [Mint](http://linuxmint.com), and [Elementary OS](https://elementary.io)

---

### Arch

*You should help add guides & tips for [Arch](https://www.archlinux.org) Linux...*

---


### Gentoo

*You should help add guides & tips for [Gentoo](https://www.gentoo.org) Linux...*

---


### openSUSE

*You should help add guides & tips for [openSUSE](https://www.opensuse.org) Linux...*

---


### Slackware

*Tips and guides for the [Slackware](http://www.slackware.com) distribution need to be written...*

---
