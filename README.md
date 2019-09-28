# Welcome to Scots Dev

Community maintained repo for collating lists of events, meetups, conferences, slack groups and organisations working in technology across Scotland.

{% for region in site.data.events %}
    ## {{region.name}}

    {% if region.conferences %}
        ### Conferences

        {% event in region.conferences %}
            * [{{event.name}}]({{event.link}})
        {% endfor %}
    {% endif %}

    {% if region.meetups %}
        ### Meetups

        {% event in region.meetups %}
            * [{{event.name}}]({{event.link}})
        {% endfor %}
    {% endif %}

    {% if region.slack %}
        ### Slack Teams

        {% event in region.slack %}
            * [{{event.name}}]({{event.link}})
        {% endfor %}
    {% endif %}

    {% if region.misc %}
        ### Other Relevant Links

        {% event in region.misc %}
            * [{{event.name}}]({{event.link}})
        {% endfor %}
    {% endif %}
{% endfor %}

## Somewhere else?

Send us a PR with any locations/events/groups we're missing.
