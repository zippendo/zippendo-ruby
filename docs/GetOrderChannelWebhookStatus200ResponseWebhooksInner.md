# Zippendo::GetOrderChannelWebhookStatus200ResponseWebhooksInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Float** | Platform webhook ID. |  |
| **topic** | **String** | Webhook event topic. |  |
| **address** | **String** | Registered callback address. |  |
| **created_at** | **String** | Webhook creation timestamp. |  |
| **delivery_url** | **String** | WooCommerce delivery URL (same as &#x60;address&#x60;; present for WooCommerce channels). | [optional] |
| **status** | **String** | WooCommerce webhook status. A value other than &#x60;active&#x60; means WooCommerce disabled the webhook (e.g. after repeated delivery failures). | [optional] |

## Example

```ruby
require 'zippendo'

instance = Zippendo::GetOrderChannelWebhookStatus200ResponseWebhooksInner.new(
  id: 1234567890,
  topic: ORDERS_CREATE,
  address: https://api.zippendo.dk/webhooks/order-channels/clz9k2f0a0001abcd1234efgh,
  created_at: 2026-06-22T14:30:00.000Z,
  delivery_url: https://api.zippendo.dk/webhooks/order-channels/clz9k2f0a0001abcd1234efgh,
  status: active
)
```

