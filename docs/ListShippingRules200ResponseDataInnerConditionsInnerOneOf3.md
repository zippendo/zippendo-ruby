# Zippendo::ListShippingRules200ResponseDataInnerConditionsInnerOneOf3

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** | Condition type discriminator |  |
| **operator** | **String** | Comparison operator |  |
| **value** | **Integer** | Quantity value to compare against |  |
| **shipping_price** | **Float** | Shipping price when condition matches |  |
| **currency** | **String** | ISO 4217 currency code |  |

## Example

```ruby
require 'zippendo'

instance = Zippendo::ListShippingRules200ResponseDataInnerConditionsInnerOneOf3.new(
  type: quantity,
  operator: gte,
  value: 3,
  shipping_price: 0,
  currency: DKK
)
```

