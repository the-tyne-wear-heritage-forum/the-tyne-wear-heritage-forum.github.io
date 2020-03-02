---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

<div class="parallax-container">
    <div class="parallax">
    <h1 class="parallax-header">HeritageAct!</h1>
    <img src="/assets/img/charlton.webp">    
    </div>
</div>

<div class="content-body">
        <p style="text-align:center;margin-bottom:30px;"><strong> We launched <em>HeritageAct!</em> at TWHF Conference 2016, with the aim of supporting local groups in developing projects which preserve, share and celebrate the North East's rich heritage.</strong></p>
        <h4>What?</h4>
        <p><em>HeritageAct!</em> is an initiative created by a network of experts and professionals who focus on remains from the industrial age, and provides mentoring and practical support to local heritage groups. We aim to help people learn the skills required to develop, finance and deliver heritage conservation and interpretation.</p>
        <h4>Why?</h4>
        <p>While the region's industrial heritage shaped the lives of many local communities over the course of 250 years, it began to disappear in the 1950s. As a reminder of this key period in the narrative of each community, its surviving features deserve recognition and preservation. We believe that the people living and working within these communities are  ones best placed to share the stories of their own neighbourhoods the impact their local heritage has had upon them.</p>
        <h4>How?</h4>
        <p>We can provide advice and support for heritage and history groups wishing to better understand, protect and improve access to a historic structure or place in their community, as well as mentoring in areas such as project development, understanding significance, conservation, understanding statutory and planning frameworks,applying for funding, setting up a charity, developing partnerships, creating interpretation, learning programmes and more.</p>
        <h4>Get in touch</h4>
        <p>Participation in the <em>HeritageACT!</em> scheme will open up a network of professional and experienced advisors to help you shape your own project. If this sounds good, or if you would like to join our list of project mentors, please get in touch with us at <a href="mailto:info@twhf.co.uk">info@twhf.co.uk</a></p>
        <p style="text-align:center;">Below you will find several example case studies of our work and impact:</p>
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