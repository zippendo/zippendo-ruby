# Zippendo::SplitShipmentParcelRequestParcelsInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Existing parcel ID to update. Omit to create a new parcel. | [optional] |
| **order_lines** | [**Array&lt;BatchSplitShipmentRequestShipmentsInnerOrderLinesInner&gt;**](BatchSplitShipmentRequestShipmentsInnerOrderLinesInner.md) | Order lines and quantities to place in this parcel. |  |

## Example

```ruby
require 'zippendo'

instance = Zippendo::SplitShipmentParcelRequestParcelsInner.new(
  id: prc_5a6b7c8d,
  order_lines: null
)
```

