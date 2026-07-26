# Zippendo::CreateShippingQuoteRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **destination** | [**CreateShippingQuoteRequestDestination**](CreateShippingQuoteRequestDestination.md) |  |  |
| **items** | [**Array&lt;CreateShippingQuoteRequestItemsInner&gt;**](CreateShippingQuoteRequestItemsInner.md) | Cart items |  |
| **currency** | **String** | ISO 4217 currency code |  |
| **total_price_cents** | **Float** | Total price in cents after discounts (optional, enables total-based conditions) | [optional] |

## Example

```ruby
require 'zippendo'

instance = Zippendo::CreateShippingQuoteRequest.new(
  destination: null,
  items: [{&quot;name&quot;:&quot;Uld trøje&quot;,&quot;quantity&quot;:2,&quot;grams&quot;:500,&quot;price&quot;:29900}],
  currency: DKK,
  total_price_cents: 59800
)
```

