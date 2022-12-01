---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
---


<section id="intro">
    <div class="flex-row-between">
        <h1>cyb3r.sh</h1>
        <button id="theme-toggle" onclick="modeSwitcher()">
            <div></div>
        </button>
    </div>
    <div class="bio">
    <p>
      playful computing as interpreted by brandon james
    </p>
    <p>
	<a href="{{ site.url }}{{ site.baseurl }}/about/">> About me</a>
    </p>
    </div>
</section>

<section class="posts">
    <h3>BLOG</h3>
    <ul>
        {% for post in site.posts %}
        <li>
            <a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a>
            <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%b %d, %Y" }}</time></li>
        {% endfor %}
    </ul>
