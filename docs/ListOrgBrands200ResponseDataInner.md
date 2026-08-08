# Zippendo::ListOrgBrands200ResponseDataInner

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
| **id** | **String** | Unique brand identifier |  |
| **org_id** | **String** | Owning organization |  |
| **name** | **String** | Brand display name |  |
| **slug** | **String** | URL-safe identifier, unique within the organization |  |
| **use_org_customs** | **Boolean** | Whether this brand ships under the organization&#39;s fiscal identity. True (the default) declares the organization&#39;s VAT number and customs identifiers and ignores the brand&#39;s own. False makes the brand&#39;s own values the sole source — nothing falls back to the organization, so an identifier the brand has not set is not declared at all. |  |
| **logo_url** | **String** | Authenticated URL for the brand logo, or null when none is set |  |
| **archived_at** | **String** | When the brand was archived; null when active |  |
| **created_at** | **String** | Creation timestamp (ISO 8601) |  |
| **updated_at** | **String** | Last update timestamp (ISO 8601) |  |

## Example

```ruby
require 'zippendo'

instance = Zippendo::ListOrgBrands200ResponseDataInner.new(
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
  id: brnd_8f3kd92ld0,
  org_id: org_8f3kd92ld0,
  name: Acme,
  slug: acme,
  use_org_customs: true,
  logo_url: /orgs/org_1/brands/brnd_1/logo,
  archived_at: 2026-08-05T10:00:00.000Z,
  created_at: 2026-06-22T14:30:00.000Z,
  updated_at: 2026-06-22T14:30:00.000Z
)
```

