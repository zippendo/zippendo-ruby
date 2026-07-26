# Zippendo::ListShipments200ResponseDataInnerCarrierSettings

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **carrier_id** | **String** | Identifier of the carrier to use. |  |
| **product_id** | **String** | Identifier of the carrier product/service. |  |
| **services** | **Array&lt;String&gt;** | Additional service codes requested from the carrier. |  |
| **additional_parameters** | [**Hash&lt;String, ListShipments200ResponseDataInnerCarrierSettingsAdditionalParametersValue&gt;**](ListShipments200ResponseDataInnerCarrierSettingsAdditionalParametersValue.md) | Carrier-specific extra parameters as key/value pairs. |  |

## Example

```ruby
require 'zippendo'

instance = Zippendo::ListShipments200ResponseDataInnerCarrierSettings.new(
  carrier_id: car_pn_001,
  product_id: prod_mypack_home,
  services: [&quot;A7&quot;],
  additional_parameters: {&quot;notificationEmail&quot;:&quot;anna@example.dk&quot;}
)
```

