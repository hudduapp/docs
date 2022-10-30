# Events

{% swagger src="../../.gitbook/assets/api.json" path="/accounts/{account_id}/projects/{project_id}/streams/{stream_id}/events" method="get" %}
[api.json](../../.gitbook/assets/api.json)
{% endswagger %}

{% swagger src="../../.gitbook/assets/api.json" path="/accounts/{account_id}/projects/{project_id}/streams/{stream_id}/events" method="post" %}
[api.json](../../.gitbook/assets/api.json)
{% endswagger %}

{% swagger src="../../.gitbook/assets/api.json" path="/accounts/{account_id}/projects/{project_id}/streams/{stream_id}/events/search" method="post" %}
[api.json](../../.gitbook/assets/api.json)
{% endswagger %}

Note that a query can look something along the ways of this:

objects.field = {"$regex": "value"}

you can use basically any MongoDB query operator

{% swagger src="../../.gitbook/assets/api.json" path="/accounts/{account_id}/projects/{project_id}/streams/{stream_id}/events/{event_id}" method="get" %}
[api.json](../../.gitbook/assets/api.json)
{% endswagger %}

{% swagger src="../../.gitbook/assets/api.json" path="/accounts/{account_id}/projects/{project_id}/streams/{stream_id}/events/{event_id}" method="put" %}
[api.json](../../.gitbook/assets/api.json)
{% endswagger %}
