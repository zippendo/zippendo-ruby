# Zippendo::UpdateAddressRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** | Name of the address | [optional] |
| **att_contact** | **String** | Attention contact person | [optional] |
| **address1** | **String** | Address line 1 | [optional] |
| **address2** | **String** | Address line 2 | [optional] |
| **zipcode** | **String** | Postal/ZIP code | [optional] |
| **city** | **String** | City | [optional] |
| **phone** | **String** | Phone number | [optional] |
| **country_code** | **String** | ISO country code | [optional] |
| **state** | **String** | State/Province | [optional] |
| **email** | **String** | Email address | [optional] |
| **customs** | **Hash&lt;String, String&gt;** | Customs identifiers | [optional] |
| **address_types** | **Array&lt;String&gt;** | Address types (sender, pickup, return) | [optional] |

## Example

```ruby
require 'zippendo'

instance = Zippendo::UpdateAddressRequest.new(
  name: Hovedlager,
  att_contact: Mette Hansen,
  address1: Vesterbrogade 1,
  address2: 2. sal,
  zipcode: 1620,
  city: København,
  phone: +4533123456,
  country_code: DK,
  state: Hovedstaden,
  email: lager@example.dk,
  customs: {&quot;eori&quot;:&quot;DK12345678&quot;},
  address_types: [&quot;sender&quot;]
)
```

