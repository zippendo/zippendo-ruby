# Zippendo::CreateShippingQuoteRequestDestination

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **country** | **String** | ISO 3166-1 alpha-2 country code |  |
| **postal_code** | **String** | Postal/ZIP code | [optional] |
| **province** | **String** | State/province code | [optional] |
| **city** | **String** | City name | [optional] |
| **address1** | **String** | Street address line 1 | [optional] |
| **address2** | **String** | Street address line 2 | [optional] |

## Example

```ruby
require 'zippendo'

instance = Zippendo::CreateShippingQuoteRequestDestination.new(
  country: DK,
  postal_code: 1620,
  province: ,
  city: København,
  address1: Vesterbrogade 1,
  address2: 2. sal
)
```

