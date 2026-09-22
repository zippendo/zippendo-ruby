# Zippendo::CreateAddressRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** | Company or person the parcel is sent from, printed on labels |  |
| **description** | **String** | Internal label for this address; never printed or sent to a carrier | [optional] |
| **att_contact** | **String** | Contact person at this address, printed as the att. line | [optional] |
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
| **brand_id** | **String** | Brand this record is assigned to; null (or omitted outside a brand session) keeps it organization-wide | [optional] |

## Example

```ruby
require 'zippendo'

instance = Zippendo::CreateAddressRequest.new(
  name: Zippendo ApS,
  description: Main warehouse, Copenhagen,
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
  address_types: [&quot;sender&quot;],
  brand_id: brnd_8f3kd92ld0
)
```

