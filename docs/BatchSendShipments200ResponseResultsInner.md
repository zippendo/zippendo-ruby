# Zippendo::BatchSendShipments200ResponseResultsInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **shipment_id** | **String** | The shipment this result refers to. |  |
| **status** | **String** | Whether this shipment was successfully booked with its carrier. |  |
| **code** | **String** | Canonical machine-readable error code, present when &#x60;status&#x60; is &#x60;failed&#x60;. | [optional] |
| **message** | **String** | Human-readable failure detail, present when &#x60;status&#x60; is &#x60;failed&#x60;. | [optional] |
| **errors** | [**Array&lt;SendShipment422ResponseErrorsInner&gt;**](SendShipment422ResponseErrorsInner.md) | Carrier-specific errors, present when the carrier rejected the booking. | [optional] |

## Example

```ruby
require 'zippendo'

instance = Zippendo::BatchSendShipments200ResponseResultsInner.new(
  shipment_id: shp_01H8XABC123,
  status: sent,
  code: CARRIER_ERROR,
  message: Shipment must be in pending or error status to be sent,
  errors: null
)
```

