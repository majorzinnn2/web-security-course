---
layout: default
nav_order: 1
---
# Sobre o Curso

{{ site.description }}

---

## Relatórios dos Alunos

<ul>
  {% for post in site.posts %}
    <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a> - <em>por {{ post.author }} em {{ post.date | date: "%d/%m/%Y" }}</em></li>
  {% endfor %}
</ul>

---
[Entre em contato]({% link contato.md %})
