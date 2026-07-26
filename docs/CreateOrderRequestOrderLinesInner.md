# Zippendo::CreateOrderRequestOrderLinesInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **sku** | **String** | Stock keeping unit identifier. | [optional] |
| **name** | **String** | Product name. |  |
| **quantity** | **Integer** | Quantity ordered. |  |
| **unit_price** | **Float** | Price per unit. | [optional] |
| **total_price** | **Float** | Total price for the line. | [optional] |
| **currency** | **String** | ISO 4217 currency code. | [optional] |
| **weight** | **Float** | Item weight in the given unit. | [optional] |
| **weight_unit** | **String** | Unit of the weight value. | [optional] |
| **variant_id** | **String** | Platform variant identifier. | [optional] |
| **product_id** | **String** | Platform product identifier. | [optional] |
| **image_url** | **String** | Product image URL. | [optional] |
| **hs_code** | **String** | Harmonized System customs code (6-13 digits). | [optional] |
| **country_of_origin** | **String** | ISO 3166-1 alpha-2 country of origin. | [optional] |
| **province_of_origin** | **String** | ISO 3166-2 province of origin. | [optional] |
| **barcode** | **String** | Item barcode (EAN/UPC). | [optional] |
| **requires_shipping** | **Boolean** | Whether the item requires shipping. | [optional] |
| **taxable** | **Boolean** | Whether the item is taxable. | [optional] |
| **gift_card** | **Boolean** | Whether the item is a gift card. | [optional] |
| **vendor** | **String** | Vendor or brand name. | [optional] |

## Example

```ruby
require 'zippendo'

instance = Zippendo::CreateOrderRequestOrderLinesInner.new(
  sku: SKU-1042-BLK,
  name: Wool Sweater,
  quantity: 2,
  unit_price: 499,
  total_price: 998,
  currency: DKK,
  weight: 0.5,
  weight_unit: kg,
  variant_id: 44218900291,
  product_id: 8123456789,
  image_url: https://cdn.example.dk/products/sweater.jpg,
  hs_code: 611020,
  country_of_origin: DK,
  province_of_origin: DK-84,
  barcode: 5712345678901,
  requires_shipping: true,
  taxable: true,
  gift_card: false,
  vendor: Norse Knits
)
```

