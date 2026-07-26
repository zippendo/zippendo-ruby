# Zippendo::CreateOrgWebhookRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** | Human-readable webhook name |  |
| **url** | **String** | Webhook endpoint URL |  |
| **events** | **Array&lt;String&gt;** | Events to subscribe to |  |
| **is_active** | **Boolean** | Whether the webhook is active | [optional][default to true] |

## Example

```ruby
require 'zippendo'

instance = Zippendo::CreateOrgWebhookRequest.new(
  name: Order fulfilment notifier,
  url: https://hooks.example.dk/zippendo,
  events: [&quot;shipment.created&quot;,&quot;tracking.updated&quot;],
  is_active: true
)
```

