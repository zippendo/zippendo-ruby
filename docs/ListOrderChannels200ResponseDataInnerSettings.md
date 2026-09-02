# Zippendo::ListOrderChannels200ResponseDataInnerSettings

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **use_webhooks** | **Boolean** | Use webhooks for real-time order sync. | [default to true] |
| **webhook_id** | **String** | External webhook identifier for management. | [optional] |
| **webhook_ids** | **Array&lt;Integer&gt;** | Registered WooCommerce webhook ids. | [optional] |
| **webhook_secret_created_at** | **Time** | When the custom channel&#39;s webhook signing secret was issued. A non-secret signal so clients can show that a secret exists; the secret itself is never returned after creation. | [optional] |
| **site_url** | **String** | WooCommerce store URL. | [optional] |
| **auto_fulfill** | **Boolean** | Push tracking back to the platform when a shipment is dispatched. Enabled by default (opt-out) — set to false to disable write-back; an unset value still syncs. | [optional] |
| **checkout_token_created_at** | **Time** | When the checkout token was issued (internal; never exposed in API responses). | [optional] |
| **auto_sync** | **Boolean** | Periodically poll the channel for new orders. | [default to false] |
| **sync_interval_minutes** | **Integer** | Polling interval in minutes (5-1440). | [default to 15] |
| **auto_ship_on_create** | **Boolean** | Create a shipment automatically when an order arrives. | [default to false] |
| **default_carrier_id** | **String** | Default carrier ID for auto-shipping. | [optional] |
| **default_product_id** | **String** | Default carrier product ID for auto-shipping. | [optional] |
| **default_address_id** | **String** | Default sender address ID for auto-shipping. | [optional] |
| **shipping_method_mappings** | [**Array&lt;ListOrderChannels200ResponseDataInnerSettingsShippingMethodMappingsInner&gt;**](ListOrderChannels200ResponseDataInnerSettingsShippingMethodMappingsInner.md) | Map imported shipping-method titles to shipping rules, for channels without checkout rate integration. | [optional] |
| **sync_only_unfulfilled** | **Boolean** | Only import orders that are not yet fulfilled. | [default to true] |
| **sync_orders_since** | **Time** | Only sync orders placed at or after this timestamp. | [optional] |
| **service_point_count** | **Integer** | Number of service points to show at checkout (1-20). | [default to 6] |

## Example

```ruby
require 'zippendo'

instance = Zippendo::ListOrderChannels200ResponseDataInnerSettings.new(
  use_webhooks: true,
  webhook_id: gid://shopify/WebhookSubscription/12345,
  webhook_ids: [12,13,14],
  webhook_secret_created_at: 2026-06-22T14:30Z,
  site_url: https://butik.dk,
  auto_fulfill: true,
  checkout_token_created_at: 2026-06-22T14:30Z,
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

