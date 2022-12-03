# Limitations

### Huddu is not built for speed
A request made via the connect API (which is used when you use one of the SDKs) can take up to 350ms.
That's partly due to the fact that there are most likely a few cold-starts happening on the backend but also that data is not necessarily stored in one centralized place but rather across a lot of different buckets without caching happening.