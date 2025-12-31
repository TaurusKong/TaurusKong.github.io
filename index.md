---
layout: home
title: 欢迎
subtitle: 记录我的开发旅程
---

你好，我是 **Taurus Kong**。我在这里分享：

- 近期项目与实践总结
- 自动化、后端开发的笔记
- 阅读、演讲等思考

如果你第一次来，建议从 [关于我](about.md) 开始，再看看 [项目](projects.md) 或最新文章。

---

### 精选项目

{% assign projects = site.projects | sort: "date" | reverse %}
<ul>
{% for project in projects limit:3 %}
	<li>
		<a href="{{ project.url | relative_url }}">{{ project.title }}</a>
		— {{ project.summary | default: project.excerpt | strip_html }}
	</li>
{% endfor %}
</ul>

更多内容请查看 [项目总览](projects.md)。
