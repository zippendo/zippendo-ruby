# Zippendo::UpdateOrderRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **order_number** | **String** | Human-readable order number. | [optional] |
| **customer_name** | **String** | Customer full name. | [optional] |
| **customer_email** | **String** | Customer email address. | [optional] |
| **shipping_address** | [**CreateOrderRequestShippingAddress**](CreateOrderRequestShippingAddress.md) |  | [optional] |
| **order_lines** | [**Array&lt;CreateOrderRequestOrderLinesInner&gt;**](CreateOrderRequestOrderLinesInner.md) | Line items in the order. | [optional] |
| **subtotal_amount** | **Float** | Order subtotal before shipping and tax. | [optional] |
| **total_amount** | **Float** | Order grand total. | [optional] |
| **currency** | **String** | ISO 4217 currency code. | [optional] |
| **notes** | **String** | Free-form internal notes. | [optional] |
| **status** | **String** | Order fulfilment status derived from its shipments. | [optional] |
| **shipping_rule_id** | **String** | ID of the shipping rule to apply. | [optional] |

## Example

```ruby
require 'zippendo'

instance = Zippendo::UpdateOrderRequest.new(
  order_number: #1042,
  customer_name: Anna Jensen,
  customer_email: anna@example.dk,
  shipping_address: null,
  order_lines: null,
  subtotal_amount: 998,
  total_amount: 1047,
  currency: DKK,
  notes: Leave at front desk,
  status: processing,
  shipping_rule_id: clz9k2f0a0002abcd5678ijkl
)
```

