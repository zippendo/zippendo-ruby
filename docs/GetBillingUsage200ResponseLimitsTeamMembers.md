# Zippendo::GetBillingUsage200ResponseLimitsTeamMembers

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **used** | **Float** | Amount of the resource currently used |  |
| **limit** | **Float** | Maximum allowed (-1 for unlimited) |  |

## Example

```ruby
require 'zippendo'

instance = Zippendo::GetBillingUsage200ResponseLimitsTeamMembers.new(
  used: 3,
  limit: 5
)
```

