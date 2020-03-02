---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

<div class="parallax-container">
    <div class="parallax">
    <h1 class="parallax-header">Scheduled Events</h1>
    <img src="/assets/img/events.webp">    
    </div>
</div>

<div class="content-body">
        <p class="intropara">Here you will find a list of our upcoming and previous events, such as meetups, conferences and workshops.</p>

        <p class="intropara">Make sure to know as soon as an event is announced: sign up to <a href="/newsletter">our newsletter</a>, or follow us on <a href="https://www.twitter.com/TWHeritageForum">Twitter</a> and <a href="https://www.facebook.com/TWHeritageForum">Facebook</a>!</p>
        
        {% assign sorted = (site.events | sort: 'date') | reverse %}
        {% for event in sorted %}
        <div class="event">
            <h4>{{ event.title }} | 
            {% assign d = event.date | date: "%-d"  %}
            {{ event.date | date: "%H:%M on " }}
                {% case d %}
                  {% when '1' or '21' or '31' %}{{ d }}st
                  {% when '2' or '22' %}{{ d }}nd
                  {% when '3' or '23' %}{{ d }}rd
                  {% else %}{{ d }}th
                {% endcase %}
            {{ event.date | date: "%B, %Y" }}
            </h4>
            <p><i>Venue: {{event.venue}} | Cost: {{event.price}}</i></p>
            <p>{{event.description}} {% if event.eventbrite %}<i><a href="{{event.eventbrite}}" target="_blank">Sign up to attend on EventBrite!</a></i>{% endif %}</p>
        </div>
        {% endfor %}
</div>