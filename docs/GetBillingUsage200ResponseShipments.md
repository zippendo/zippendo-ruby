# Zippendo::GetBillingUsage200ResponseShipments

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **used** | **Float** | Shipments created this period |  |
| **included** | **Float** | Shipments included in the plan |  |
| **overage** | **Float** | Shipments above the included allowance |  |
| **overage_charges** | **Float** | Overage charges so far, in øre |  |

## Example

```ruby
require 'zippendo'

instance = Zippendo::GetBillingUsage200ResponseShipments.new(
  used: 1240,
  included: 1000,
  overage: 240,
  overage_charges: 36000
)
```

