# Zippendo::UpdateOrgRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** | Organization name | [optional] |
| **slug** | **String** | Organization slug | [optional] |
| **description** | **String** | Organization description | [optional] |
| **currency** | **String** | Billing currency (ISO 4217 code) | [optional] |
| **vat_number** | **String** | Company VAT/tax ID for invoices | [optional] |
| **overage_enabled** | **Boolean** | Allow shipments beyond plan limit (overage charges apply) | [optional] |
| **billing_email** | **String** | Billing email for invoices | [optional] |
| **company_name** | **String** | Legal company name | [optional] |
| **address_line1** | **String** | Address line 1 | [optional] |
| **address_line2** | **String** | Address line 2 | [optional] |
| **city** | **String** | City | [optional] |
| **postal_code** | **String** | Postal code | [optional] |
| **country** | **String** | Country (ISO 3166-1 alpha-2 code) | [optional] |
| **customs** | **Hash&lt;String, String&gt;** | Organization-wide customs identifiers (EORI, IOSS, VOEC, etc.); null clears all | [optional] |

## Example

```ruby
require 'zippendo'

instance = Zippendo::UpdateOrgRequest.new(
  name: Nordic Logistics ApS,
  slug: nordic-logistics,
  description: Parcel and freight logistics across the Nordics,
  currency: DKK,
  vat_number: DK12345678,
  overage_enabled: false,
  billing_email: billing@nordic-logistics.dk,
  company_name: Nordic Logistics ApS,
  address_line1: Havnegade 12,
  address_line2: 3. sal,
  city: København,
  postal_code: 1058,
  country: DK,
  customs: null
)
```

