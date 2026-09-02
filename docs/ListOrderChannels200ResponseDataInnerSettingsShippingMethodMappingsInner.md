# Zippendo::ListOrderChannels200ResponseDataInnerSettingsShippingMethodMappingsInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **match** | **String** | Shipping-method title to match against imported orders (trimmed, case-insensitive, exact). |  |
| **shipping_rule_id** | **String** | Shipping rule applied to orders whose shipping-method title matches. |  |
| **service_point_selection** | **String** | For rules whose product delivers to a service point: &#39;nearest&#39; auto-selects the closest point to the recipient address; &#39;manual&#39; keeps the shipment in draft for manual selection. | [optional] |

## Example

```ruby
require 'zippendo'

instance = Zippendo::ListOrderChannels200ResponseDataInnerSettingsShippingMethodMappingsInner.new(
  match: GLS Hjemmelevering,
  shipping_rule_id: clz9k2f0a0007abcd2468qrst,
  service_point_selection: nearest
)
```

