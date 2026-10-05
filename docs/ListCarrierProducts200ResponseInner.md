# Zippendo::ListCarrierProducts200ResponseInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** | Display name of the carrier product |  |
| **product_id** | **String** | Unique carrier product identifier |  |
| **type** | **String** | Direction of the shipment for this product |  |
| **description** | **String** | Description of the carrier product | [optional] |
| **available_countries** | **Array&lt;String&gt;** | Receiver countries this product delivers to |  |
| **available_sender_countries** | **Array&lt;String&gt;** | Sender countries supported by this product |  |
| **is_service_point** | **Boolean** | Whether this product delivers to a service point | [default to false] |
| **is_pickup_available** | **Boolean** | Whether carrier pickup is available for this product | [default to false] |
| **services** | [**Array&lt;ListCarrierProducts200ResponseInnerServicesInner&gt;**](ListCarrierProducts200ResponseInnerServicesInner.md) | Additional services available for this product | [optional] |
| **additional_parameters** | [**Array&lt;ListCarrierProducts200ResponseInnerAdditionalParametersInner&gt;**](ListCarrierProducts200ResponseInnerAdditionalParametersInner.md) | Extra parameters that can or must be supplied for this product | [optional] |
| **weight_limits** | [**ListCarrierProducts200ResponseInnerWeightLimits**](ListCarrierProducts200ResponseInnerWeightLimits.md) |  | [optional] |

## Example

```ruby
require 'zippendo'

instance = Zippendo::ListCarrierProducts200ResponseInner.new(
  name: PostNord MyPack Home,
  product_id: PNL13,
  type: outbound,
  description: Home delivery within Denmark,
  available_countries: null,
  available_sender_countries: null,
  is_service_point: false,
  is_pickup_available: true,
  services: null,
  additional_parameters: null,
  weight_limits: null
)
```

