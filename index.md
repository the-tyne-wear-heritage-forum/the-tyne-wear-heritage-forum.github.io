---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

<div class="parallax-container">
    <div class="parallax">
    <h1 class="parallax-header">The Tyne & Wear Heritage Forum</h1>
    <img src="/assets/img/fenwick.webp">    
    </div>
</div>

<div class="content-body">
    <div class="section">
    <p>The Tyne & Wear Heritage Forum was formed in 2015 by representatives of local
    heritage groups active within the North-East of England. These groups celebrate
    the period of industrialization associated with Tyne & Wear, County Durham and
    Northumberland, when the region was at the forefront of world development during
    the period of the industrial revolution.</p>
    <p>The TWHF is an alliance of key heritage bodies and individuals active within the
    North-East of England. At a time of restricted public funding for protection and
    preservation of heritage, the Forum seeks to make a tangible and significant
    impact on the regional environment to the benefit of those who live and work
    here.</p>
    <p>Through the <em>HeritageAct!</em> initiative, we aim to help local heritage groups and individuals learn the skills required to develop, finance and deliver heritage conservation and interpretation. Visit the <a href="/heritageAct"><em>HeritageAct!</em> page</a> for more information and see some of the projects that we've worked on.</p>
    </div>
    <div class="section">
        <div class="latest-blog">
            <h3>Latest Blog Post</h3>
            {% for post in site.posts limit:1 %}
                <h4 class="preview-title">{{post.title}}</h4>
                <p class="preview-detail">{{post.author}} | {{post.date | date: "%-d %B %Y"}}</p>
                <p>{{post.excerpt}}</p>
                <p><a href="{{ post.url }}">Read more</a> &middot; <a href="/blog">View all posts</a> </p>
            {% endfor %}
        </div>
        <div class="twitter-feed">
            <h3>Latest Tweet</h3>
            <a class="twitter-timeline" href="https://twitter.com/TWHeritageForum" 
                    data-chrome="noheader nofooter noborders transparent noscrollbar" 
                    data-tweet-limit="1" dnt="true">Tweets by Tyne & Wear Heritage Forum</a>
                    <script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>
                    <br/>
                    <br/>
        </div>
    </div>
    <div class="section"></div>
</div>

