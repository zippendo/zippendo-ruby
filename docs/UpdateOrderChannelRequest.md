# Zippendo::UpdateOrderChannelRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **brand_id** | **String** | Brand this channel belongs to; null for organization-wide | [optional] |
| **name** | **String** | Display name for the channel. | [optional] |
| **enabled** | **Boolean** | Whether the channel is active. | [optional] |
| **role** | **String** | What Zippendo is used for on this channel. &#x60;orders_and_rates&#x60; (default) imports orders and serves checkout rates. &#x60;rates_only&#x60; serves checkout rates and service-point selection ONLY — orders are owned by an external system such as a WMS, nothing is imported, and no fulfilment or tracking is pushed back to the platform. | [optional] |
| **credentials** | **Hash&lt;String, Object&gt;** | Type-specific platform credentials. | [optional] |
| **settings** | [**UpdateOrderChannelRequestSettings**](UpdateOrderChannelRequestSettings.md) |  | [optional] |
| **shipping_rule_ids** | **Array&lt;String&gt;** | IDs of shipping rules linked to this channel. | [optional] |

## Example

```ruby
require 'zippendo'

instance = Zippendo::UpdateOrderChannelRequest.new(
  brand_id: brnd_8f3kd92ld0,
  name: Anna&#39;s Shopify Store,
  enabled: true,
  role: orders_and_rates,
  credentials: null,
  settings: null,
  shipping_rule_ids: [&quot;clz9k2f0a0002abcd5678ijkl&quot;]
)
```

