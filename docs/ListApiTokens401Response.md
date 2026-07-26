# Zippendo::ListApiTokens401Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **code** | **String** | Machine-readable error code (translate by this on the client) | [optional] |
| **error** | **String** | Short human title |  |
| **message** | **String** | Human-readable English detail (i18n fallback) |  |

## Example

```ruby
require 'zippendo'

instance = Zippendo::ListApiTokens401Response.new(
  code: CARRIER_GLS_WRONG_ADDRESS,
  error: Bad Request,
  message: Failed to create address
)
```

