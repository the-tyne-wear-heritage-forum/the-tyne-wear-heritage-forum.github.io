---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

<div class="parallax-container">
    <div class="parallax">
    <h1>Case Studies</h1>
    <img src="/assets/img/litphil.webp">    
    </div>
</div>

<div class="content-body">
        <p style="text-align:center;margin-bottom:30px;">Below you will find several example case studies of the Forum's work and impact:</p>
        {% for study in site.casestudies %}
            <a href="{{ study.url }}">
            <div class="box">
                <div class="boxInner">
                <img src="{{ study.image }}" alt="Image for {{study.title}}">
                <div class="titleBox">{{ study.title }}</div>
                </div>
            </div>
            </a>
        {% endfor %}
</div>