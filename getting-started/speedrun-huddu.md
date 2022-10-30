# Speedrun Huddu

Have a project you want to monitor using Huddu? This is the right place! If you get stuck at any point please feel free to join our community&#x20;

{% content-ref url="../other/community.md" %}
[community.md](../other/community.md)
{% endcontent-ref %}

#### First, let's get a few basic things out of the way:

1. Create an account at [https://huddu.io/](https://huddu.io/) and go to the dashboard
2. Create a fresh project (make sure to give it a memorable name)
3. In the project create a new stream
4. Once you open the stream, you will get the option to create a new token or pick an old one; For this example create a new token scoped to the project.
5. After creating the token make sure to copy it by clicking the **show** button on the tokens page

[✨](https://emojipedia.org/sparkles/) Wonderful, that's half the job!

{% embed url="https://www.loom.com/share/2bf3d5636ef748c5aa2511e7856682fc" %}

#### Implementing Code

Next, we need to publish our events via the Huddu API. The following shows an example of doing so using Python, if you're using a different language, please check the SDKs page.

1. Let's create a client and set a few variables

```python
from huddu import ApiClient
cl = ApiClient("<api_token>")

project_id = "<project_id>"  
stream_id = "<stream_id>"  
account_id = "<account_id>"  
event_id = "<event_id>"  
```

2\. Let's now create 10 events containing some data

```python
for i in range(0,10):
        res = client.Events.create(
                account=account_id,
                project=project_id,
                stream=stream_id,
                data="some data; run"+i,
            )
        )
```

#### Getting the data again

Lets now attempt to retrieve the data we sent again.

```python
print(
    client.Events.search(
        project=project_id,
        account=account_id,
        stream=stream_id,
        query={"data": {"$regex": "some data;"}},
    )
)
```

If you just want to retrieve the latest entries you could also just use the Events.list method however, this way we can filter our results as well.



Not sure how to make things work? Ask in the community.

{% content-ref url="../other/community.md" %}
[community.md](../other/community.md)
{% endcontent-ref %}
