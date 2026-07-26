# Zippendo::GetOrg200Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Unique organization identifier |  |
| **name** | **String** | Organization name |  |
| **slug** | **String** | Organization URL slug (unique identifier) |  |
| **description** | **String** | Organization description |  |
| **currency** | **String** | Billing currency (ISO 4217 code) | [default to &#39;DKK&#39;] |
| **vat_number** | **String** | Company VAT/tax ID for invoices | [optional] |
| **billing_email** | **String** | Billing email for invoices | [optional] |
| **company_name** | **String** | Legal company name | [optional] |
| **address_line1** | **String** | Address line 1 | [optional] |
| **address_line2** | **String** | Address line 2 | [optional] |
| **city** | **String** | City | [optional] |
| **postal_code** | **String** | Postal code | [optional] |
| **country** | **String** | Country (ISO 3166-1 alpha-2 code) | [optional] |
| **customs** | **Hash&lt;String, String&gt;** | Customs identifiers keyed by type | [optional] |
| **created_at** | **String** | Creation timestamp (ISO 8601) |  |
| **updated_at** | **String** | Last update timestamp (ISO 8601) |  |
| **_count** | [**GetOrg200ResponseCount**](GetOrg200ResponseCount.md) |  |  |

## Example

```ruby
require 'zippendo'

instance = Zippendo::GetOrg200Response.new(
  id: org_4d8af01qw2,
  name: Nordic Logistics ApS,
  slug: nordic-logistics,
  description: Parcel and freight logistics across the Nordics,
  currency: DKK,
  vat_number: DK12345678,
  billing_email: billing@nordic-logistics.dk,
  company_name: Nordic Logistics ApS,
  address_line1: Havnegade 12,
  address_line2: 3. sal,
  city: København,
  postal_code: 1058,
  country: DK,
  customs: {&quot;eori&quot;:&quot;DK12345678&quot;},
  created_at: 2026-06-22T14:30:00.000Z,
  updated_at: 2026-06-22T14:30:00.000Z,
  _count: null
)
```

