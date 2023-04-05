{% for i in include.content %}

<a href="i.link"><svg aria-labelledby="{{ i.id }}" role="img"><title id="{{ i.id }}">{{ i.alt_text }}</title><use xlink:href="/assets/img/sprite.svg#{{ i.sprite }}"></use></svg> </a>

{% endfor %}