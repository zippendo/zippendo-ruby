# Zippendo::GetBillingUsage200ResponseZippyMessages

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **used** | **Float** | Zippy messages used this period |  |
| **charges** | **Float** | Zippy message charges so far, in øre |  |
| **limit** | **Float** | Maximum Zippy messages per month (-1 for unlimited) |  |

## Example

```ruby
require 'zippendo'

instance = Zippendo::GetBillingUsage200ResponseZippyMessages.new(
  used: 42,
  charges: 4158,
  limit: -1
)
```

