# FAQs

## About Infrastructure

Our infrastructure is primarily but not exclusively hosted on [GCP.](https://cloud.google.com)

## About Tokens / Access keys

As of now, there are two major types of tokens used on the Huddu Platform.

1. **Auth Tokens**: These are issued by our authentication service and offer access for users to the dashboard and to our API. The major use case for them as of now is to authenticate users and later on implement a system for building integrations for the Huddu platform. **You likely don't have to worry about them.**
2. **Collection Tokens**: Collection Tokens are used to perform CRUD operations via the collections API. **** They are directly stored in your collection and cannot be retrieved via this API. **Collection Tokens are the tokens you need to set up if you want to interface with collections via our SDKs.**&#x20;

## Any more questions?

Feel free to ask us!

* [Community](../other/community.md)
