# Zippendo::CreateApiTokenRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** | Token name for identification |  |
| **scopes** | **Array&lt;String&gt;** | Permission scopes for the token |  |
| **expires_in_days** | **Integer** | Token expiry in days (optional, max 365) | [optional] |

## Example

```ruby
require 'zippendo'

instance = Zippendo::CreateApiTokenRequest.new(
  name: Warehouse integration,
  scopes: [&quot;read:shipments&quot;,&quot;write:shipments&quot;],
  expires_in_days: 90
)
```

