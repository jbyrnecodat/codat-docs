---
title: "Use the Chargify integration"
description: "When an SMB user has linked their Chargify account, access their subscriptions and billing data by making proxy requests to the Chargify API"
createdAt: "2022-08-08T15:57:27.458Z"
updatedAt: "2022-10-19T16:29:45.213Z"
---

The Chargify integration is part of the [Domain discovery program](/domain-discovery-program), so Codat doesn't yet expose standardized data types or provide any data visualization or metrics (for example, in Assess).

Instead, when an SMB customer (a company) has [linked their Chargify account](/commerce-chargify-setup), you can access their subscriptions and billing data through the `proxy` endpoint in the Codat API. Only GET requests are currently supported.

## Send a proxy request

To proxy to the Chargify API, send a GET request to the `proxy` endpoint:

```
GET /companies/COMPANY_ID/connections/CONNECTION_ID/data/proxy?endpoint=CHARGIFY_ENDPOINT
```

Replace `CHARGIFY_ENDPOINT` with the desired Chargify API object, which must be URL encoded. For example, use `customers.json` to query a company's list of customers in Chargify.

To view a list of all available endpoints, see the <a className="external" href="https://developers.chargify.com/docs/api-docs/YXBpOjE0MTA4MjYx-chargify-api" target="_blank">Chargify API documentation</a>.

:::caution

Use of the Chargify integration is subject to participation in the Codat [Domain discovery program](/domain-discovery-program). Be aware of the program expectations before using the integration.
:::
