# Zippendo::SendShipment422Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **code** | **String** | Machine-readable error code. | [optional] |
| **error** | **String** | Error category. |  |
| **message** | **String** | Human-readable summary of the carrier failure. |  |
| **errors** | [**Array&lt;SendShipment422ResponseErrorsInner&gt;**](SendShipment422ResponseErrorsInner.md) | Detailed carrier errors that caused the booking to fail. |  |

## Example

```ruby
require 'zippendo'

instance = Zippendo::SendShipment422Response.new(
  code: CARRIER_GLS_WRONG_ADDRESS,
  error: Carrier Error,
  message: Shipment could not be booked with PostNord.,
  errors: null
)
```

