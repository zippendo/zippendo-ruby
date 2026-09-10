# Zippendo::GetOrder200ResponseShipmentsInnerParcelsInnerOrderLinesInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Parcel content line ID. |  |
| **sku** | **String** | SKU of the packed item. | [optional] |
| **quantity** | **Integer** | Quantity packed in this parcel. |  |
| **description** | **String** | Product description. | [optional] |

## Example

```ruby
require 'zippendo'

instance = Zippendo::GetOrder200ResponseShipmentsInnerParcelsInnerOrderLinesInner.new(
  id: ol_9c1d2e3f,
  sku: SKU-1042-BLK,
  quantity: 2,
  description: Wool Sweater
)
```

