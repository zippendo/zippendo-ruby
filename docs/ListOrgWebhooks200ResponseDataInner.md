# Zippendo::ListOrgWebhooks200ResponseDataInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Webhook ID |  |
| **name** | **String** | Human-readable webhook name |  |
| **url** | **String** | Webhook endpoint URL |  |
| **events** | **Array&lt;String&gt;** | Events the webhook is subscribed to |  |
| **is_active** | **Boolean** | Whether the webhook is active |  |
| **created_at** | **String** | Creation timestamp (ISO 8601) |  |
| **updated_at** | **String** | Last update timestamp (ISO 8601) |  |

## Example

```ruby
require 'zippendo'

instance = Zippendo::ListOrgWebhooks200ResponseDataInner.new(
  id: wh_clx1a2b3c4,
  name: Order fulfilment notifier,
  url: https://hooks.example.dk/zippendo,
  events: [&quot;shipment.created&quot;],
  is_active: true,
  created_at: 2026-06-01T09:30:00.000Z,
  updated_at: 2026-06-10T11:15:00.000Z
)
```

