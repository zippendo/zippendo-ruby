# Zippendo::CreateShippingQuoteRequestItemsInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** | Item name |  |
| **sku** | **String** | SKU identifier | [optional] |
| **quantity** | **Integer** | Quantity |  |
| **grams** | **Float** | Weight in grams |  |
| **price** | **Float** | Price in cents |  |
| **product_id** | **String** | Product ID | [optional] |
| **variant_id** | **String** | Variant ID | [optional] |

## Example

```ruby
require 'zippendo'

instance = Zippendo::CreateShippingQuoteRequestItemsInner.new(
  name: Uld trøje,
  sku: SKU-1001,
  quantity: 2,
  grams: 500,
  price: 29900,
  product_id: prod_01HZX9K2QF,
  variant_id: var_01HZX9K2QF
)
```

