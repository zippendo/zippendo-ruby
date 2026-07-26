# Zippendo::GetOrder200ResponseShipmentsInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Unique shipment identifier. |  |
| **reference** | **String** | Customer-facing shipment reference. |  |
| **status** | **String** | Lifecycle status of the shipment. |  |
| **type** | **String** | Direction of the shipment relative to the organization. |  |
| **tracking** | [**CreateShipment201ResponseTracking**](CreateShipment201ResponseTracking.md) |  | [optional] |
| **carrier_settings** | [**ListShipments200ResponseDataInnerCarrierSettings**](ListShipments200ResponseDataInnerCarrierSettings.md) |  |  |
| **created_at** | **String** | Timestamp when the shipment was created. |  |
| **updated_at** | **String** | Timestamp when the shipment was last updated. |  |
| **shipping_rule_id** | **String** | ID of the shipping rule used for this shipment. | [optional] |
| **documents** | [**Array&lt;CreateShipment201ResponseDocumentsInner&gt;**](CreateShipment201ResponseDocumentsInner.md) | Documents (labels, customs forms) for this shipment. | [optional] |

## Example

```ruby
require 'zippendo'

instance = Zippendo::GetOrder200ResponseShipmentsInner.new(
  id: shp_4d9e7a2f,
  reference: ORDER-1042,
  status: pending,
  type: outbound,
  tracking: null,
  carrier_settings: null,
  created_at: 2026-06-22T14:30:00.000Z,
  updated_at: 2026-06-22T14:30:00.000Z,
  shipping_rule_id: clz9k2f0a0002abcd5678ijkl,
  documents: null
)
```

