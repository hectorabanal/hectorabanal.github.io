---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
title: Home
order: 1
---

<div class="home">
    <h1 class="page-heading">{{ site.title }}</h1>
    <p class="page-description">{{ site.description }}</p>

    <div class="home__posts">
        <h2>Últimos post</h2>
        <ul>
            {% for post in site.posts %}
                <li>
                    <h3>
                        <a class="post-link" href="{{ post.url | relative_url }}">
                        {{ post.title | escape }}
                    </h3>
                    <span class="post-meta">{{ post.date | date: "%b %-d, %Y "}}</span>
                </li>
            {% endfor %}
        </ul>
    </div>
</div>