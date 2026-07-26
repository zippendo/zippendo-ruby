# Zippendo::GetOrder200Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Unique order ID. |  |
| **order_number** | **String** | Human-readable order number. |  |
| **external_id** | **String** | Identifier of the order in the source platform. | [optional] |
| **customer_name** | **String** | Customer full name. | [optional] |
| **customer_email** | **String** | Customer email address. | [optional] |
| **shipping_address** | [**CreateOrder201ResponseShippingAddress**](CreateOrder201ResponseShippingAddress.md) |  | [optional] |
| **order_lines** | [**Array&lt;CreateOrder201ResponseOrderLinesInner&gt;**](CreateOrder201ResponseOrderLinesInner.md) | Line items in the order. |  |
| **subtotal_amount** | **Float** | Order subtotal before shipping and tax. | [optional] |
| **total_amount** | **Float** | Order grand total. | [optional] |
| **currency** | **String** | ISO 4217 currency code. | [optional] |
| **status** | **String** | Order fulfilment status derived from its shipments. |  |
| **shipping_rule_id** | **String** | ID of the applied shipping rule. | [optional] |
| **notes** | **String** | Free-form internal notes. | [optional] |
| **external_data** | **Hash&lt;String, Object&gt;** | Raw platform-specific payload for reference. | [optional] |
| **order_channel_id** | **String** | ID of the order channel this order belongs to. |  |
| **org_id** | **String** | Owning organization ID. |  |
| **created_at** | **String** | Creation timestamp (ISO 8601). |  |
| **updated_at** | **String** | Last update timestamp (ISO 8601). |  |
| **order_channel** | [**ListOrders200ResponseDataInnerOrderChannel**](ListOrders200ResponseDataInnerOrderChannel.md) |  |  |
| **shipping_rule** | [**GetOrder200ResponseShippingRule**](GetOrder200ResponseShippingRule.md) |  | [optional] |
| **shipments** | [**Array&lt;GetOrder200ResponseShipmentsInner&gt;**](GetOrder200ResponseShipmentsInner.md) |  |  |

## Example

```ruby
require 'zippendo'

instance = Zippendo::GetOrder200Response.new(
  id: clz9k2f0a0003abcd9012mnop,
  order_number: #1042,
  external_id: 5012345678901,
  customer_name: Anna Jensen,
  customer_email: anna@example.dk,
  shipping_address: null,
  order_lines: null,
  subtotal_amount: 998,
  total_amount: 1047,
  currency: DKK,
  status: processing,
  shipping_rule_id: clz9k2f0a0002abcd5678ijkl,
  notes: Leave at front desk,
  external_data: null,
  order_channel_id: clz9k2f0a0001abcd1234efgh,
  org_id: clz9k2f0a0000abcd0000zzzz,
  created_at: 2026-06-22T14:30:00.000Z,
  updated_at: 2026-06-22T14:30:00.000Z,
  order_channel: null,
  shipping_rule: null,
  shipments: null
)
```

