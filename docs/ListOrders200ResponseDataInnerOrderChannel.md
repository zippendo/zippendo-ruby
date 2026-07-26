# Zippendo::ListOrders200ResponseDataInnerOrderChannel

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Order channel ID. |  |
| **name** | **String** | Order channel name. |  |
| **type** | **String** | Type of the order channel (sales platform). |  |

## Example

```ruby
require 'zippendo'

instance = Zippendo::ListOrders200ResponseDataInnerOrderChannel.new(
  id: clz9k2f0a0001abcd1234efgh,
  name: Anna&#39;s Shopify Store,
  type: shopify
)
```

