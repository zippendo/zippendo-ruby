# Zippendo::TrackShipment200Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **tracking_number** | **String** | Carrier tracking number. |  |
| **tracking_url** | **String** | Public carrier tracking URL. |  |
| **current_status** | **String** | Latest normalized tracking status. |  |
| **estimated_delivery** | **String** | Estimated delivery timestamp. | [optional] |
| **events** | [**Array&lt;TrackShipment200ResponseEventsInner&gt;**](TrackShipment200ResponseEventsInner.md) | Tracking events ordered from newest to oldest. |  |

## Example

```ruby
require 'zippendo'

instance = Zippendo::TrackShipment200Response.new(
  tracking_number: 00370724710000012345,
  tracking_url: https://tracking.postnord.com/00370724710000012345,
  current_status: delivered,
  estimated_delivery: 2026-06-23T12:00:00.000Z,
  events: null
)
```

