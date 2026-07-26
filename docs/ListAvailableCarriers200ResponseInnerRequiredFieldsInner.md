# Zippendo::ListAvailableCarriers200ResponseInnerRequiredFieldsInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** | Human-readable label for the configuration field |  |
| **key** | **String** | Machine key used to store the field value |  |
| **type** | **String** | Data type of the configuration field |  |
| **options** | [**Array&lt;ListCarrierProducts200ResponseInnerAdditionalParametersInnerOptionsInner&gt;**](ListCarrierProducts200ResponseInnerAdditionalParametersInnerOptionsInner.md) | Selectable options for enum-type fields | [optional] |
| **description** | **String** | Help text describing the field |  |
| **required** | **Boolean** | Whether the field is mandatory | [optional] |

## Example

```ruby
require 'zippendo'

instance = Zippendo::ListAvailableCarriers200ResponseInnerRequiredFieldsInner.new(
  name: Customer number,
  key: customerNumber,
  type: string,
  options: null,
  description: Your PostNord customer number,
  required: true
)
```

