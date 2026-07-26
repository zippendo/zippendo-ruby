# Zippendo::CreateShippingRuleRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** | Shipping rule name |  |
| **description** | **String** | Optional description | [optional] |
| **direction** | **String** | Whether this rule is for outbound or inbound (return) shipments | [optional][default to &#39;outbound&#39;] |
| **carrier_id** | **String** | Carrier ID |  |
| **product_id** | **String** | Product ID from carrier |  |
| **services** | **Array&lt;String&gt;** | List of selected services |  |
| **additional_parameters** | [**CreateShippingRuleRequestAdditionalParameters**](CreateShippingRuleRequestAdditionalParameters.md) |  | [optional] |
| **address_id** | **String** | Sender address ID |  |
| **receiving_countries** | **Array&lt;String&gt;** | List of supported country codes |  |
| **email_notification** | **Boolean** | Send email notification to recipient | [optional][default to false] |
| **phone_notification** | **Boolean** | Send SMS notification to recipient | [optional][default to false] |
| **min_weight** | **Float** | Minimum required weight in kg | [optional] |
| **max_weight** | **Float** | Maximum allowed weight in kg | [optional] |
| **min_order_value** | **Float** | Minimum required order value in currency units | [optional] |
| **max_order_value** | **Float** | Maximum allowed order value in currency units | [optional] |
| **conditions** | [**Array&lt;CreateShippingRuleRequestConditionsInner&gt;**](CreateShippingRuleRequestConditionsInner.md) | Rule conditions (weight/price/quantity) |  |
| **generate_proforma_invoice** | **Boolean** | Generate proforma invoice for shipments | [optional][default to false] |
| **generate_commercial_invoice** | **Boolean** | Generate commercial invoice for international shipments | [optional][default to false] |
| **generate_packing_list** | **Boolean** | Generate packing slip with package and item details | [optional][default to false] |
| **auto_print_labels** | **Boolean** | Automatically print labels when shipment is sent | [optional][default to false] |
| **auto_print_documents** | **Boolean** | Automatically print documents when shipment is sent | [optional][default to false] |
| **label_printer_id** | **String** | ID of the label printer | [optional] |
| **document_printer_id** | **String** | ID of the document printer | [optional] |
| **return_shipping_rule_id** | **String** | ID of the return shipping rule | [optional] |
| **auto_create_return_shipment** | **Boolean** | Automatically create and send a return shipment on dispatch | [optional][default to false] |

## Example

```ruby
require 'zippendo'

instance = Zippendo::CreateShippingRuleRequest.new(
  name: Standard DK,
  description: Standard levering i Danmark,
  direction: outbound,
  carrier_id: carr_01HZX9K2QF,
  product_id: PNL13,
  services: [&quot;EMAIL_NOTIFICATION&quot;],
  additional_parameters: null,
  address_id: addr_01HZX9K2QF,
  receiving_countries: [&quot;DK&quot;,&quot;SE&quot;],
  email_notification: true,
  phone_notification: false,
  min_weight: 0,
  max_weight: 20,
  min_order_value: 0,
  max_order_value: 5000,
  conditions: [{&quot;type&quot;:&quot;flatRate&quot;,&quot;shippingPrice&quot;:39,&quot;currency&quot;:&quot;DKK&quot;}],
  generate_proforma_invoice: false,
  generate_commercial_invoice: false,
  generate_packing_list: false,
  auto_print_labels: false,
  auto_print_documents: false,
  label_printer_id: null,
  document_printer_id: null,
  return_shipping_rule_id: null,
  auto_create_return_shipment: false
)
```

