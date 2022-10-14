# Public API / Integrations API

This API can be used to retrieve data from our platform. In order to interface with the public API, you have to create and install a new integration via the developer settings. &#x20;

The following goes through the configuration options for new integrations:

#### Configuring an integration

When clicking on the _+ Create Integration_ button in your developer settings you should see the following dialog open. The developer settings can be found at [https://app.huddu.io/\_/developers/integrations](https://app.huddu.io/\_/developers/integrations).

<figure><img src="../../.gitbook/assets/SCR-20221014-s1g.png" alt=""><figcaption></figcaption></figure>

The first few fields should be quite self-explanatory. There you can specify a few different options that adjust how the integration will be displayed on the marketplace ([http://huddu.io/marketplace](http://huddu.io/marketplace)).&#x20;

#### Fields

This field specified which variables have to be set by users when installing your integration. You can always retrieve the integration installations via **https://api.huddu.io/installations.**

The following format is **required**:&#x20;

\<field\_name>:\<field\_type>,\<field\_name2>:\<field\_type2>

So a valid example would be:

webhook\__url:text,message_\_color:text
