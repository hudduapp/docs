# SDK

The Huddu SDK is the simplest way to create key, value pairs on Huddu. As of now only one language (namely python) is supported with plans for nodejs and java to follow suit soon!

Any languages to add to that list? Tell us in a [community channel!](../other/community.md)

## Installation

{% tabs %}
{% tab title="Python" %}
```
pip install huddu
```

{% hint style="info" %}
It's great practice to keep all your requirements in a requirements.txt file!
{% endhint %}
{% endtab %}
{% endtabs %}

## Initiating the SDK

First, we need a few variables (namely a **collection token** and a **collection identifier**).

1. To obtain the collection token open a collection and switch to the **Authorization tab** and press the **Create Token** button.
2. Getting our collection identifier is simpler. We just need to press the **Connect** button in the top right corner. This will open a drawer that displays our collection identifier.
3. In the same drawer, you will find the region identifier. (in future versions of the sdk you won't have to specify this)

{% tabs %}
{% tab title="Python" %}
```python
from huddu import Store


store = Store(
    token="<auth_token>", # how to obtain? see above
    collection="<collection_identifier>", # how to obtain? see above
    region="<region>" # how to obtain? see above
)
```
{% endtab %}
{% endtabs %}

## Adding data

The Store class offers the following methods:

* .get() - Get one entry by identifier
* .put() - Create a new entry
* .delete() - delete one entry
* .update() - override an existing entry with new data
* .fetch() - List entry items with a set limit and skip or even by identifier.

## Get

{% tabs %}
{% tab title="Python" %}
```python
store.get(
    id: str,
    start: int = None,
    end: int = None,
)
```
{% endtab %}
{% endtabs %}

### Parameters:

* id: the entry identifier
* start: the line after which the content of the entry should be returned (optional)
* end: the line before which the content of the entry should be returned (optional)

## Put

{% tabs %}
{% tab title="Python" %}
```python
store.put(
    id: str,
    data: str, 
    safe: bool = True
)
```
{% endtab %}
{% endtabs %}

## Parameters:

* id: the entry identifier
* data: the entry data
* safe: if true will check if an entry with the identifier already exists to prevent overriding it. (optional)

## Delete

{% tabs %}
{% tab title="Python" %}
```python
store.delete(
    id: str
)
```
{% endtab %}
{% endtabs %}

## Parameters

* id: the entry identifier

## Update

{% tabs %}
{% tab title="Python" %}
```python
store.update(
    id: str,
    data: str
)
```
{% endtab %}
{% endtabs %}

## Parameters

* id: the entry identifier
* data: the entry data

## Fetch

{% tabs %}
{% tab title="Python" %}
```python
store.fetch(
    ids: List[str] = None,
    skip: int = 0,
    limit: int = 25,
    start: int = None,
    end: int = None,
)
```
{% endtab %}
{% endtabs %}

### Parameters

* ids: List of ids to query (optional)
* skip: Number of items to skip from results (defaults to 0)
* limit: Number of items to limit to from results (defaults to 25)
* start: the line after which the content of the entry should be returned (optional)
* end: the line before which the content of the entry should be returned (optional)
