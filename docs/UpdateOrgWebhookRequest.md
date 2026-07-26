# Zippendo::UpdateOrgWebhookRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** | Human-readable webhook name | [optional] |
| **url** | **String** | Webhook endpoint URL | [optional] |
| **events** | **Array&lt;String&gt;** | Events to subscribe to | [optional] |
| **is_active** | **Boolean** | Whether the webhook is active | [optional] |

## Example

```ruby
require 'zippendo'

instance = Zippendo::UpdateOrgWebhookRequest.new(
  name: Order fulfilment notifier,
  url: https://hooks.example.dk/zippendo,
  events: [&quot;shipment.created&quot;],
  is_active: true
)
```

