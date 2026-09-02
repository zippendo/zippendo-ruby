# Zippendo::CreateOrderChannelRequestSettings

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **use_webhooks** | **Boolean** | Use webhooks for real-time order sync. | [optional][default to true] |
| **site_url** | **String** | WooCommerce store URL. | [optional] |
| **auto_fulfill** | **Boolean** | Push tracking back to the platform when a shipment is dispatched. Enabled by default (opt-out) — set to false to disable write-back; an unset value still syncs. | [optional] |
| **auto_sync** | **Boolean** | Periodically poll the channel for new orders. | [optional][default to false] |
| **sync_interval_minutes** | **Integer** | Polling interval in minutes (5-1440). | [optional][default to 15] |
| **auto_ship_on_create** | **Boolean** | Create a shipment automatically when an order arrives. | [optional][default to false] |
| **default_carrier_id** | **String** | Default carrier ID for auto-shipping. | [optional] |
| **default_product_id** | **String** | Default carrier product ID for auto-shipping. | [optional] |
| **default_address_id** | **String** | Default sender address ID for auto-shipping. | [optional] |
| **shipping_method_mappings** | [**Array&lt;CreateOrderChannelRequestSettingsShippingMethodMappingsInner&gt;**](CreateOrderChannelRequestSettingsShippingMethodMappingsInner.md) | Map imported shipping-method titles to shipping rules, for channels without checkout rate integration. | [optional] |
| **sync_only_unfulfilled** | **Boolean** | Only import orders that are not yet fulfilled. | [optional][default to true] |
| **sync_orders_since** | **Time** | Only sync orders placed at or after this timestamp. | [optional] |
| **service_point_count** | **Integer** | Number of service points to show at checkout (1-20). | [optional][default to 6] |

## Example

```ruby
require 'zippendo'

instance = Zippendo::CreateOrderChannelRequestSettings.new(
  use_webhooks: true,
  site_url: https://butik.dk,
  auto_fulfill: true,
  auto_sync: false,
  sync_interval_minutes: 15,
  auto_ship_on_create: false,
  default_carrier_id: clz9k2f0a0006abcd1357yzab,
  default_product_id: postnord-home-delivery,
  default_address_id: clz9k2f0a0005abcd7890uvwx,
  shipping_method_mappings: [{&quot;match&quot;:&quot;GLS Hjemmelevering&quot;,&quot;shippingRuleId&quot;:&quot;clz9k2f0a0007abcd2468qrst&quot;}],
  sync_only_unfulfilled: true,
  sync_orders_since: 2026-05-22T00:00Z,
  service_point_count: 6
)
```

