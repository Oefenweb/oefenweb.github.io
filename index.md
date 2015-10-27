---
title: Oefenweb open-source software
---

# Oefenweb open-source software

{% for repository in site.github.public_repositories %}
* [{{ repository.name }}]({{ repository.html_url }}) - {{ repository.description }}<br />
  [![Build Status](https://img.shields.io/travis/{{ repository.full_name }}.svg)](https://travis-ci.org/{{ repository.full_name }})
{% if repository.open_issues_count > 5 %}
{% assign badge_color = 'red' %}
{% elsif repository.open_issues_count > 0 %}
{% assign badge_color = 'orange' %}
{% else %}
{% assign badge_color = 'brightgreen' %}
{% endif %}
  [![Issues](https://img.shields.io/badge/issues-{{ repository.open_issues_count }}-{{ badge_color }}.svg)](https://github.com/{{ repository.full_name }}/issues)
  [![Tag](https://img.shields.io/github/tag/{{ repository.full_name }}.svg)](https://github.com/{{ repository.full_name }}/tags)
  [![Stars](https://img.shields.io/badge/stars-{{ repository.stargazers_count }}-blue.svg)](https://github.com/{{ repository.full_name }}/stargazers)
  [![Forks](https://img.shields.io/badge/forks-{{ repository.forks_count }}-blue.svg)](https://github.com/{{ repository.full_name }}/network)
{% endfor %}
