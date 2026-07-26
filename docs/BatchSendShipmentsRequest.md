# Zippendo::BatchSendShipmentsRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **shipment_ids** | **Array&lt;String&gt;** | IDs of the shipments to book. Each must be in &#x60;pending&#x60; or &#x60;error&#x60; status; duplicates are ignored. Max 100 per request. |  |

## Example

```ruby
require 'zippendo'

instance = Zippendo::BatchSendShipmentsRequest.new(
  shipment_ids: [&quot;shp_01H8XABC123&quot;,&quot;shp_01H8XDEF456&quot;]
)
```

