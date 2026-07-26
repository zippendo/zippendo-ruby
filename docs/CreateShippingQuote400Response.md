# Zippendo::CreateShippingQuote400Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **error** | **String** | Error type |  |
| **message** | **String** | Human-readable error message |  |

## Example

```ruby
require 'zippendo'

instance = Zippendo::CreateShippingQuote400Response.new(
  error: Bad Request,
  message: Invalid destination country
)
```

