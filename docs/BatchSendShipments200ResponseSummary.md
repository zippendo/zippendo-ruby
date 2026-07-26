# Zippendo::BatchSendShipments200ResponseSummary

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **total** | **Integer** | Number of unique shipments processed. |  |
| **sent** | **Integer** | How many were successfully booked. |  |
| **failed** | **Integer** | How many failed. |  |

## Example

```ruby
require 'zippendo'

instance = Zippendo::BatchSendShipments200ResponseSummary.new(
  total: 3,
  sent: 2,
  failed: 1
)
```

