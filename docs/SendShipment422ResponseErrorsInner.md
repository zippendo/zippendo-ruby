# Zippendo::SendShipment422ResponseErrorsInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **code** | **String** | Carrier-specific error code. | [optional] |
| **message** | **String** | Carrier-specific error message. |  |

## Example

```ruby
require 'zippendo'

instance = Zippendo::SendShipment422ResponseErrorsInner.new(
  code: INVALID_POSTAL_CODE,
  message: Receiver postal code is invalid for the selected product.
)
```

