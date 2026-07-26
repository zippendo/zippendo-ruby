# Zippendo::CreateShipment201ResponseErrorsInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Unique error identifier. |  |
| **carrier** | **String** | Carrier that produced the error. |  |
| **code** | **String** | Carrier-specific error code. | [optional] |
| **message** | **String** | Human-readable error message. |  |
| **created_at** | **String** | Timestamp when the error occurred. |  |

## Example

```ruby
require 'zippendo'

instance = Zippendo::CreateShipment201ResponseErrorsInner.new(
  id: err_2b3c4d5e,
  carrier: PostNord,
  code: INVALID_POSTAL_CODE,
  message: Receiver postal code is invalid for the selected product.,
  created_at: 2026-06-22T14:30:00.000Z
)
```

