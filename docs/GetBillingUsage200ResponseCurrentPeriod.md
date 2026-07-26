# Zippendo::GetBillingUsage200ResponseCurrentPeriod

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **start** | **String** | Start of the current usage period (ISO 8601) |  |
| **_end** | **String** | End of the current usage period (ISO 8601) |  |

## Example

```ruby
require 'zippendo'

instance = Zippendo::GetBillingUsage200ResponseCurrentPeriod.new(
  start: 2026-06-01T00:00:00.000Z,
  _end: 2026-07-01T00:00:00.000Z
)
```

