# Zippendo::ListApiTokens200ResponseDataInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Unique API token identifier |  |
| **name** | **String** | Token name for identification |  |
| **token_prefix** | **String** | First 12 chars of the token for identification |  |
| **scopes** | **Array&lt;String&gt;** | Permission scopes granted by the token |  |
| **last_used_at** | **String** | Timestamp the token was last used (ISO 8601), null if never used |  |
| **expires_at** | **String** | Expiry timestamp (ISO 8601), null if it never expires |  |
| **created_at** | **String** | Creation timestamp (ISO 8601) |  |
| **created_by** | [**ListApiTokens200ResponseDataInnerCreatedBy**](ListApiTokens200ResponseDataInnerCreatedBy.md) |  |  |

## Example

```ruby
require 'zippendo'

instance = Zippendo::ListApiTokens200ResponseDataInner.new(
  id: tok_6e2fa83ij9,
  name: Warehouse integration,
  token_prefix: zipp_live_8f,
  scopes: [&quot;read:shipments&quot;,&quot;write:shipments&quot;],
  last_used_at: 2026-06-22T14:30:00.000Z,
  expires_at: 2026-09-20T14:30:00.000Z,
  created_at: 2026-06-22T14:30:00.000Z,
  created_by: null
)
```

