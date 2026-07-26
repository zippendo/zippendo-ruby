# Zippendo::ListOrgWebhookDeliveries200ResponseDataInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Delivery log ID |  |
| **webhook_id** | **String** | ID of the webhook this delivery belongs to |  |
| **event** | **String** | Event type that was delivered |  |
| **payload** | **Object** | JSON payload that was sent |  |
| **status_code** | **Float** | HTTP status code returned by the endpoint |  |
| **response** | **String** | Response body returned by the endpoint |  |
| **duration** | **Float** | Request duration in milliseconds |  |
| **success** | **Boolean** | Whether the delivery succeeded |  |
| **attempt** | **Float** | Delivery attempt number |  |
| **error** | **String** | Error message if the delivery failed |  |
| **created_at** | **String** | Delivery timestamp (ISO 8601) |  |

## Example

```ruby
require 'zippendo'

instance = Zippendo::ListOrgWebhookDeliveries200ResponseDataInner.new(
  id: whd_clx9z8y7x6,
  webhook_id: wh_clx1a2b3c4,
  event: shipment.created,
  payload: {&quot;id&quot;:&quot;shp_123&quot;},
  status_code: 200,
  response: OK,
  duration: 142,
  success: true,
  attempt: 1,
  error: null,
  created_at: 2026-06-10T11:16:00.000Z
)
```

