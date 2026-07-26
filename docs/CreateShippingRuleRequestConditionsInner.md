# Zippendo::CreateShippingRuleRequestConditionsInner

## Class instance methods

### `openapi_one_of`

Returns the list of classes defined in oneOf.

#### Example

```ruby
require 'zippendo'

Zippendo::CreateShippingRuleRequestConditionsInner.openapi_one_of
# =>
# [
#   :'CreateShippingRuleRequestConditionsInnerOneOf',
#   :'CreateShippingRuleRequestConditionsInnerOneOf1',
#   :'CreateShippingRuleRequestConditionsInnerOneOf2',
#   :'CreateShippingRuleRequestConditionsInnerOneOf3',
#   :'CreateShippingRuleRequestConditionsInnerOneOf4'
# ]
```

### build

Find the appropriate object from the `openapi_one_of` list and casts the data into it.

#### Example

```ruby
require 'zippendo'

Zippendo::CreateShippingRuleRequestConditionsInner.build(data)
# => #<CreateShippingRuleRequestConditionsInnerOneOf:0x00007fdd4aab02a0>

Zippendo::CreateShippingRuleRequestConditionsInner.build(data_that_doesnt_match)
# => nil
```

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| **data** | **Mixed** | data to be matched against the list of oneOf items |

#### Return type

- `CreateShippingRuleRequestConditionsInnerOneOf`
- `CreateShippingRuleRequestConditionsInnerOneOf1`
- `CreateShippingRuleRequestConditionsInnerOneOf2`
- `CreateShippingRuleRequestConditionsInnerOneOf3`
- `CreateShippingRuleRequestConditionsInnerOneOf4`
- `nil` (if no type matches)

