# Zippendo::CreateShipment201ResponseParcelsInnerOrderLinesInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Unique order line identifier. | [optional] |
| **order_line_id** | **String** | ID of the order line this packed line came from. Null when the item did not originate from an order line, such as a free gift or a replacement part. | [optional] |
| **sku** | **String** | Stock keeping unit of the product. Optional — not every webshop assigns SKUs. | [optional] |
| **quantity** | **Integer** | Number of units in this order line. |  |
| **description** | **String** | Human-readable product description. | [optional] |
| **unit_price** | **Float** | Price per unit in the order line currency. | [optional] |
| **currency** | **String** | ISO 4217 currency code. | [optional] |
| **vat_percent** | **Float** | VAT percentage applied to the unit price. | [optional] |
| **location** | **String** | Warehouse picking location. | [optional] |
| **country_of_origin** | **String** | ISO 3166-1 alpha-2 country of origin. | [optional] |
| **hs_code** | **String** | Harmonized System customs code. | [optional] |
| **tarrif_number** | **String** | Deprecated misspelling of &#x60;hsCode&#x60;, kept for backwards compatibility. | [optional] |

## Example

```ruby
require 'zippendo'

instance = Zippendo::CreateShipment201ResponseParcelsInnerOrderLinesInner.new(
  id: ol_9c1d2e3f,
  order_line_id: clz9k2f0a0004abcd3456qrst,
  sku: SKU-1024,
  quantity: 2,
  description: Wool sweater, navy,
  unit_price: 299.95,
  currency: DKK,
  vat_percent: 25,
  location: A-12-3,
  country_of_origin: DK,
  hs_code: 61101100,
  tarrif_number: 61101100
)
```

