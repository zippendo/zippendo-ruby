# Zippendo::ListShippingRules200ResponseDataInnerConditionsInner

## Class instance methods

### `openapi_one_of`

Returns the list of classes defined in oneOf.

#### Example

```ruby
require 'zippendo'

Zippendo::ListShippingRules200ResponseDataInnerConditionsInner.openapi_one_of
# =>
# [
#   :'ListShippingRules200ResponseDataInnerConditionsInnerOneOf',
#   :'ListShippingRules200ResponseDataInnerConditionsInnerOneOf1',
#   :'ListShippingRules200ResponseDataInnerConditionsInnerOneOf2',
#   :'ListShippingRules200ResponseDataInnerConditionsInnerOneOf3',
#   :'ListShippingRules200ResponseDataInnerConditionsInnerOneOf4'
# ]
```

### build

Find the appropriate object from the `openapi_one_of` list and casts the data into it.

#### Example

```ruby
require 'zippendo'

Zippendo::ListShippingRules200ResponseDataInnerConditionsInner.build(data)
# => #<ListShippingRules200ResponseDataInnerConditionsInnerOneOf:0x00007fdd4aab02a0>

Zippendo::ListShippingRules200ResponseDataInnerConditionsInner.build(data_that_doesnt_match)
# => nil
```

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| **data** | **Mixed** | data to be matched against the list of oneOf items |

#### Return type

- `ListShippingRules200ResponseDataInnerConditionsInnerOneOf`
- `ListShippingRules200ResponseDataInnerConditionsInnerOneOf1`
- `ListShippingRules200ResponseDataInnerConditionsInnerOneOf2`
- `ListShippingRules200ResponseDataInnerConditionsInnerOneOf3`
- `ListShippingRules200ResponseDataInnerConditionsInnerOneOf4`
- `nil` (if no type matches)

