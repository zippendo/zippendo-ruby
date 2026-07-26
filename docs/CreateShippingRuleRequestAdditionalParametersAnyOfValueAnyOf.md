# Zippendo::CreateShippingRuleRequestAdditionalParametersAnyOfValueAnyOf

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Identifier of the selected service point. |  |
| **name** | **String** | Display name of the service point. |  |
| **address** | **String** | Formatted address of the service point. |  |
| **coordinates** | [**Array&lt;CreateShippingRuleRequestAdditionalParametersAnyOfValueAnyOfCoordinatesInner&gt;**](CreateShippingRuleRequestAdditionalParametersAnyOfValueAnyOfCoordinatesInner.md) | Latitude/longitude of the service point. | [optional] |

## Example

```ruby
require 'zippendo'

instance = Zippendo::CreateShippingRuleRequestAdditionalParametersAnyOfValueAnyOf.new(
  id: sp_pn_4521,
  name: Føtex Nørrebro,
  address: Nørrebrogade 20, 2200 København N,
  coordinates: [55.6987,12.5501]
)
```

