---
layout: page
title: Staff 工作人员
description: A listing of all the course staff members.
---

# Staff 工作人员

<!-- Staff information is stored in the `_staffers` directory and rendered according to the layout file, `_layouts/staffer.html`. -->

## Instructor 教师

{% assign instructors = site.staffers | where: 'role', 'Instructor' %}
{% for staffer in instructors %}
{{ staffer }}
{% endfor %}

{% assign teaching_assistants = site.staffers | where: 'role', 'Teaching Assistant' %}
{% assign num_teaching_assistants = teaching_assistants | size %}
{% if num_teaching_assistants != 0 %}
## Teaching Assistant 助教

{% for staffer in teaching_assistants %}
{{ staffer }}
{% endfor %}
{% endif %}
