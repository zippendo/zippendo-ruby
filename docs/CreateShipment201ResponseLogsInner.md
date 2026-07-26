# Zippendo::CreateShipment201ResponseLogsInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Unique log entry identifier. |  |
| **direction** | **String** | Direction of the logged request. |  |
| **request** | **Object** | Captured request payload. |  |
| **response** | **Object** | Captured response payload. | [optional] |
| **status_code** | **Float** | HTTP status code of the response. | [optional] |
| **error** | **String** | Error message if the request failed. | [optional] |
| **duration** | **Float** | Request duration in milliseconds. | [optional] |
| **created_at** | **String** | Timestamp when the log entry was created. |  |

## Example

```ruby
require 'zippendo'

instance = Zippendo::CreateShipment201ResponseLogsInner.new(
  id: log_6f7a8b9c,
  direction: outbound,
  request: null,
  response: null,
  status_code: 200,
  error: Connection timed out,
  duration: 342,
  created_at: 2026-06-22T14:30:00.000Z
)
```

