# Zippendo::CreateOrderChannelRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** | Display name for the channel. |  |
| **type** | **String** | Type of the order channel. Platform channels (Shopify, WooCommerce) are created via their connect flows. |  |
| **brand_id** | **String** | Brand this channel belongs to; null for organization-wide | [optional] |
| **enabled** | **Boolean** | Whether the channel is active. | [optional][default to true] |
| **role** | **String** | What Zippendo is used for on this channel. &#x60;orders_and_rates&#x60; (default) imports orders and serves checkout rates. &#x60;rates_only&#x60; serves checkout rates and service-point selection ONLY — orders are owned by an external system such as a WMS, nothing is imported, and no fulfilment or tracking is pushed back to the platform. | [optional][default to &#39;orders_and_rates&#39;] |
| **settings** | [**CreateOrderChannelRequestSettings**](CreateOrderChannelRequestSettings.md) |  | [optional] |

## Example

```ruby
require 'zippendo'

instance = Zippendo::CreateOrderChannelRequest.new(
  name: Anna&#39;s webshop,
  type: custom,
  brand_id: brnd_8f3kd92ld0,
  enabled: true,
  role: orders_and_rates,
  settings: null
)
```

