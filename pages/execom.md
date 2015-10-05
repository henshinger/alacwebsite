---
layout: page
title: "Ateneo Lingua Ars Cultura Executive Committee"
permalink: "/about/execom/"

---

<div>
    {% for member in site.data.execom %}
        {% capture thecycle %}{% cycle 'odd', 'even' %}{% endcapture %}
        
        {% if thecycle == 'odd' %}
        <div class="row" style="margin-bottom: 10px;">
            <div class="medium-6 columns">
                <img src="{{ member.photo }}" alt="{{ member.position }}" style="float:right;width:100%;"/>
            </div>
            <div class="medium-6 columns">
                <h3>{{member.name}}</h3>
                <h5>{{member.course}}</h5>
                <h5>{{member.position}}</h5>
                <a href="https://www.facebook.com/{{member.fblink}}"><i class="fi-social-facebook" style="color:#3a5795;font-size:2em;"></i> {{member.fblink}}</a>
            </div>
        </div>
        {% else %}
        <div class="row" style="margin-bottom:10px;">
            <div class="medium-6 columns" style="text-align:right;">
                <h3>{{member.name}}</h3>
                <h5>{{member.course}}</h5>
                <h5>{{member.position}}</h5>
                <a href="https://www.facebook.com/{{member.fblink}}"><i class="fi-social-facebook" style="color:#3a5795; font-size: 2em;"></i> {{member.fblink}}</a>
            </div>
            <div class="medium-6 columns">
                <img src="{{ member.photo }}" alt="{{ member.position }}" style="float:left;width:100%;"/>
            </div>
        </div>
        {% endif %}
    {% endfor %}
</div>