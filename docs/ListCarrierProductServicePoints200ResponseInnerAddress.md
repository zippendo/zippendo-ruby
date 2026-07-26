# Zippendo::ListCarrierProductServicePoints200ResponseInnerAddress

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **address1** | **String** | Street address line 1 |  |
| **address2** | **String** | Street address line 2 | [optional] |
| **postal_code** | **String** | Postal code |  |
| **state** | **String** | State or region | [optional] |
| **city** | **String** | City name |  |
| **country_code** | **String** | ISO 3166-1 alpha-2 country code |  |

## Example

```ruby
require 'zippendo'

instance = Zippendo::ListCarrierProductServicePoints200ResponseInnerAddress.new(
  address1: Vesterbrogade 1,
  address2: 2. sal,
  postal_code: 1620,
  state: null,
  city: København,
  country_code: DK
)
```

