---
layout: default
title: 项目
permalink: /projects/
---

{% assign projects = site.projects | sort: "date" | reverse %}

这里展示了我参与开发的技术美术工具与 PCG 案例：

<ul>
{% for project in projects %}
	<li>
		<h3><a href="{{ project.url | relative_url }}">{{ project.title }}</a></h3>
		<p>{{ project.summary | default: project.excerpt | strip_html }}</p>
		{% if project.tags %}<p>标签：{{ project.tags | join: ", " }}</p>{% endif %}
		{% if project.links %}
			<p>
				{% if project.links.repo %}<a href="{{ project.links.repo }}" target="_blank">源码</a>{% endif %}
				{% if project.links.demo %} · <a href="{{ project.links.demo }}" target="_blank">演示</a>{% endif %}
			</p>
		{% endif %}
	</li>
{% endfor %}
</ul>
