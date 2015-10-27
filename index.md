---
title: Oefenweb open-source software
---

# Oefenweb open-source software

{% for repository in site.github.public_repositories %}
* [{{ repository.name }}]({{ repository.html_url }}) - {{ repository.description }}<br />
  [![Build Status](https://img.shields.io/travis/{{ repository.full_name }}.svg)](https://travis-ci.org/{{ repository.full_name }})
  [![Issues](https://img.shields.io/github/issues/{{ repository.full_name }}.svg)]({{ repository.homepage }}/{{ repository.full_name }}/issues)
  [![Tag](https://img.shields.io/github/tag/{{ repository.full_name }}.svg)]({{ repository.homepage }}/{{ repository.full_name }}/tags)
  [![Stars](https://img.shields.io/github/stars/{{ repository.full_name }}.svg)]({{ repository.homepage }}/{{ repository.full_name }}/stargazers)
  [![Forks](https://img.shields.io/github/forks/{{ repository.full_name }}.svg)]({{ repository.homepage }}/{{ repository.full_name }}/network)
{% endfor %}
