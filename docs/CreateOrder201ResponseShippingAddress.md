# Zippendo::CreateOrder201ResponseShippingAddress

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** | Recipient full name. |  |
| **attention** | **String** | Attention / care-of line. | [optional] |
| **company** | **String** | Company name. | [optional] |
| **address1** | **String** | Street address line 1. |  |
| **address2** | **String** | Street address line 2. | [optional] |
| **city** | **String** | City name. |  |
| **province** | **String** | Province or region name. | [optional] |
| **province_code** | **String** | Province or region code. | [optional] |
| **postal_code** | **String** | Postal code. |  |
| **country** | **String** | Country name. | [optional] |
| **country_code** | **String** | ISO 3166-1 alpha-2 country code. |  |
| **phone** | **String** | Recipient phone number. | [optional] |
| **email** | **String** | Recipient email address. | [optional] |

## Example

```ruby
require 'zippendo'

instance = Zippendo::CreateOrder201ResponseShippingAddress.new(
  name: Anna Jensen,
  attention: c/o Reception,
  company: Jensen Design ApS,
  address1: Nørregade 12,
  address2: 2. sal,
  city: København,
  province: Hovedstaden,
  province_code: DK-84,
  postal_code: 1165,
  country: Denmark,
  country_code: DK,
  phone: +45 12 34 56 78,
  email: anna@example.dk
)
```

