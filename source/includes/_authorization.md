# Authorization

> To authorize you'll need an OAuth token:

```shell
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here"
  -H "Authorization: OAuth thisisyouroauthtoken"

```

> Make sure to replace `thisisyouroauthtoken` with your OAuth API key.

Code School uses API keys to allow access to the API. Email [Olivier](mailto:olivier@codeschool.com) to obtain one.

Code School expects for the API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: OAuth thisisyouroauthtoken`

<aside class="notice">
You must replace `thisisyouroauthtoken` with your personal API key.
</aside>
