# Zippendo::CreateShipment201ResponseShippingRule

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Unique shipping rule identifier. |  |
| **name** | **String** | Display name of the shipping rule. |  |
| **carrier_id** | **String** | Carrier applied by the rule. |  |
| **product_id** | **String** | Carrier product applied by the rule. |  |
| **services** | **Array&lt;String&gt;** | Additional service codes applied by the rule. |  |
| **address_id** | **String** | Sender address applied by the rule. |  |
| **return_shipping_rule_id** | **String** | Shipping rule used for return shipments. | [optional] |
| **auto_create_return_shipment** | **Boolean** | Whether a return shipment is created automatically. | [optional] |
| **auto_print_labels** | **Boolean** | Whether labels are printed automatically on send. | [optional] |
| **auto_print_documents** | **Boolean** | Whether documents are printed automatically on send. | [optional] |
| **label_printer_id** | **String** | Printer used for labels. | [optional] |
| **document_printer_id** | **String** | Printer used for documents. | [optional] |

## Example

```ruby
require 'zippendo'

instance = Zippendo::CreateShipment201ResponseShippingRule.new(
  id: rule_3c4d5e6f,
  name: Domestic standard,
  carrier_id: car_pn_001,
  product_id: prod_mypack_home,
  services: [&quot;A7&quot;],
  address_id: addr_7e8f9a0b,
  return_shipping_rule_id: rule_return_01,
  auto_create_return_shipment: false,
  auto_print_labels: true,
  auto_print_documents: false,
  label_printer_id: prn_label_01,
  document_printer_id: prn_doc_01
)
```

