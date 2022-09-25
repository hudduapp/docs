# Basic example

A component that utilizes the [huddu/markdown](https://huddu.io/marketplace/697468167417722477) component.

It's usually a good practice to pick a and the respective data schema before beginning to push data.

```python
from huddu import ApiClient


_huddu_client = ApiClient(
    "<project_id>",
    "<stream_name>"
)


for i in range(0,5):
    try:
        a==b
    except Exception as e:
        _huddu_client.report("errors", {
            "markdown": f"# Error occurred \n {e}"
        })
        print("Successfully logged error!")
```

This example is hosted on Github at [https://github.com/hudduapp/huddu-python/blob/main/examples/demo.py](https://github.com/hudduapp/huddu-python/blob/main/examples/demo.py)
