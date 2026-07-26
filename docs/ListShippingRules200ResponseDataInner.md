# Zippendo::ListShippingRules200ResponseDataInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Unique shipping rule identifier |  |
| **name** | **String** | Shipping rule name |  |
| **description** | **String** | Optional description |  |
| **direction** | **String** | Whether this rule is for outbound or inbound (return) shipments | [default to &#39;outbound&#39;] |
| **carrier_id** | **String** | Carrier ID |  |
| **product_id** | **String** | Product ID from carrier |  |
| **services** | **Array&lt;String&gt;** | List of selected services |  |
| **additional_parameters** | [**Array&lt;ListShippingRules200ResponseDataInnerAdditionalParametersInner&gt;**](ListShippingRules200ResponseDataInnerAdditionalParametersInner.md) | Carrier-specific extra parameters. DEPRECATED array form &#x60;[{ name, val }]&#x60; where &#x60;name&#x60; is the carrier parameter &#x60;key&#x60; (from the product&#39;s &#x60;additionalParameters[].key&#x60;, e.g. &#x60;returnFunctionality&#x60;) and &#x60;val&#x60; is the stringified value. This will change to a &#x60;{ key: value }&#x60; object in a future version — writes already accept either shape. |  |
| **address_id** | **String** | Sender address ID |  |
| **receiving_countries** | **Array&lt;String&gt;** | List of supported country codes |  |
| **email_notification** | **Boolean** | Send email notification to recipient | [default to false] |
| **phone_notification** | **Boolean** | Send SMS notification to recipient | [default to false] |
| **min_weight** | **Float** | Minimum required weight in kg. Orders below this are excluded from the rule. |  |
| **max_weight** | **Float** | Maximum allowed weight in kg. Orders exceeding this are excluded from the rule. |  |
| **min_order_value** | **Float** | Minimum required order value in currency units. Orders below this are excluded from the rule. |  |
| **max_order_value** | **Float** | Maximum allowed order value in currency units. Orders exceeding this are excluded from the rule. |  |
| **conditions** | [**Array&lt;ListShippingRules200ResponseDataInnerConditionsInner&gt;**](ListShippingRules200ResponseDataInnerConditionsInner.md) | Rule conditions (weight/price/quantity) |  |
| **generate_proforma_invoice** | **Boolean** | Generate proforma invoice for shipments | [default to false] |
| **generate_commercial_invoice** | **Boolean** | Generate commercial invoice for international shipments | [default to false] |
| **generate_packing_list** | **Boolean** | Generate packing slip with package and item details | [default to false] |
| **auto_print_labels** | **Boolean** | Automatically print labels when shipment is sent | [default to false] |
| **auto_print_documents** | **Boolean** | Automatically print documents when shipment is sent | [default to false] |
| **label_printer_id** | **String** | ID of the label printer |  |
| **document_printer_id** | **String** | ID of the document printer |  |
| **return_shipping_rule_id** | **String** | ID of the return shipping rule |  |
| **auto_create_return_shipment** | **Boolean** | Automatically create and send a return shipment on dispatch | [default to false] |
| **org_id** | **String** | Owning organization ID |  |
| **created_at** | **String** | Creation timestamp (ISO 8601) |  |
| **updated_at** | **String** | Last update timestamp (ISO 8601) |  |
| **carrier** | [**ListShippingRules200ResponseDataInnerCarrier**](ListShippingRules200ResponseDataInnerCarrier.md) |  |  |
| **address** | [**ListAddresses200ResponseDataInner**](ListAddresses200ResponseDataInner.md) |  |  |
| **label_printer** | [**ListShippingRules200ResponseDataInnerLabelPrinter**](ListShippingRules200ResponseDataInnerLabelPrinter.md) |  | [optional] |
| **document_printer** | [**ListShippingRules200ResponseDataInnerLabelPrinter**](ListShippingRules200ResponseDataInnerLabelPrinter.md) |  | [optional] |
| **return_shipping_rule** | [**ListShippingRules200ResponseDataInnerReturnShippingRule**](ListShippingRules200ResponseDataInnerReturnShippingRule.md) |  | [optional] |

## Example

```ruby
require 'zippendo'

instance = Zippendo::ListShippingRules200ResponseDataInner.new(
  id: rule_01HZX9K2QF,
  name: Standard DK,
  description: Standard levering i Danmark,
  direction: outbound,
  carrier_id: carr_01HZX9K2QF,
  product_id: PNL13,
  services: [&quot;EMAIL_NOTIFICATION&quot;],
  additional_parameters: [{&quot;name&quot;:&quot;returnFunctionality&quot;,&quot;val&quot;:&quot;LABELLESS&quot;}],
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
  auto_create_return_shipment: false,
  org_id: org_01HZX9K2QF,
  created_at: 2026-06-22T09:00:00.000Z,
  updated_at: 2026-06-22T09:00:00.000Z,
  carrier: null,
  address: null,
  label_printer: null,
  document_printer: null,
  return_shipping_rule: null
)
```

