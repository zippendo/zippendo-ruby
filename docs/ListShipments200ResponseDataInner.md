# Zippendo::ListShipments200ResponseDataInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Unique shipment identifier. |  |
| **reference** | **String** | Customer-facing shipment reference. |  |
| **type** | **String** | Direction of the shipment relative to the organization. |  |
| **carrier_settings** | [**ListShipments200ResponseDataInnerCarrierSettings**](ListShipments200ResponseDataInnerCarrierSettings.md) |  |  |
| **status** | **String** | Lifecycle status of the shipment. |  |
| **brand_id** | **String** | Brand this record belongs to, or null when it is organization-wide |  |
| **address** | [**ListShipments200ResponseDataInnerAddress**](ListShipments200ResponseDataInnerAddress.md) |  | [optional] |
| **created_at** | **String** | Timestamp when the shipment was created. |  |
| **updated_at** | **String** | Timestamp when the shipment was last updated. |  |

## Example

```ruby
require 'zippendo'

instance = Zippendo::ListShipments200ResponseDataInner.new(
  id: shp_4d9e7a2f,
  reference: ORDER-1042,
  type: outbound,
  carrier_settings: null,
  status: pending,
  brand_id: brnd_8f3kd92ld0,
  address: null,
  created_at: 2026-06-22T14:30:00.000Z,
  updated_at: 2026-06-22T14:30:00.000Z
)
```

