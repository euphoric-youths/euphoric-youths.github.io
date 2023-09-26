---
layout: home
---

![EY banner](assets/images/banner.png)

<div class="album-shelf">
    {% for album in site.data.albums %}
    <div class="album-container">
        <img src="{{ album.cover }}" alt="{{ album.name }}">
        <div class="album-mask">
            <div class="album-text">{{ album.name }}</div>
            <!-- The social buttons are stolen from the bottom bar -->
            <ul class="social-media-list">
                {% for platform in album.platforms %}
                <li>
                    <a href="{{ platform.url }}" target="_blank" title="{{ platform.name }}" style="background-color:black;opacity:0.5">
                        <svg class="svg-icon grey"><use xlink:href="/assets/minima-social-icons.svg#{{ platform.name }}" /></svg>
                    </a>
                </li>
                {% endfor %}
            </ul>
        </div>
    </div>
    {% endfor %}
</div>
