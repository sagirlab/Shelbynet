API Keys
API keys are how your resource identifies itself to us for authentication and rate limiting purposes. If you do not use an API key, your client will be considered “anonymous” and subject to significantly lower rate limits. You can learn how to attach an API key to your requests by using the snippets on the detail page of any resource.

As a general rule, you should only have one API key at a time per resource. Geomi lets you create multiple keys for a single resource purely to enable key rotation in case a key is leaked.

Client Usage
The allowed URLs / extension IDs feature is only an optimistic protection, it is possible for a bad actor to send requests with any Origin header value outside from outside of a browser context. Like most other infrastructure services with API keys, it is ultimately up to you to protect your API keys. Make sure to set an appropriate per IP limit and a daily / monthly budget to control your spend.

We have ideas here that could make it easier to use frontend keys. If you’d like to discuss these features, or have ideas of your own, please reach out, we’d love to discuss them.

When creating a new API key you will be prompted to decide whether it is intended for client usage or not. Client usage implies any context where the API key is exposed to the public, e.g. a dapp, a mobile app, or a browser extension. If you will only use the API key in a private, backend context, you do not need to worry about this.

If you select “Client Usage” you will be prompted to provide a set of approved URLs and/or extension IDs. We will confirm that the Origin of the request matches one of the approved URLs or extension IDs.

When using a client key you can configure per-IP rate limit rules. These rules let you control how many requests each individual IP address can make, helping prevent abuse from any single user of your application. You can create up to 6 rules per key, with each rule targeting different scopes (all requests, specific upstreams, specific operations, etc.).

Learn more about per-IP rate limit rules and billing and system limits.

Key Types
To help you manage your keys correctly, you’ll notice that keys intended for client usage have a different format than keys intended for backend usage:

Server: Used from a private backend. Keep these secret. Example: aptoslabs_aXjFX8fDdZv_AXMynDZvp711WTBpSBmqLyj12RV9RFA6B
Client: Used from a public frontend. We perform additional checks and analytics to ensure the use of these IDs is authentic. Example: AG-FL4PYMZ1YX1LGAJCWP2R1ACYTYRCBY1GB
Anonymous Requests
Certain Geomi services (e.g. the node and indexer APIs) allow unauthenticated requests, also known as anonymous requests. When no key is provided, ratelimiting is applied on a per-IP per-origin basis. Anonymous limits are significantly lower than authenticated limits.