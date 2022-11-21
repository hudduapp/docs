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


store =Store(
    token="<auth_token>", # how to obtain? see above
    collection="<collection_identifier>", # how to obtain? see above
    region="<region>" # how to obtain? see above
)
```
{% endtab %}

{% tab title="Second Tab" %}

{% endtab %}
{% endtabs %}
