# Zippendo::CreateAddressRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** | Name of the address |  |
| **att_contact** | **String** | Attention contact person |  |
| **address1** | **String** | Address line 1 |  |
| **address2** | **String** | Address line 2 | [optional] |
| **zipcode** | **String** | Postal/ZIP code |  |
| **city** | **String** | City |  |
| **phone** | **String** | Phone number |  |
| **country_code** | **String** | Country code (ISO 2 or 3 letter) |  |
| **state** | **String** | State/Province | [optional] |
| **email** | **String** | Email address |  |
| **customs** | **Hash&lt;String, String&gt;** | Customs identifiers (voec, eori, sprn, ioss, fda, duns) | [optional] |
| **address_types** | **Array&lt;String&gt;** | Address types (sender, pickup, return) | [optional] |

## Example

```ruby
require 'zippendo'

instance = Zippendo::CreateAddressRequest.new(
  name: Hovedlager,
  att_contact: Mette Hansen,
  address1: Vesterbrogade 1,
  address2: 2. sal,
  zipcode: 1620,
  city: København,
  phone: +4533123456,
  country_code: DK,
  state: ,
  email: lager@example.dk,
  customs: {&quot;eori&quot;:&quot;DK12345678&quot;},
  address_types: [&quot;sender&quot;]
)
```

