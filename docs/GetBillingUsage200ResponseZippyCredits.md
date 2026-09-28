# Zippendo::GetBillingUsage200ResponseZippyCredits

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **used** | **Float** | Zippy credits used this period, included bundle and metered alike |  |
| **included** | **Float** | Credits included in the add-on bundle this period |  |
| **billed** | **Float** | Credits beyond the bundle, metered this period |  |
| **charges** | **Float** | Metered credit charges so far, in øre (whole packs) |  |
| **limit** | **Float** | Maximum Zippy credits per month (-1 for unlimited) |  |

## Example

```ruby
require 'zippendo'

instance = Zippendo::GetBillingUsage200ResponseZippyCredits.new(
  used: 2640,
  included: 2500,
  billed: 140,
  charges: 1000,
  limit: -1
)
```

