# Zippendo::TrackShipment200ResponseEventsInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Unique tracking event identifier. |  |
| **status** | **String** | Normalized tracking status for the event. |  |
| **carrier_status** | **String** | Raw status string reported by the carrier. |  |
| **description** | **String** | Human-readable description of the event. |  |
| **location** | **String** | Location where the event was registered. |  |
| **occurred_at** | **String** | Timestamp when the event occurred. |  |

## Example

```ruby
require 'zippendo'

instance = Zippendo::TrackShipment200ResponseEventsInner.new(
  id: trk_7a8b9c0d,
  status: in_transit,
  carrier_status: INFORMED,
  description: The shipment is on its way.,
  location: København,
  occurred_at: 2026-06-22T14:30:00.000Z
)
```

