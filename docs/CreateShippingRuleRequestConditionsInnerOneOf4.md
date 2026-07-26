# Zippendo::CreateShippingRuleRequestConditionsInnerOneOf4

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** | Condition type discriminator |  |
| **shipping_price** | **Float** | Flat shipping price |  |
| **currency** | **String** | ISO 4217 currency code |  |

## Example

```ruby
require 'zippendo'

instance = Zippendo::CreateShippingRuleRequestConditionsInnerOneOf4.new(
  type: flatRate,
  shipping_price: 39,
  currency: DKK
)
```

