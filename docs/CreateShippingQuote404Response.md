# Zippendo::CreateShippingQuote404Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **error** | **String** | Error type |  |
| **message** | **String** | Human-readable error message |  |

## Example

```ruby
require 'zippendo'

instance = Zippendo::CreateShippingQuote404Response.new(
  error: Not Found,
  message: Organization not found
)
```

