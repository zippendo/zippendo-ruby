# Zippendo::CreateShippingRuleRequestAdditionalParametersAnyOfInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** | Carrier parameter key |  |
| **val** | **String** | Parameter value (stringified) |  |

## Example

```ruby
require 'zippendo'

instance = Zippendo::CreateShippingRuleRequestAdditionalParametersAnyOfInner.new(
  name: returnFunctionality,
  val: LABELLESS
)
```

