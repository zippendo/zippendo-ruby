# Zippendo::ListOrders200ResponseDataInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Unique order ID. |  |
| **order_number** | **String** | Human-readable order number. |  |
| **customer_name** | **String** | Customer full name. | [optional] |
| **customer_email** | **String** | Customer email address. | [optional] |
| **status** | **String** | Order fulfilment status derived from its shipments. |  |
| **brand_id** | **String** | Brand this record belongs to, or null when it is organization-wide |  |
| **subtotal_amount** | **Float** | Order subtotal before shipping and tax. | [optional] |
| **total_amount** | **Float** | Order grand total. | [optional] |
| **currency** | **String** | ISO 4217 currency code. | [optional] |
| **shipment_count** | **Integer** | Number of shipments created for the order. |  |
| **order_channel** | [**ListOrders200ResponseDataInnerOrderChannel**](ListOrders200ResponseDataInnerOrderChannel.md) |  |  |
| **created_at** | **String** | Creation timestamp (ISO 8601). |  |
| **updated_at** | **String** | Last update timestamp (ISO 8601). |  |

## Example

```ruby
require 'zippendo'

instance = Zippendo::ListOrders200ResponseDataInner.new(
  id: clz9k2f0a0003abcd9012mnop,
  order_number: #1042,
  customer_name: Anna Jensen,
  customer_email: anna@example.dk,
  status: processing,
  brand_id: brnd_8f3kd92ld0,
  subtotal_amount: 998,
  total_amount: 1047,
  currency: DKK,
  shipment_count: 1,
  order_channel: null,
  created_at: 2026-06-22T14:30:00.000Z,
  updated_at: 2026-06-22T14:30:00.000Z
)
```

