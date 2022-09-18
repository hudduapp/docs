# Code

Getting Huddu installed in your project is fairly straightforward.

This quick tutorial will explain the installation required when using the python programming language. For guides on how to get started with a different language please consult the SDKs section of our documentation.

{% content-ref url="broken-reference" %}
[Broken link](broken-reference)
{% endcontent-ref %}

### Installing the dependency

First, we need to install the [huddu-python](https://github.com/hudduapp/huddu-python) SDK via the GitHub repository.

`pip install git+`[`https://github.com/hudduapp/huddu-python.git#egg=huddu`](https://github.com/hudduapp/huddu-python.git#egg=huddu)``

or depending on your setup:

`pip3 install git+`[`https://github.com/hudduapp/huddu-python.git#egg=huddu`](https://github.com/hudduapp/huddu-python.git#egg=huddu)``

### Writing our first logic with huddu-python

First things first, we have to import the `huddu-python` SDK like so:

```python
from huddu import ApiClient
```

Next, let's initialize the huddu client:&#x20;

```python
_huddu_client = ApiClient(
    "<project_id>", # the project identifier can be found on the dashboard 
    "<stream_name>" # the same goes for the stream name
)
```



For this example, we will simply write 10 events to the ingest API, each containing markdown content. So let's do that!

```python
for i in range(0,9):
    _huddu_client.report(
    "demo_event", # this is the name of our event under which entries will be displayed on the dashboard
    data={
            "markdown": f"#Dummy Event\n reporting this event for the {i}th time!"
        }
    )
    
```

### Moving on

if you want to see some more in-depth examples you can check the huddu-python GitHub repository under the examples folder ([here](https://github.com/hudduapp/huddu-python/tree/main/examples)).

If you need any further support feel free to ask on our [discord](https://discord.gg/JFW7dyNXpW)!
