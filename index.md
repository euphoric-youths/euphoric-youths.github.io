---
layout: home
---

![EY banner](assets/images/EY_banner.png)

<div class="album-shelf">
    {% for album in site.data.albums %}
    <div class="album-container">
        <img src="{{ album.cover }}" alt="{{ album.name }}">
        <div class="album-mask">
            <div class="album-text">{{ album.name }}</div>
            <ul class="social-media-list">
                {% for platform in album.platforms %}
                <li>
                    <a rel="me" href="{{ platform.link }}" target="_blank" title="{{ platform.name }}" class="button">
                        <svg class="svg-icon white">
                            <use xlink:href="/assets/minima-social-icons.svg#{{ platform.name }}"></use>
                        </svg>
                    </a>
                </li>
                {% endfor %}
            </ul>
        </div>
    </div>
    {% endfor %}
</div>
