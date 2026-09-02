# Zippendo::CreateOrderChannelRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** | Display name for the channel. |  |
| **type** | **String** | Type of the order channel. Platform channels (Shopify, WooCommerce) are created via their connect flows. |  |
| **brand_id** | **String** | Brand this channel belongs to; null for organization-wide | [optional] |
| **enabled** | **Boolean** | Whether the channel is active. | [optional][default to true] |
| **settings** | [**CreateOrderChannelRequestSettings**](CreateOrderChannelRequestSettings.md) |  | [optional] |

## Example

```ruby
require 'zippendo'

instance = Zippendo::CreateOrderChannelRequest.new(
  name: Anna&#39;s webshop,
  type: custom,
  brand_id: brnd_8f3kd92ld0,
  enabled: true,
  settings: null
)
```

