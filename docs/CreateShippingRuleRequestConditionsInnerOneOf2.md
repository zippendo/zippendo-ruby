# Zippendo::CreateShippingRuleRequestConditionsInnerOneOf2

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** | Condition type discriminator |  |
| **price_type** | **String** | Whether to compare against subtotal (before discounts) or total (after discounts) | [optional][default to &#39;total&#39;] |
| **min** | **Float** | Minimum cart value (inclusive) |  |
| **max** | **Float** | Maximum cart value (inclusive) |  |
| **shipping_price** | **Float** | Shipping price when condition matches |  |
| **currency** | **String** | ISO 4217 currency code |  |

## Example

```ruby
require 'zippendo'

instance = Zippendo::CreateShippingRuleRequestConditionsInnerOneOf2.new(
  type: priceRange,
  price_type: total,
  min: 0,
  max: 499,
  shipping_price: 49,
  currency: DKK
)
```

