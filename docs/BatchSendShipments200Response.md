# Zippendo::BatchSendShipments200Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **results** | [**Array&lt;BatchSendShipments200ResponseResultsInner&gt;**](BatchSendShipments200ResponseResultsInner.md) | Per-shipment outcome (one entry per unique requested shipment id). |  |
| **summary** | [**BatchSendShipments200ResponseSummary**](BatchSendShipments200ResponseSummary.md) |  |  |

## Example

```ruby
require 'zippendo'

instance = Zippendo::BatchSendShipments200Response.new(
  results: null,
  summary: null
)
```

