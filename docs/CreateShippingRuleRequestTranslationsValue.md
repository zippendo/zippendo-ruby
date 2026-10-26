# Zippendo::CreateShippingRuleRequestTranslationsValue

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** | Checkout name in this language; blank keeps the rule&#39;s own name. | [optional] |
| **description** | **String** | Checkout description in this language; blank keeps the rule&#39;s own description. | [optional] |

## Example

```ruby
require 'zippendo'

instance = Zippendo::CreateShippingRuleRequestTranslationsValue.new(
  name: Pakkeshop,
  description: Levering til en pakkeshop nær dig
)
```

