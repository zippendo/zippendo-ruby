# Zippendo::BatchSendShipments200ResponseSummary

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **total** | **Integer** | Number of unique shipments requested. |  |
| **sent** | **Integer** | How many were successfully booked. |  |
| **failed** | **Integer** | How many the carrier or Zippendo rejected. |  |
| **skipped** | **Integer** | How many the batch ran out of time to attempt. Submit these again. |  |

## Example

```ruby
require 'zippendo'

instance = Zippendo::BatchSendShipments200ResponseSummary.new(
  total: 3,
  sent: 2,
  failed: 1,
  skipped: 0
)
```

