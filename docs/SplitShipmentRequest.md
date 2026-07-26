# Zippendo::SplitShipmentRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **parcel_id** | **String** | Parcel whose order lines are split into a new shipment. |  |
| **order_line_ids** | **Array&lt;String&gt;** | Order line IDs to move. If omitted, all order lines in the parcel are moved. | [optional] |
| **carrier_id** | **String** | Carrier for the new shipment. Copied from the original if omitted. | [optional] |
| **product_id** | **String** | Carrier product for the new shipment. Copied from the original if omitted. | [optional] |
| **services** | **Array&lt;String&gt;** | Service codes for the new shipment. Copied from the original if omitted. | [optional] |
| **additional_parameters** | **Hash&lt;String, Object&gt;** | Carrier-specific parameters for the new shipment. | [optional] |
| **reference** | **String** | Reference for the new shipment. Defaults to the original reference with a suffix. | [optional] |

## Example

```ruby
require 'zippendo'

instance = Zippendo::SplitShipmentRequest.new(
  parcel_id: prc_5a6b7c8d,
  order_line_ids: [&quot;ol_9c1d2e3f&quot;],
  carrier_id: car_pn_001,
  product_id: prod_mypack_home,
  services: [&quot;A7&quot;],
  additional_parameters: {&quot;notificationEmail&quot;:&quot;anna@example.dk&quot;},
  reference: ORDER-1042-split
)
```

