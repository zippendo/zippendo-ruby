# Zippendo::CreateShipment201Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Unique shipment identifier. |  |
| **reference** | **String** | Customer-facing shipment reference. |  |
| **address_id** | **String** | Sender address identifier. | [optional] |
| **service_point_id** | **String** | Selected carrier service point identifier. | [optional] |
| **parties** | [**Array&lt;CreateShipment201ResponsePartiesInner&gt;**](CreateShipment201ResponsePartiesInner.md) | Parties involved in the shipment (sender, receiver, etc.). |  |
| **type** | **String** | Direction of the shipment relative to the organization. |  |
| **carrier_settings** | [**ListShipments200ResponseDataInnerCarrierSettings**](ListShipments200ResponseDataInnerCarrierSettings.md) |  |  |
| **parcels** | [**Array&lt;CreateShipment201ResponseParcelsInner&gt;**](CreateShipment201ResponseParcelsInner.md) | Parcels included in the shipment. |  |
| **pickup_details** | [**CreateShipment201ResponsePickupDetails**](CreateShipment201ResponsePickupDetails.md) |  | [optional] |
| **term_of_trade** | **String** | Incoterm governing the shipment. | [default to &#39;DAP&#39;] |
| **documents** | [**Array&lt;CreateShipment201ResponseDocumentsInner&gt;**](CreateShipment201ResponseDocumentsInner.md) | Documents generated for the shipment (labels, invoices). | [optional] |
| **errors** | [**Array&lt;CreateShipment201ResponseErrorsInner&gt;**](CreateShipment201ResponseErrorsInner.md) | Carrier errors recorded for the shipment. |  |
| **tracking** | [**CreateShipment201ResponseTracking**](CreateShipment201ResponseTracking.md) |  | [optional] |
| **status** | **String** | Lifecycle status of the shipment. |  |
| **org_id** | **String** | Owning organization identifier. |  |
| **order_id** | **String** | Associated order identifier. | [optional] |
| **shipping_rule_id** | **String** | Applied shipping rule identifier. | [optional] |
| **shipping_rule** | [**CreateShipment201ResponseShippingRule**](CreateShipment201ResponseShippingRule.md) |  | [optional] |
| **label_printer_id** | **String** | Printer assigned for labels on this shipment. | [optional] |
| **document_printer_id** | **String** | Printer assigned for documents on this shipment. | [optional] |
| **logs** | [**Array&lt;CreateShipment201ResponseLogsInner&gt;**](CreateShipment201ResponseLogsInner.md) | Request/response logs captured during carrier interactions. |  |
| **activities** | [**Array&lt;CreateShipment201ResponseActivitiesInner&gt;**](CreateShipment201ResponseActivitiesInner.md) | Chronological activity history of the shipment. |  |
| **created_at** | **String** | Timestamp when the shipment was created. |  |
| **updated_at** | **String** | Timestamp when the shipment was last updated. |  |

## Example

```ruby
require 'zippendo'

instance = Zippendo::CreateShipment201Response.new(
  id: shp_4d9e7a2f,
  reference: ORDER-1042,
  address_id: addr_7e8f9a0b,
  service_point_id: sp_pn_4521,
  parties: null,
  type: outbound,
  carrier_settings: null,
  parcels: null,
  pickup_details: null,
  term_of_trade: DAP,
  documents: null,
  errors: null,
  tracking: null,
  status: pending,
  org_id: org_1a2b3c4d,
  order_id: ord_5e6f7a8b,
  shipping_rule_id: rule_3c4d5e6f,
  shipping_rule: null,
  label_printer_id: prn_label_01,
  document_printer_id: prn_doc_01,
  logs: null,
  activities: null,
  created_at: 2026-06-22T14:30:00.000Z,
  updated_at: 2026-06-22T14:30:00.000Z
)
```

