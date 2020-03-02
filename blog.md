---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

<div class="parallax-container">
    <div class="parallax">
    <h1 class="parallax-header">Blog Posts</h1>
    <img src="/assets/img/blog.webp">    
    </div>
</div>

<div class="content-body">

        <p class="intropara">Interested in writing a blog post about heritage preservation? Drop us an email with your idea at <a href="mailto:tynewearheritageforum@gmail.com">tynewearheritageforum@gmail.com</a>.</p>

        <p class="intropara">All blog posts:</p>
        

        {% for post in site.posts %}
        <div class="event">
            <h4><a href="{{post.url}}">{{ post.title }}</a></h4>
            <p><i>{{post.author}} &middot;
            {% assign d = post.date | date: "%-d"  %}
                {% case d %}
                  {% when '1' or '21' or '31' %}{{ d }}st
                  {% when '2' or '22' %}{{ d }}nd
                  {% when '3' or '23' %}{{ d }}rd
                  {% else %}{{ d }}th
                {% endcase %}
            {{ post.date | date: "%B, %Y" }}            
            </i></p>
            <p>{{post.excerpt}}</p>
            <p><a href="{{post.url}}">Read more...</a></p>
        </div>
        {% endfor %}
</div>