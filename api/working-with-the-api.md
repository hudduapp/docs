# Working with the api

### Introduction

The API can be found at **https://api.huddu.io**

This is the documentation for our public API which allows users to edit items in an organization

Please note that we offer clientside SKDs in python (and soon nodejs).

{% content-ref url="broken-reference" %}
[Broken link](broken-reference)
{% endcontent-ref %}

If possible we suggest you use the SDKs over accessing the API directly, if you decide to use our API nonetheless you can find documentation generated via the openapi spec in this category.

{% content-ref url="dashboards.md" %}
[dashboards.md](dashboards.md)
{% endcontent-ref %}

{% content-ref url="entries.md" %}
[entries.md](entries.md)
{% endcontent-ref %}

{% content-ref url="series.md" %}
[series.md](series.md)
{% endcontent-ref %}

### Scopes

Tokens can have all different types of scopes that may or may not be required for certain API routes. Here's a short list of scopes and their respective routes:

| Endpoint                            | Scope               |
| ----------------------------------- | ------------------- |
| **Entries**                         |                     |
| POST /entries                       | create\_entry       |
| GET /series/\<series\_id>/entries   | query\_entries      |
| **Dashboards**                      |                     |
| POST /dashboards                    | create\_dashboard   |
| GET /dashboards                     | query\_dashboards   |
| GET /dashboards/\<dashboard\_id>    | retrieve\_dashboard |
| PUT /dashboards/\<dashboard\_id>    | update\_dashboard   |
| DELETE /dashboards/\<dashboard\_id> | delete\_dashboard   |
| **Series**                          |                     |
| POST /series                        | create\_series      |
| GET /series                         | query\_series       |
| GET /series/\<series\_id>           | retrieve\_series    |
| PUT /series/\<series\_id>           | update\_series      |
| DELETE /series/\<series\_id>        | delete\_series      |

