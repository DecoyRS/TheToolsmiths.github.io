---
layout: codex_page
title: Articles and Web Pages on the topic of Miscellaneous Stuff
short_title: Miscellaneous
permalink: /codex/tool_development_resources/articles/miscellaneous
codex_page_type: lvl4
nav_tag: dev_resources
lvl3_nav_tag: resources_web_articles
---

<!-- To Edit or Add content to this page please edit the _data/article.yaml file -->
{% assign article_topics = site.data.article_links | sort: 'topic_name' %}

{% for topic in article_topics %}

	{% if topic.topic_name == "miscellaneous" %}

		{% assign articles = topic.articles | sort: 'caption' %}
		{% for article in articles %}

<h4><a href="{{article.url}}">{{article.caption}}</a></h4>
			{% if article.pic_url %}
<p><img src="{{article.pic_url}}" alt="{{article.pic_caption}}"></p>
			{% endif %}

			{% if article.author %}
<h5>by {{article.author}}</h5>
			{% endif %}
<hr>

		{% endfor %}
	{% endif %}
{% endfor %}