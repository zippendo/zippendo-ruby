# Zippendo::BatchSplitShipmentRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **parcel_id** | **String** | Parcel whose order lines are split across new shipments. |  |
| **shipments** | [**Array&lt;BatchSplitShipmentRequestShipmentsInner&gt;**](BatchSplitShipmentRequestShipmentsInner.md) | New shipments to create from the split parcel. |  |
| **carrier_id** | **String** | Carrier for all new shipments. Copied from the original if omitted. | [optional] |
| **product_id** | **String** | Carrier product for all new shipments. Copied from the original if omitted. | [optional] |
| **services** | **Array&lt;String&gt;** | Service codes for all new shipments. Copied from the original if omitted. | [optional] |
| **additional_parameters** | **Hash&lt;String, Object&gt;** | Carrier-specific parameters for all new shipments. | [optional] |

## Example

```ruby
require 'zippendo'

instance = Zippendo::BatchSplitShipmentRequest.new(
  parcel_id: prc_5a6b7c8d,
  shipments: null,
  carrier_id: car_pn_001,
  product_id: prod_mypack_home,
  services: [&quot;A7&quot;],
  additional_parameters: {&quot;notificationEmail&quot;:&quot;anna@example.dk&quot;}
)
```

