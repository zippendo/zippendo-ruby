# Zippendo::BatchSendShipments200ResponseResultsInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **shipment_id** | **String** | The shipment this result refers to. |  |
| **status** | **String** | &#x60;sent&#x60; when the carrier booked it, &#x60;failed&#x60; when the carrier or Zippendo rejected it, and &#x60;skipped&#x60; when the batch ran out of time before reaching it. A &#x60;skipped&#x60; shipment was never sent to the carrier and is safe to submit again. |  |
| **code** | **String** | Canonical machine-readable error code, present when &#x60;status&#x60; is &#x60;failed&#x60; or &#x60;skipped&#x60;. | [optional] |
| **message** | **String** | Human-readable detail, present when &#x60;status&#x60; is &#x60;failed&#x60; or &#x60;skipped&#x60;. | [optional] |
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

