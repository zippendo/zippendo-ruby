# Zippendo::CreateApiTokenRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** | Token name for identification |  |
| **scopes** | **Array&lt;String&gt;** | Permission scopes for the token |  |
| **expires_in_days** | **Integer** | Token expiry in days (optional, max 365) | [optional] |
| **brand_id** | **String** | Restrict this token to a single brand. Requests made with it can only read and write that brand&#39;s data. Omit for organization-wide access. | [optional] |

## Example

```ruby
require 'zippendo'

instance = Zippendo::CreateApiTokenRequest.new(
  name: Warehouse integration,
  scopes: [&quot;read:shipments&quot;,&quot;write:shipments&quot;],
  expires_in_days: 90,
  brand_id: brnd_8f3kd92ld0
)
```

