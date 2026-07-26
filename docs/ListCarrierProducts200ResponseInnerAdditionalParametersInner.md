# Zippendo::ListCarrierProducts200ResponseInnerAdditionalParametersInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** | Display label for the parameter |  |
| **key** | **String** | Machine key the value is stored under |  |
| **type** | **String** | Data type of the parameter |  |
| **options** | [**Array&lt;ListCarrierProducts200ResponseInnerAdditionalParametersInnerOptionsInner&gt;**](ListCarrierProducts200ResponseInnerAdditionalParametersInnerOptionsInner.md) | Selectable options for enum-type parameters | [optional] |
| **description** | **String** | Description of the parameter |  |
| **is_required** | **Boolean** | Whether the parameter is mandatory | [default to false] |
| **required_service** | **Array&lt;String&gt;** | Service IDs for which this parameter is required | [optional] |

## Example

```ruby
require 'zippendo'

instance = Zippendo::ListCarrierProducts200ResponseInnerAdditionalParametersInner.new(
  name: Return Mode,
  key: returnFunctionality,
  type: enum,
  options: null,
  description: Instruction shown to the delivery driver,
  is_required: false,
  required_service: null
)
```

