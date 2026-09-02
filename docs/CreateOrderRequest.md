# Zippendo::CreateOrderRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **order_number** | **String** | Human-readable order number. |  |
| **external_id** | **String** | Identifier of the order in the source platform. | [optional] |
| **order_channel_id** | **String** | ID of the order channel this order belongs to. |  |
| **customer_name** | **String** | Customer full name. | [optional] |
| **customer_email** | **String** | Customer email address. | [optional] |
| **shipping_address** | [**CreateOrderRequestShippingAddress**](CreateOrderRequestShippingAddress.md) |  | [optional] |
| **order_lines** | [**Array&lt;CreateOrderRequestOrderLinesInner&gt;**](CreateOrderRequestOrderLinesInner.md) | Line items in the order. |  |
| **subtotal_amount** | **Float** | Order subtotal before shipping and tax. | [optional] |
| **total_amount** | **Float** | Order grand total. | [optional] |
| **currency** | **String** | ISO 4217 currency code. | [optional] |
| **notes** | **String** | Free-form internal notes. | [optional] |
| **shipping_rule_id** | **String** | Shipping rule to ship this order with. When set, a shipment is created immediately (and dispatched if the channel has autoShipOnCreate enabled). | [optional] |
| **shipping_method_title** | **String** | Shipping-method title from the source checkout; matched against the order channel&#39;s shipping-method mappings to pick a shipping rule. | [optional] |
| **external_data** | **Hash&lt;String, Object&gt;** | Raw platform-specific payload for reference. | [optional] |

## Example

```ruby
require 'zippendo'

instance = Zippendo::CreateOrderRequest.new(
  order_number: #1042,
  external_id: 5012345678901,
  order_channel_id: clz9k2f0a0001abcd1234efgh,
  customer_name: Anna Jensen,
  customer_email: anna@example.dk,
  shipping_address: null,
  order_lines: null,
  subtotal_amount: 998,
  total_amount: 1047,
  currency: DKK,
  notes: Leave at front desk,
  shipping_rule_id: clz9k2f0a0007abcd2468qrst,
  shipping_method_title: GLS Hjemmelevering,
  external_data: null
)
```

