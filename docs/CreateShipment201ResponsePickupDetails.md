# Zippendo::CreateShipment201ResponsePickupDetails

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **date** | **String** | Requested pickup date (YYYY-MM-DD). |  |
| **from** | **String** | Requested earliest pickup time (HH:MM:SS). |  |
| **to** | **String** | Requested latest pickup time (HH:MM:SS). |  |
| **instruction** | **String** | Pickup instruction to the carrier. | [optional] |

## Example

```ruby
require 'zippendo'

instance = Zippendo::CreateShipment201ResponsePickupDetails.new(
  date: 2026-06-22,
  from: 08:00:00,
  to: 16:00:00,
  instruction: Ring the bell at the loading dock.
)
```

