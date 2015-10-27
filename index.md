---
title: Oefenweb open-source software
---

# Oefenweb open-source software

{% for repository in site.github.public_repositories %}
* [{{ repository.name }}]({{ repository.html_url }}) - {{ repository.description }}<br />
  [![Build Status](https://img.shields.io/travis/{{ repository.full_name }}.svg)](https://travis-ci.org/{{ repository.full_name }})
{% if repository.open_issues_count > 5 %}
  [![Issues](https://img.shields.io/badge/issues-{{ repository.open_issues_count }}-red.svg)](https://github.com/{{ repository.full_name }}/issues)
{% elsif repository.open_issues_count > 0 %}
  [![Issues](https://img.shields.io/badge/issues-{{ repository.open_issues_count }}-orange.svg)](https://github.com/{{ repository.full_name }}/issues)
{% else %}
  [![Issues](https://img.shields.io/badge/issues-{{ repository.open_issues_count }}-brightgreen.svg)](https://github.com/{{ repository.full_name }}/issues)
{% endif %}
  [![Tag](https://img.shields.io/github/tag/{{ repository.full_name }}.svg)](https://github.com/{{ repository.full_name }}/tags)
  [![Stars](https://img.shields.io/badge/stars-{{ repository.stargazers_count }}-blue.svg)](https://github.com/{{ repository.full_name }}/stargazers)
  [![Forks](https://img.shields.io/badge/forks-{{ repository.forks_count }}-blue.svg)](https://github.com/{{ repository.full_name }}/network)
{% endfor %}
