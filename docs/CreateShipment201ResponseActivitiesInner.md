# Zippendo::CreateShipment201ResponseActivitiesInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Unique activity identifier. |  |
| **action** | **String** | Type of activity performed on the shipment. |  |
| **description** | **String** | Human-readable description of the activity. |  |
| **metadata** | **Object** | Additional structured data about the activity. | [optional] |
| **created_at** | **String** | Timestamp when the activity occurred. |  |

## Example

```ruby
require 'zippendo'

instance = Zippendo::CreateShipment201ResponseActivitiesInner.new(
  id: act_1d2e3f4a,
  action: created,
  description: Shipment created,
  metadata: null,
  created_at: 2026-06-22T14:30:00.000Z
)
```

