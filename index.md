---
layout: home
title: 欢迎
subtitle: 探索技术与艺术的边界
---

你好，我是 **Taurus Kong**。我在这里分享：

- 游戏美术管线 (Pipeline) 开发心得
- Houdini 程序化生成 (PCG) 研究
- DCC 工具链与自动化实践

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
