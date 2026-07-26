# Zippendo::CreateShipmentRequestParcelsInnerOrderLinesInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Unique order line identifier. | [optional] |
| **sku** | **String** | Stock keeping unit of the product. |  |
| **quantity** | **Integer** | Number of units in this order line. |  |
| **description** | **String** | Human-readable product description. | [optional] |
| **unit_price** | **Float** | Price per unit in the order line currency. | [optional] |
| **currency** | **String** | ISO 4217 currency code. | [optional] |
| **vat_percent** | **Float** | VAT percentage applied to the unit price. | [optional] |
| **location** | **String** | Warehouse picking location. | [optional] |
| **country_of_origin** | **String** | ISO 3166-1 alpha-2 country of origin. | [optional] |
| **tarrif_number** | **String** | Customs tariff (HS) code. | [optional] |

## Example

```ruby
require 'zippendo'

instance = Zippendo::CreateShipmentRequestParcelsInnerOrderLinesInner.new(
  id: ol_9c1d2e3f,
  sku: SKU-1024,
  quantity: 2,
  description: Wool sweater, navy,
  unit_price: 299.95,
  currency: DKK,
  vat_percent: 25,
  location: A-12-3,
  country_of_origin: DK,
  tarrif_number: 61101100
)
```

