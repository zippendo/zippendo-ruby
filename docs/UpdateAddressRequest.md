# Zippendo::UpdateAddressRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** | Company or person the parcel is sent from, printed on labels | [optional] |
| **description** | **String** | Internal label for this address; send null or an empty string to clear it | [optional] |
| **att_contact** | **String** | Contact person at this address; send null or an empty string to clear it | [optional] |
| **address1** | **String** | Address line 1 | [optional] |
| **address2** | **String** | Address line 2; send null or an empty string to clear it | [optional] |
| **zipcode** | **String** | Postal/ZIP code | [optional] |
| **city** | **String** | City | [optional] |
| **phone** | **String** | Phone number | [optional] |
| **country_code** | **String** | ISO country code | [optional] |
| **state** | **String** | State/Province; send null or an empty string to clear it | [optional] |
| **email** | **String** | Email address | [optional] |
| **customs** | **Hash&lt;String, String&gt;** | Customs identifiers | [optional] |
| **address_types** | **Array&lt;String&gt;** | Address types (sender, pickup, return) | [optional] |
| **brand_id** | **String** | Brand this record is assigned to; null (or omitted outside a brand session) keeps it organization-wide | [optional] |

## Example

```ruby
require 'zippendo'

instance = Zippendo::UpdateAddressRequest.new(
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

