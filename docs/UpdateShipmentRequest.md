# Zippendo::UpdateShipmentRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **reference** | **String** | Customer-facing shipment reference. | [optional] |
| **address_id** | **String** | Sender address identifier. | [optional] |
| **service_point_id** | **String** | Selected carrier service point identifier. | [optional] |
| **parties** | [**Array&lt;CreateShipmentRequestPartiesInner&gt;**](CreateShipmentRequestPartiesInner.md) | Parties involved in the shipment. Optional when orderId is provided. | [optional] |
| **type** | **String** | Direction of the shipment relative to the organization. | [optional] |
| **carrier_settings** | [**CreateShipmentRequestCarrierSettings**](CreateShipmentRequestCarrierSettings.md) |  | [optional] |
| **parcels** | [**Array&lt;CreateShipmentRequestParcelsInner&gt;**](CreateShipmentRequestParcelsInner.md) | Parcels to include. Optional when orderId is provided. | [optional] |
| **pickup_details** | [**CreateShipmentRequestPickupDetails**](CreateShipmentRequestPickupDetails.md) |  | [optional] |
| **term_of_trade** | **String** | Incoterm governing the shipment. | [optional][default to &#39;DAP&#39;] |
| **status** | **String** | Lifecycle status of the shipment. | [optional][default to &#39;pending&#39;] |
| **order_id** | **String** | Order to derive parties and parcels from. | [optional] |
| **label_printer_id** | **String** | Printer to assign for labels. | [optional] |
| **document_printer_id** | **String** | Printer to assign for documents. | [optional] |
| **shipping_rule_id** | **String** | Shipping rule to apply to the shipment. Pass null to clear. | [optional] |

## Example

```ruby
require 'zippendo'

instance = Zippendo::UpdateShipmentRequest.new(
  reference: ORDER-1042,
  address_id: addr_7e8f9a0b,
  service_point_id: sp_pn_4521,
  parties: null,
  type: outbound,
  carrier_settings: null,
  parcels: null,
  pickup_details: null,
  term_of_trade: DAP,
  status: pending,
  order_id: ord_5e6f7a8b,
  label_printer_id: prn_label_01,
  document_printer_id: prn_doc_01,
  shipping_rule_id: rule_3c4d5e6f
)
```

