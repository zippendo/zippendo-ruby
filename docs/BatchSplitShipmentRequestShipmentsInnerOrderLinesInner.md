# Zippendo::BatchSplitShipmentRequestShipmentsInnerOrderLinesInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Order line identifier to move. |  |
| **quantity** | **Integer** | Quantity of the order line to move. |  |

## Example

```ruby
require 'zippendo'

instance = Zippendo::BatchSplitShipmentRequestShipmentsInnerOrderLinesInner.new(
  id: ol_9c1d2e3f,
  quantity: 1
)
```

