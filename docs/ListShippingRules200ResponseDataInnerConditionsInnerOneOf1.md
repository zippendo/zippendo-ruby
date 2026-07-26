# Zippendo::ListShippingRules200ResponseDataInnerConditionsInnerOneOf1

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** | Condition type discriminator |  |
| **price_type** | **String** | Whether to compare against subtotal (before discounts) or total (after discounts) | [default to &#39;total&#39;] |
| **operator** | **String** | Comparison operator |  |
| **value** | **Float** | Price value to compare against |  |
| **shipping_price** | **Float** | Shipping price when condition matches |  |
| **currency** | **String** | ISO 4217 currency code |  |

## Example

```ruby
require 'zippendo'

instance = Zippendo::ListShippingRules200ResponseDataInnerConditionsInnerOneOf1.new(
  type: price,
  price_type: total,
  operator: gte,
  value: 500,
  shipping_price: 0,
  currency: DKK
)
```

