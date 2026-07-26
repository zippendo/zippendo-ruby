# Zippendo::BatchSplitShipmentRequestShipmentsInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **reference** | **String** | Reference for this new shipment. Defaults to original reference with a suffix. | [optional] |
| **order_lines** | [**Array&lt;BatchSplitShipmentRequestShipmentsInnerOrderLinesInner&gt;**](BatchSplitShipmentRequestShipmentsInnerOrderLinesInner.md) | Order lines and quantities to move into this new shipment. |  |

## Example

```ruby
require 'zippendo'

instance = Zippendo::BatchSplitShipmentRequestShipmentsInner.new(
  reference: ORDER-1042-split-1,
  order_lines: null
)
```

