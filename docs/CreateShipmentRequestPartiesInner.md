# Zippendo::CreateShipmentRequestPartiesInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** | Role of the party in the shipment. |  |
| **name** | **String** | Full name or company name of the party. |  |
| **attention** | **String** | Attention contact at the party. | [optional] |
| **address1** | **String** | Primary street address line. |  |
| **address2** | **String** | Secondary address line. | [optional] |
| **postal_code** | **String** | Postal code of the party address. |  |
| **city** | **String** | City of the party address. |  |
| **country_code** | **String** | ISO 3166-1 alpha-2 country code. |  |
| **email** | **String** | Email address of the party. | [optional] |
| **phone** | **String** | Phone number of the party in E.164 format. | [optional] |
| **attributes** | [**Array&lt;CreateShipmentRequestPartiesInnerAttributesInner&gt;**](CreateShipmentRequestPartiesInnerAttributesInner.md) | Additional carrier-specific attributes for the party. | [optional] |

## Example

```ruby
require 'zippendo'

instance = Zippendo::CreateShipmentRequestPartiesInner.new(
  type: receiver,
  name: Anna Jensen,
  attention: Reception,
  address1: Vesterbrogade 12,
  address2: 2. sal,
  postal_code: 1620,
  city: København V,
  country_code: DK,
  email: anna@example.dk,
  phone: +4520123456,
  attributes: null
)
```

