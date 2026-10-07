# Zippendo::GetBillingUsage200ResponseAddOnsInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** | Type of billing add-on |  |
| **quantity** | **Float** | Number of add-on units purchased |  |
| **unit_price** | **Float** | Price per unit per month, in minor units of the billing currency |  |
| **total_price** | **Float** | Total price per month, in minor units of the billing currency |  |

## Example

```ruby
require 'zippendo'

instance = Zippendo::GetBillingUsage200ResponseAddOnsInner.new(
  type: extra_carrier,
  quantity: 2,
  unit_price: 9900,
  total_price: 19800
)
```

