# Zippendo::CreateOrderChannelWebhookSecret201Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **secret** | **String** | The webhook signing secret. Returned only once — store it in your system; every push to the ingest URL must carry an HMAC-SHA256 hex signature of the raw body computed with it. |  |
| **webhook_url** | **String** | The ingest URL your system pushes signed order events to. |  |
| **created_at** | **Time** | When this secret was issued (ISO 8601). |  |

## Example

```ruby
require 'zippendo'

instance = Zippendo::CreateOrderChannelWebhookSecret201Response.new(
  secret: zwhs_XeVJ1n8vJZbJ0N3mYQ2fV0dK9cA5tR7uW4pL6sH8gB0,
  webhook_url: https://api.zippendo.com/webhooks/order-channels/clz9k2f0a0001abcd1234efgh,
  created_at: 2026-09-02T14:30Z
)
```

