# Zippendo::ListAddresses200ResponseDataInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Unique address identifier |  |
| **name** | **String** | Name of the address |  |
| **att_contact** | **String** | Attention contact person |  |
| **address1** | **String** | Address line 1 |  |
| **address2** | **String** | Address line 2 |  |
| **zipcode** | **String** | Postal/ZIP code |  |
| **city** | **String** | City |  |
| **phone** | **String** | Phone number |  |
| **country_code** | **String** | ISO country code |  |
| **state** | **String** | State/Province |  |
| **email** | **String** | Email address |  |
| **customs** | **Hash&lt;String, String&gt;** | Customs identifiers keyed by type | [optional] |
| **address_types** | **Array&lt;String&gt;** | Address types (sender, pickup, return) |  |
| **org_id** | **String** | Owning organization ID |  |
| **created_at** | **String** | Creation timestamp (ISO 8601) |  |
| **updated_at** | **String** | Last update timestamp (ISO 8601) |  |

## Example

```ruby
require 'zippendo'

instance = Zippendo::ListAddresses200ResponseDataInner.new(
  id: addr_01HZX9K2QF,
  name: Hovedlager,
  att_contact: Mette Hansen,
  address1: Vesterbrogade 1,
  address2: 2. sal,
  zipcode: 1620,
  city: København,
  phone: +4533123456,
  country_code: DK,
  state: null,
  email: lager@example.dk,
  customs: {&quot;eori&quot;:&quot;DK12345678&quot;},
  address_types: [&quot;sender&quot;],
  org_id: org_01HZX9K2QF,
  created_at: 2026-06-22T09:00:00.000Z,
  updated_at: 2026-06-22T09:00:00.000Z
)
```

