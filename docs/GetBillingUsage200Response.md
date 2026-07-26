# Zippendo::GetBillingUsage200Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **current_period** | [**GetBillingUsage200ResponseCurrentPeriod**](GetBillingUsage200ResponseCurrentPeriod.md) |  |  |
| **shipments** | [**GetBillingUsage200ResponseShipments**](GetBillingUsage200ResponseShipments.md) |  |  |
| **limits** | [**GetBillingUsage200ResponseLimits**](GetBillingUsage200ResponseLimits.md) |  |  |
| **add_ons** | [**Array&lt;GetBillingUsage200ResponseAddOnsInner&gt;**](GetBillingUsage200ResponseAddOnsInner.md) | Active add-ons on the subscription |  |

## Example

```ruby
require 'zippendo'

instance = Zippendo::GetBillingUsage200Response.new(
  current_period: null,
  shipments: null,
  limits: null,
  add_ons: []
)
```

