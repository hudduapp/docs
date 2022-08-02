# Working with the api

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
|                                     |                     |

