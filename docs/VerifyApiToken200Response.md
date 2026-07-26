# Zippendo::VerifyApiToken200Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **valid** | **Boolean** | Whether the token is valid |  |
| **token_id** | **String** | Token identifier | [optional] |
| **user_id** | **String** | User identifier the token belongs to | [optional] |
| **org_id** | **String** | Organization identifier the token belongs to | [optional] |
| **scopes** | **Array&lt;String&gt;** | Permission scopes granted by the token | [optional] |
| **expires_at** | **String** | Expiry timestamp (ISO 8601), null if it never expires | [optional] |

## Example

```ruby
require 'zippendo'

instance = Zippendo::VerifyApiToken200Response.new(
  valid: true,
  token_id: tok_6e2fa83ij9,
  user_id: usr_9f3kd92ld0,
  org_id: org_4d8af01qw2,
  scopes: [&quot;read:shipments&quot;],
  expires_at: 2026-09-20T14:30:00.000Z
)
```

