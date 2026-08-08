# Zippendo::UpdateOrgBrandRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **company_name** | **String** | Legal entity name printed on this brand&#39;s documents | [optional] |
| **vat_number** | **String** | VAT/tax ID for this brand&#39;s shipments and documents | [optional] |
| **customs** | **Hash&lt;String, String&gt;** | Customs identifiers keyed by type | [optional] |
| **address_line1** | **String** | Street address line 1 | [optional] |
| **address_line2** | **String** | Street address line 2 | [optional] |
| **city** | **String** | City | [optional] |
| **postal_code** | **String** | Postal code | [optional] |
| **country** | **String** | Country (ISO 3166-1 alpha-2) | [optional] |
| **primary_color** | **String** | Primary brand colour — document title and table headers | [optional] |
| **secondary_color** | **String** | Secondary brand colour — subtitle, section headings, totals accent | [optional] |
| **name** | **String** | Brand display name | [optional] |
| **slug** | **String** | URL-safe identifier, unique within the org | [optional] |
| **use_org_customs** | **Boolean** | Whether this brand ships under the organization&#39;s fiscal identity. True (the default) declares the organization&#39;s VAT number and customs identifiers and ignores the brand&#39;s own. False makes the brand&#39;s own values the sole source — nothing falls back to the organization, so an identifier the brand has not set is not declared at all. | [optional] |

## Example

```ruby
require 'zippendo'

instance = Zippendo::UpdateOrgBrandRequest.new(
  company_name: Acme ApS,
  vat_number: DK12345678,
  customs: {&quot;eori&quot;:&quot;DK12345678&quot;},
  address_line1: Vestergade 12,
  address_line2: 3. sal,
  city: København,
  postal_code: 1456,
  country: DK,
  primary_color: #1D4ED8,
  secondary_color: #F59E0B,
  name: Acme,
  slug: acme,
  use_org_customs: true
)
```

