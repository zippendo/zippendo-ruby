# Zippendo::GetOrder200ResponseShipmentsInnerParcelsInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Parcel ID. |  |
| **weight** | **Float** | Parcel weight in the given unit. |  |
| **weight_unit** | **String** | Unit of measurement for parcel weight. |  |
| **dimensions** | [**CreateShipment201ResponseParcelsInnerDimensions**](CreateShipment201ResponseParcelsInnerDimensions.md) |  |  |
| **order_lines** | [**Array&lt;GetOrder200ResponseShipmentsInnerParcelsInnerOrderLinesInner&gt;**](GetOrder200ResponseShipmentsInnerParcelsInnerOrderLinesInner.md) | Contents of this parcel. |  |

## Example

```ruby
require 'zippendo'

instance = Zippendo::GetOrder200ResponseShipmentsInnerParcelsInner.new(
  id: prc_5a6b7c8d,
  weight: 2.5,
  weight_unit: kg,
  dimensions: null,
  order_lines: null
)
```

