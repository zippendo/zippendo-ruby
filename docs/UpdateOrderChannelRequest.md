# Zippendo::UpdateOrderChannelRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **brand_id** | **String** | Brand this channel belongs to; null for organization-wide | [optional] |
| **name** | **String** | Display name for the channel. | [optional] |
| **enabled** | **Boolean** | Whether the channel is active. | [optional] |
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
  credentials: null,
  settings: null,
  shipping_rule_ids: [&quot;clz9k2f0a0002abcd5678ijkl&quot;]
)
```

