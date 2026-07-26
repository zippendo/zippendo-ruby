# Zippendo::ListCarrierProducts200ResponseInnerWeightLimits

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **min** | **Float** | Minimum allowed parcel weight |  |
| **max** | **Float** | Maximum allowed parcel weight |  |
| **unit** | **String** | Unit of the weight limits |  |

## Example

```ruby
require 'zippendo'

instance = Zippendo::ListCarrierProducts200ResponseInnerWeightLimits.new(
  min: 0.1,
  max: 35,
  unit: kg
)
```

