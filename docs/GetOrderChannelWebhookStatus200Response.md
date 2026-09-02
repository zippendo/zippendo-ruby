# Zippendo::GetOrderChannelWebhookStatus200Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **enabled** | **Boolean** | Whether webhooks are enabled for the channel. |  |
| **webhook_url** | **String** | Expected callback URL for this channel. |  |
| **webhooks** | [**Array&lt;GetOrderChannelWebhookStatus200ResponseWebhooksInner&gt;**](GetOrderChannelWebhookStatus200ResponseWebhooksInner.md) | Webhooks registered for this channel&#39;s callback URL. |  |

## Example

```ruby
require 'zippendo'

instance = Zippendo::GetOrderChannelWebhookStatus200Response.new(
  enabled: true,
  webhook_url: https://api.zippendo.dk/webhooks/order-channels/clz9k2f0a0001abcd1234efgh,
  webhooks: null
)
```

