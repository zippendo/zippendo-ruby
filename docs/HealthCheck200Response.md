# Zippendo::HealthCheck200Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **status** | **String** | Service status |  |
| **timestamp** | **String** | Current server time (ISO 8601) |  |
| **version** | **String** | API version |  |

## Example

```ruby
require 'zippendo'

instance = Zippendo::HealthCheck200Response.new(
  status: ok,
  timestamp: 2026-06-22T14:30:00.000Z,
  version: 1.0.0
)
```

