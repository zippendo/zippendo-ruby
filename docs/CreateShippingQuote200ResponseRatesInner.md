# Zippendo::CreateShippingQuote200ResponseRatesInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **service_name** | **String** | Display name of the shipping option |  |
| **service_code** | **String** | Unique identifier for this shipping option |  |
| **total_price** | **String** | Total shipping price in cents as string |  |
| **currency** | **String** | ISO 4217 currency code |  |
| **description** | **String** | Optional description | [optional] |
| **min_delivery_date** | **String** | Minimum delivery date (ISO 8601) | [optional] |
| **max_delivery_date** | **String** | Maximum delivery date (ISO 8601) | [optional] |
| **carrier_name** | **String** | Carrier display name | [optional] |
| **carrier_slug** | **String** | Carrier slug identifier | [optional] |
| **product_id** | **String** | Carrier product ID | [optional] |
| **shipping_rule_id** | **String** | Shipping rule ID that generated this rate |  |

## Example

```ruby
require 'zippendo'

instance = Zippendo::CreateShippingQuote200ResponseRatesInner.new(
  service_name: Standard DK,
  service_code: postnord:PNL13:rule_01HZX9K2QF,
  total_price: 3900,
  currency: DKK,
  description: Standard levering i Danmark,
  min_delivery_date: 2026-06-24,
  max_delivery_date: 2026-06-26,
  carrier_name: PostNord,
  carrier_slug: postnord,
  product_id: PNL13,
  shipping_rule_id: rule_01HZX9K2QF
)
```

