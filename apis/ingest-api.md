# Ingest API

This API is used to create events. It can be used with or without authentication (this can be changed via the dashboard).

&#x20;

#### POST /\<project\_id>/\<stream\_id>

{% swagger src="../.gitbook/assets/ingest.json" path="/{project_id}/{stream_id}" method="post" %}
[ingest.json](../.gitbook/assets/ingest.json)
{% endswagger %}

#### Notes:

#### Body:

data: This field can be any valid json datatype (integer, string, map, array, ...)

batch: This field is basically the same as the data field but for multiple entries

#### Headers:

If auth is required via the dashboard an auth token is required

Note that a **Content-Length** header is required, otherwise the request will be rejected.

