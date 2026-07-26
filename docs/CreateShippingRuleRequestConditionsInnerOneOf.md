# Zippendo::CreateShippingRuleRequestConditionsInnerOneOf

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** | Condition type discriminator |  |
| **min** | **Float** | Minimum weight in kg (inclusive) |  |
| **max** | **Float** | Maximum weight in kg (inclusive) |  |
| **shipping_price** | **Float** | Shipping price when condition matches |  |
| **currency** | **String** | ISO 4217 currency code |  |

## Example

```ruby
require 'zippendo'

instance = Zippendo::CreateShippingRuleRequestConditionsInnerOneOf.new(
  type: weight,
  min: 0,
  max: 5,
  shipping_price: 39,
  currency: DKK
)
```

