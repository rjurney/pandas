# Team

## Contributors

_pandas_ is made with love by more than [1,500 volunteer contributors](https://github.com/pandas-dev/pandas/graphs/contributors).

If you want to support pandas development, you can find information in the [donations page](../donate.html).

## Maintainers

<div class="row maintainers">
    {% for row in maintainers.people | batch(6, "") %}
        <div class="card-group maintainers">
            {% for person in row %}
                {% if person %}
                    <div class="card">
                        <img class="card-img-top" alt="" src="{{ person.avatar_url }}"/>
                        <div class="card-body">
                            <h6 class="card-title">
                                {% if person.blog %}
                                    <a href="{{ person.blog }}">
                                        {{ person.name or person.login }}
                                    </a>
                                {% else %}
                                    {{ person.name or person.login }}
                                {% endif %}
                            </h6>
                            <p class="card-text small"><a href="{{ person.html_url }}">{{ person.login }}</a></p>
                        </div>
                    </div>
                {% else %}
                    <div class="card border-0"></div>
                {% endif %}
            {% endfor %}
        </div>
    {% endfor %}
</div>

## Governance

Wes McKinney is the Benevolent Dictator for Life (BDFL).

The project governance is available in the [project governance documents](https://github.com/pandas-dev/pandas-governance).

## Code of conduct committee

<ul>
    {% for person in maintainers.coc %}
        <li>{{ person }}</li>
    {% endfor %}
</ul>

## NumFOCUS committee

<ul>
    {% for person in maintainers.numfocus %}
        <li>{{ person }}</li>
    {% endfor %}
</ul>

## Emeritus maintainers

<ul>
    {% for person in maintainers.emeritus %}
        <li>{{ person }}</li>
    {% endfor %}
</ul>
